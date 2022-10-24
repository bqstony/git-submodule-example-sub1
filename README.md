# git-submodule-example-sub1 

This repository can used as a example of a submodule for a project.

**How To add this repository as git submodule **

Execute the following command in your project root folder:

```cmd
git submodule add -b main --name git-submodule-example-sub1 https://github.com/bqstony/git-submodule-example-sub1.git .\source\submodules\git-submodule-example-sub1
```

This creates a file named `.gitmodules` with the entry:

```
[submodule "git-submodule-example-sub1"]
	path = .\\source\\submodules\\git-submodule-example-sub1
	url = https://github.com/bqstony/git-submodule-example-sub1.git
	branch = master
```

_QA_

fatal: no submodule mapping found in .gitmodules for path 'source/submodules/iotnetlib'
Example:

```cmd
git submodule status
fatal: no submodule mapping found in .gitmodules for path 'source/submodules/iotnetlib'
```

simply clear the git cache

```cmd
git rm --cached .\source\submodules\git-submodule-example-sub1\
git submodule update --init --recursive
```