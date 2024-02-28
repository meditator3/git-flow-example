# git-flow-example
git-flow example of feature/prod/dev/hotfix from v1.0 to v2.0 to v2.0.1

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
