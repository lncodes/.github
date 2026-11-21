# Contributing to Last Night Codes

Thanks for helping improve these examples! This guide covers questions, issues and pull requests for every repository in the [lncodes](https://github.com/lncodes) organization.

## Questions and ideas

Use the repository's **Discussions** tab where it is enabled, or comment on the related post at [lncodes.com](https://www.lncodes.com). If neither fits, open an issue. Issues are mainly for concrete bugs and changes.

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
3. Make the change and check it the way that repository's README describes:
   - **C# repositories** (`csharp-*`, requires the [.NET 10 SDK](https://dotnet.microsoft.com/download)): from the repository root, run
     ```bash
     dotnet build
     dotnet test
     ```
   - **Unity repositories**: follow the setup steps in the README and confirm the project opens in Unity without console errors.
   - **Documentation-only repositories** (`docs`, `.github`): preview the Markdown and check that every link works.
4. Stage only the files for this change and review the staged diff:
   ```bash
   git add -- path/to/changed/file.cs
   git diff --cached
   git commit -m "fix(search): correct the binary search upper bound"
   ```
   For Unity, stage each added, moved, or removed asset with its `.meta` file and preserve the GUID when moving an asset.
5. Push the topic branch and open a pull request against `main` unless the repository documents another target. Complete the PR template and report any checks you could not run.

### Commit messages and pull request titles

Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) with `type(scope): subject`; omit `(scope)` when it does not add context. Use `feat`, `fix`, `refactor`, `perf`, `test`, `docs`, `build`, `ci`, `chore`, `style`, or `revert`. Start the subject with a lowercase imperative verb (for example, `correct`), omit the final period, and keep the authored title to 72 characters or fewer. When a longer explanation helps, leave a blank line and explain why the change is needed. For a breaking change, add `!` before the colon and include a `BREAKING CHANGE:` note in the commit body and PR description.

Use the same format for the PR title: repositories that squash with the PR title use it as the basis for the commit on the target branch. Maintainers should preserve any required `BREAKING CHANGE:` note when confirming the squash message. This convention applies to new work; do not rewrite already published history to match it.

## Pull request guidelines

- **One topic per pull request.** Separate unrelated fixes into separate pull requests.
- **Explain the change** in the description and link the issue (`Fixes #123`).
- **Add or update tests** when you change behavior. Before merging, check the latest PR revision and wait for required CI checks to pass where configured. Do not count failed or unrun checks as passed.
- **Update the folder's README** when commands, files or behavior change.
- **Match the surrounding style.** In the C# repositories, the target framework and package versions are set once in `Directory.Build.props` and `Directory.Packages.props`; don't override them per project.
- A maintainer reviews every pull request. Respond to feedback by pushing new commits to the same branch.

## Code of Conduct

By participating you agree to the [Code of Conduct](https://github.com/lncodes/.github/blob/main/CODE_OF_CONDUCT.md).
