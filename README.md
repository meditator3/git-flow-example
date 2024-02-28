# git-flow-example
git-flow example of feature/prod/dev/hotfix from v1.0 to v2.0 to v2.0.1

in this process we maintain a gitops ethic to FFW to main only. we are not allowing merge commit branching. 
this is via branch rules(in settings) select option only linear history.

process:
started at v1.0 with file 

added develop branch:
file2, file3

so current branches: dev:2 files, main:1 file

locked branches main+develop to allow only via pull request
you can try to push into develop or main, but they are locked(in setting>branches>not allow bypassing option)

and can be add/modify files only via new branch> hencforth-

add the new branch (because of locked) feature/ariel :

(from git) git push --set-upstream origin feature/ariel (incase git push origin feature/ariel didnt work)
added file4, file5 (to feature/ariel)

now, feature/ariel has file-file5, but develop and main can't have it because they are locked.
dev:2 files, mian: still 1 file


next, we want to update/merge the deveop branch ONLY.
so we use pull request but from feature/ariel to develop (not main)
we see if we can actually do merge commit-not squash- if not-change it with setting>general>allow merge commit.
-close the pull request.
next, we have a hotshot who can develop even better feature-
so we open a new branch for him, feature/hotshot from develop

now, the hotshot also wants to pull request, because he's better than ariel. of course from develop to noa.
because the Team Leader loves the hotshot, he authorized the merge.
because he loves the hotshot so much he even allowed squash and merge!

next, we want to have better visualization so we use --git kraken-- to look at it, using this repo. downlaod-install and authorize this repo.
currently: develop has 3 files-two old 2, and the great_feature from hotshot branch

but hotshot forgot something, and updated the "great feature".
created a pull request, and squash and merged into develop. because he is a loved hotshot

next, ariel wants to pull request his files to develop branch, with pull request.
but his boss doesn't like him as much, so he allows only with "merge commit"

now, we have advanced to version2.0.0
so ariel tags it: git tag -a v2.0 -m "version 2.0"
and has to push the tag into the repo, using:

git push --tags origin feature/ariel

and now it is also in develop (v2), everyone knows, now i have to bring the new version to production>to main.

but there's a condition- we merge it from develop to main. to maintain the FFW. we don't allow merge commit(at first that was the condition), to make it more organised. 



