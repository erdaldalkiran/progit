#Chapter 2 Notes
##add command
git add is a multipurpose command. You use it **to begin
tracking new files, to stage files, and to do other things like marking merge conflicted files as resolved**. It may be helpful to think of it more as “add this content to the next commit” rather than “add this file to the project”.

##git status short
**git status -s**

New files that aren’t tracked have a ?? next to them, new files that have
been added to the staging area have an A , modified files have an M and so on.
There are two columns to the output - the left hand column indicates that the
file is staged and the right hand column indicates that it’s modified.

For an example, check page 49.

##git diff
**git diff**

To see what you have changed but not staged

**git diff --staged/--cached**

To see the changes you have staged

**git difftool**

To see the changes through GUI

##git rm file_name

To remove file from working directory and stage it.

##git rm --cached file_name

To remove file from staged area but keep it in the working directory

##git log
|Common git log options                                       ||
|-------------------------------------------------------------|:-:|
|Option         | Description                                   |
|-p             | Show the patch introduced with each commit    |
|--stat         | Show statistics for files modified in each commit|
|--shortstat    | Display only the changed/insertions/deletions line from the --stat command|
|--name-only    | Show the list of files modified after the commit information|
|--name-status  | Show the list of files affected with added/modified/deleted information as well|
|--abbrev-commit| Show only the first few characters of the SHA-1 checksum instead of all 40|
|--relative-date| Display the date in a relative format|
|--graph        | Display an ASCII graph of the branch and merge history beside the log output|
|--pretty       | Show commits in an alternate format. Options include oneline, short, full, fuller, and format|


|Useful options for git log --pretty=format        |
|--------------------------------------------------|
|Option      | Description of Output               |
|%H          | Commit hash                         |
|%h          | Abbreviated commit hash             |
|%T          | Tree hash                           |
|%t          | Abbreviated tree hash               |
|%P          | Parent hashes                       |
|%p          | Abbreviated parent hashes           |
|%an         | Author name                         |
|%ae         | Author email                        |
|%ad         | Author date                         |
|%ar         | Author date, relative               |
|%cn         | Committer name                      |
|%ce         | Committer email                     |
|%cr         | Committer date, relative            |
|%cd         | Committer date                      |
|%s          | Subject                             |


|Options to limit the output of git log                   |
|---------------------------------------------------------|
| Option           | Description                          |
| -(n)             | Show only the last n commits.        |
| --since, --after | Limit the commits to those made after the specified date |
| --until, --before| Limit the commits to those made before the specified date |
| --author         | Only show commits in which the author entry matches the specified string |
| --committer      | Only show commits in which the committer entry matches the specified string |
| --grep           | Only show commits with a commit message containing the string |
| -S               | Only show commit adding or removing code mathcing the string |
