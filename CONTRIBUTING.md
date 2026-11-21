# Contributing to Last Night Codes

Thanks for helping improve these examples! This guide covers questions, issues and pull requests for every repository in the [lncodes](https://github.com/lncodes) organization.

## Questions and ideas

Use the repository's **Discussions** tab, or comment on the related post at [lncodes.com](https://www.lncodes.com). Issues are for concrete bugs and changes.

## Reporting an issue

1. Search the repository's **Issues** first. If a closed issue still applies, open a new one and link to it.
2. Open **Issues → New issue** and choose a form:
   - **Bug report**: something builds, runs or behaves incorrectly.
   - **Feature request**: a new example, pattern, algorithm or capability.
   - **Code refinement**: readability, naming, structure or performance, with no behavior change.
   - **Documentation or tests**: README, comments or unit tests.
3. Security problems must **not** go in a public issue; follow the [Security Policy](https://github.com/lncodes/.github/blob/main/SECURITY.md).

## Submitting a change

1. Fork the repository and clone your fork:
   ```bash
   git clone https://github.com/<your-username>/<repository>.git
   ```
2. Create a branch from `main`, named after the work, for example `fix/binary-search-bounds` or `feature/composite-pattern`:
   ```bash
   git switch -c fix/binary-search-bounds
   ```
3. Make the change, then build and test from the repository root (requires the [.NET 10 SDK](https://dotnet.microsoft.com/download)):
   ```bash
   dotnet build
   dotnet test
   ```
4. Commit only the files you changed, with a message that says what and why:
   ```bash
   git add path/to/changed/file.cs
   git commit -m "Fix off-by-one in BinarySearch upper bound"
   ```
5. Push the branch and open a pull request against `main`, completing the template's checklist.

## Pull request guidelines

- **One topic per pull request.** Separate unrelated fixes into separate pull requests.
- **Explain the change** in the description and link the issue (`Fixes #123`).
- **Add or update tests** when you change behavior; CI must pass before review.
- **Update the folder's README** when commands, files or behavior change.
- **Match the surrounding style.** The target framework and package versions are set once in `Directory.Build.props` and `Directory.Packages.props`; don't override them per project.
- A maintainer reviews every pull request. Respond to feedback by pushing new commits to the same branch.

## Code of Conduct

By participating you agree to the [Code of Conduct](https://github.com/lncodes/.github/blob/main/CODE_OF_CONDUCT.md).
