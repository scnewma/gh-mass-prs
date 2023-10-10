# gh-mass-prs

A simple extension to interactively search, approve, merge PRs from the CLI.

## Requirements:

* [fzf](https://github.com/junegunn/fzf)

## Install

```
gh extension install scnewma/gh-mass-prs
```

## Example Usage

This extension is an interactive wrapper on top of `gh search prs` so you can
provide the same flags to it as to `gh search prs`.

```
# view open PRs waiting for your review
$ gh mass-prs --state=open --review-requested=@me

# view dependabot PRs waiting for your review
$ gh mass-prs --state=open --review-requested=@me --label dependencies --archived=false
```

When in the FZF window, you have the following actions available to you.

* `ctrl-a`: approve the PR
* `ctrl-g`: merge the PR
* `ctrl-e`: approve and merge the PR

## Troubleshooting

### Pull request Auto merge is not allowed for this repository

```
GraphQL: Pull request Auto merge is not allowed for this repository (enablePullRequestAutoMerge)
```

See [GitHub documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/automatically-merging-a-pull-request) for enabling auto-merge.
