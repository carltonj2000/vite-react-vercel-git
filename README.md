# Vite React Project To Test Vercel Release Procedure

Thinking of following the `github-flow` model for releases.

- https://docs.github.com/en/get-started/using-github/github-flow

## History

1 - Created a vite project - a react website
2 - Customized and simplified the website content
3 - Create a git repo, commit and pushed to github
4 - Create a branch and add a feature or fix bug/documentation/etc
5 - Commit the branch, push to github and submit pull request.
6 - Use the `gh` cli merge command to merge the pr and delete the branch
7 - Use the `gh` cli issue command to close the issue and reference the pr

### Example Commands

Go to checkout example below best summary of commands.

```bash
# create issue
git branch --list
git branch -d update2v0p2
git add .
git commit -m 'update version to 0.2'
git push --set-upstream origin update2v0p2
gh pr checkout 4
gh pr merge
gh issue close 3 -c 'closed #4'

gh auth login
gh status
gh repo list -L 600
gh issue create
git checkout -b update2v0p3
gh pr create
gh issue list -s all
gh --help

# a checkout example
gh issue create # star a change by noting a goal. note #
## can make changes to the main branch but don't commit them
git switch -c update2v0p4 # switch changes to a new/goal branch
git add .
git commit -m 'update version to 0.4'
git push --set-upstream origin update2v0p2
# create pull request for the present changes
gh pr create --title "update version to 0.4" --body "for issue #5"
# merge pull request into the main branch and delete goal branches
gh pr merge --title "update version to 0.4" --body "closed #6"
# close issue associate with the goal/feature pull request
gh issue close 5 -c 'close #5'
```
