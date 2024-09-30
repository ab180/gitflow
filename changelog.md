## 2.3.1

- fix: solve issue that auto-unreleased-commit feature is not working

## 2.3.0

- feature: add dependabot to default feature branches

## 2.2.4

- fix: solve issue that gitflow is failed if source branch is removed

## 2.2.3

- fix: solve issue that CHANGELOG input is not used on everywhere

## 2.2.2

- feature: add Unreleased to changelog if necessary

## 2.2.1

- fix: use TOKEN instead of GITHUB_TOKEN

## 2.2.0

- feature: support fetching github token from github app

## 2.1.2

- fix: solve issue that DEVELOP_BRANCH input is not used

## 2.1.1

- fix: solve issue that github token is not applied to github command line tool

## 2.1.0

- feature: add customizable feature

## 2.0.0

- change: make gitflow as reusable workflow
- change: do not close pull request if branch do not satisfy condition
- change: make gitflow works with one job

## 1.1.2

- fix: solve issue that workflow do not work every modification of pull request

## 1.1.1

- change: replace (release/ or hotfix/ => develop) merge with pull request

## 1.1.0

- fix: solve issue that release/ or hotfix/ branch can not be merged to develop branch when branch protection rules are applied on develop branch
- feature: when (feature/ => develop) pull request is merged, github actions remove feature/ branch
- feature: when (release/ or hotfix/ => main) pull request is merged, github actions remove release/ or hotfix/ branch

## 1.0.0

- feature: when pull reqeust, github actions check pull request is (release/ or hotfix/ => main) or (feature/ => develop), if not github actions close the pull request
- feature: when (feature/ => develop) pull request, github actions check changelog.md is modified, if not github actions add comment to recommend modifying changelog.md
- feature: when (feature/ => develop) pull request, github actions check changelog.md contains '## Unreleased' sentence, if not github actions close the pull request
- feature: when (release/ or hotfix/ => main) pull request, github actions check source branch's name in 'type/0.0.0' format, if not github actions close the pull request
- feature: when (release/ or hotfix/ => main) pull request, github actions check changelog.md contains not '## Unreleased' sentence, if not github actions close the pull request
- feature: when (release/ or hotfix/ => main) pull request, github actions check changelog.md contains '## $VERSION' sentence, if not github actions close the pull request
- feature: when (release/ or hotfix/ => main) pull request, github actions check changelog.md's content of '## $VERSION' is not empty, if not github actions close the pull request
- feature: when (release/ or hotfix/ => main) pull request is merged, github actions create '$VERSION' tag and '$VERSION' release, append changelog.md's content of '## $VERSION' to release note, append result of github's generate release note feature to release note
- feature: when (release/ or hotfix/ => main) pull request is merged, github actions create and merge (release/ or hotfix/ => develop) pull request
