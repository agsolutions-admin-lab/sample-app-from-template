# Main Branch Protection Rules

## Purpose

The `main` branch is protected to ensure that changes are reviewed before they are merged into the repository.

## Ruleset

Ruleset name: `Protect Main Branch`

Target branch: `main`

Enforcement status: Active

## Configured Rules

- Pull requests are required before merging into `main`.
- At least 1 approving review is required.
- Direct changes to `main` should be made through a pull request.
- Force pushes are blocked.
- Branch deletion is restricted.
- Pull request conversations must be resolved before merging.

## Test Performed

The branch protection rules were tested using a separate feature branch.

1. A change was made to `README.md` on a separate branch.
2. A pull request was opened from the feature branch into `main`.
3. GitHub blocked the merge because one approving review was required.
4. A second GitHub account with the required repository access reviewed the changes.
5. The reviewer approved the pull request.
6. After approval, GitHub allowed the pull request to be merged.
7. The pull request was successfully merged into `main`.

## Result

The test confirmed that the configured ruleset successfully prevents an unreviewed pull request from being merged into the `main` branch.
