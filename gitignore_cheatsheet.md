# Gitignore Cheatsheet

The `.gitignore` file is used to specify intentionally untracked files to ignore. It uses glob patterns to match files and directories.

### Rules for Matching Patterns in .gitignore Files

| Pattern            |                                             Explanations/Matches                                             |                                                                Examples |
| ------------------ | :----------------------------------------------------------------------------------------------------------: | ----------------------------------------------------------------------: |
| \*\*/lib/name.file |    Starting with \*\* before / specifies that it matches any folder in the repository. Not just on root.     |                                      /lib/name.file /test/lib/name.file |
| lib/name.file      | Patterns specifying files in specific folders are always relative to root (even if you do not start with / ) |                                                          /lib/name.file |
| \*\*/name          |                          All name folders, and files and folders in any name folder                          |                    /name/log.file /lib/name/log.file /name/lib/log.file |
| /lib/\*\*/name     |              All name folders, and files and folders in any name folder within the lib folder.               | /lib/name/log.file /lib/test/name/log.file /lib/test/ver1/name/log.file |
| \*.file            |                                       All files withe .file extention                                        |                                               /name.file /lib/name.file |
