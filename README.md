# Vite React Project To Test Vercel Release Procedure

Thinking of following the `github-flow` model for releases.

- https://docs.github.com/en/get-started/using-github/github-flow

## History

1 - Created a vite project - a react website
2 - Customized and simplified the website content
3 - Create a git repo, commit and pushed to github
4 - Create a branch and add a feature or fix bug/documentation/etc
5 - Commit the branch, push to github and submit pull request.

### Example Commands

```bash
# create issue
git branch --list
git branch -d update2v0p2
# merge branch
git pull

gh auth login
gh status
gh repo list -L 600
gh issue create
git checkout -b update2v0p3
gh pr create
gh --help
```
