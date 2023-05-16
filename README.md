[![CI/CD](https://github.com/you54f/gh-releases-report/actions/workflows/test.yml/badge.svg)](https://github.com/you54f/gh-releasse-report/actions/workflows/test.yml)

# gh-releases-report

A `gh` CLI extension that reports and visualizes GitHub respostories release's total
download count, as well as the individual download counts for each of its assets.

It can optionally search across an entire GitHub user or organisation, and perform the same
for each repo.

## Usage

Inspect the download counts associated with a particular GitHub repositories release:

```
    gh releases-report --repo cli/cli
```

Inspect the download counts associated with a particular GitHub organisations releases for each repository:

```
    gh releases-report --org cli
```

## Help

```
  usage:
    gh releases-report --repo <repo>
    gh releases-report --org <org>

  commands:
    gh releases-report --repo <repo>     shows the list of download stats for all release assets for the specified repo
    gh releases-report --org <user/org>  shows the list of download stats for all release assets for all repos in the specified org

  [options]
    -h, --help                  Display the help information
    -o, --org <user/org>        Specify the user or org to list the repos for
    -r, --repo <repo>           Specify the repo to list the releases for

  source code: https://github.com/you54f/gh-releases-report
  credits: https://github.com/mdb/gh-release-report

```

By default, the `repo` is set to `you54f/pact-ruby-standalone`
By default, the `org` is set to `you54f/safdotdev`

## Installation

### Pre-requisities

Install the `gh` CLI [for your platform](https://github.com/cli/cli#installation). For example, on Mac OS:

```
brew install gh
```

Install the `jq` CLI [for your platform](https://stedolan.github.io/jq/download/). For example, on Mac OS:

```
brew install jq
```

It relies on [gh-release-report](https://github.com/mdb/gh-release-report), this tool will attempt to brute install it for you :)

### Install the extension

Install the latest `releases-report` extension from [its releases](https://github.com/mdb/gh-releases-report/releases):

```
gh extension install you54f/gh-releases-report
```

## Development

Build and test `gh-releases-report` locally:

```
git clone https://github.com/YOU54F/gh-releases-report.git
cd gh-releases-report
gh extension install .
```
