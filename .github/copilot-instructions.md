# Project Guidelines

## Mandatory Development Checklist
Run from repository root before finishing any change.

- [ ] Lint/analyzers: `dotnet build SocOps/SocOps.csproj -warnaserror`
- [ ] Build: `dotnet build SocOps/SocOps.csproj`
- [ ] Test: `dotnet test`

## Architecture
Blazor WASM single-game flow:
- Entry/DI: `SocOps/Program.cs`; routing: `SocOps/App.razor`; main page: `SocOps/Pages/Home.razor`
- UI: `SocOps/Components/`; state orchestration: `SocOps/Services/BingoGameService.cs`; game rules: `SocOps/Services/BingoLogicService.cs`
- Models/data: `SocOps/Models/`, `SocOps/Data/Questions.cs`

## Conventions
- Prefer existing custom utility classes in `SocOps/wwwroot/css/app.css` for styling.
- Keep game rules in `BingoLogicService` and UI/state transitions in `BingoGameService`.
- Follow page lifecycle pattern in `SocOps/Pages/Home.razor` (subscribe in init, unsubscribe in `Dispose`).
- Keep components parameter-driven (`EventCallback`, simple `[Parameter]` props); `Counter`/`Weather` are scaffold pages.

## Pitfalls and Workspace Notes
- Do not edit generated outputs in `bin/` or `obj/`.
- Ignore `.solutions/` for production edits (workshop checkpoints only).
- Dev URL default: `http://localhost:5166` in `SocOps/Properties/launchSettings.json`.

## Related Docs
Prefer links over duplication:
- `README.md`, `CONTRIBUTING.md`, `workshop/GUIDE.md`, `workshop/01-setup.md`
- `.github/instructions/frontend-design.instructions.md`, `.github/instructions/css-utilities.instructions.md`
