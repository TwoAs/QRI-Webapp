## Github Procedure and Practices

This doc is intended to standardize our github procedures and practices.

### Branches

All commits must be made to a non-protected branch and submitted via a pull request. Naming these branches is important for filtering, so we will be using these keywords for naming branches:

> branches should be all lower case and have NO whitespace (use `-` instead of spaces)

- docs/*
- feature/*
- hotfix/*


Both [QRI-back](https://github.com/TwoAs/QRI-Back) and [QRI-front](https://github.com/TwoAs/QRI-Front) will have two protected branches. The first being `master` which will be used for production and will match the latest stable build. The second being `develop` which we will use when developing our code (this makes things easier for certain workflows).

### Commits

**Make sure you are on a non-protected branch before committing!**
Commits should be limited to only 40 characters in the summary. Any additional info will be in the description of the commit. Commits can start with any of the following keywords and CAN contain whitespace:

> commit messages are not limited to just these, just make sure the first word of your commit message is capitalized

- Add
- Delete
- Update
- Rename
- Fix

### Pull Requests

PRs require at least one reviewer and may or may not require checks before merging. Please make sure your code passes all checks before submitting a PR for review. If a PR closes/references an issue please make a comment of it and add the issue number with `#`.

### Issues

Issues can be named and handled any way you want, just make sure you label them accordingly so the can be easily filtered. If an issue is blocked by another issue or PR, make sure you label it **blocked** and reference the problem using `#` in the description. Link any open PRs that resolve the issue.
