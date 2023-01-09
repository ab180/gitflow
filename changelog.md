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
