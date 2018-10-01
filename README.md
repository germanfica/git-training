# git-training
## Untrack files
Use this when:
1. You want to untrack a lot of files, or
2. You updated your gitignore file
Source link: http://www.codeblocq.com/2016/01/Untrack-files-already-added-to-git-repository-based-on-gitignore/

Let’s say you have already added/committed some files to your git repository and you then add them to your .gitignore; these files will still be present in your repository index. This article we will see how to get rid of them.

Step 1: Commit all your changes
Before proceeding, make sure all your changes are committed, including your .gitignore file.

Step 2: Remove everything from the repository
To clear your repo, use:

git rm -r --cached .
rm is the remove command
-r will allow recursive removal
–cached will only remove files from the index. Your files will still be there.
The rm command can be unforgiving. If you wish to try what it does beforehand, add the -n or --dry-run flag to test things out.

Step 3: Re add everything
git add .
Step 4: Commit
git commit -m ".gitignore fix"
Your repository is clean :)

Push the changes to your remote to see the changes effective there as well.

<b>Credits:</b>
[Dheeraj Bhaskar](https://stackoverflow.com/users/1311745/dheeraj-bhaskar)
