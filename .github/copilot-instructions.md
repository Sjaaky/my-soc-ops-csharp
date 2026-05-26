# Copilot Workspace Instructions

## Mandatory Development Checklist

Before finishing any change:

- [ ] Lint or diagnostics are clean
- [ ] `dotnet build SocOps/SocOps.csproj` succeeds
- [ ] `dotnet test` succeeds when test projects exist

## Project Map

- Blazor WebAssembly app targeting .NET 10
- `SocOps/Program.cs` boots the app and registers `BingoGameService`
- `SocOps/Pages/Home.razor` is the main page and controls start, play, and bingo states
- `SocOps/Components/` contains the UI surface
- `SocOps/Services/BingoGameService.cs` manages app state and `localStorage`
- `SocOps/Services/BingoLogicService.cs` contains board and win logic
- `SocOps/Data/Questions.cs` provides the bingo prompts

## Working Rules

- Make small, focused changes
- Keep rules in `BingoLogicService` and UI state in `BingoGameService`
- Reuse utilities from `SocOps/wwwroot/css/app.css` before adding styles
- Follow `.github/instructions/css-utilities.instructions.md` for styling details
- Follow `.github/instructions/frontend-design.instructions.md` for design tasks
