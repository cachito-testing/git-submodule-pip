# git-submodule-pip

Repo for testing how Cachito handles [Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules). <br/>
Such repos can be identified with `[submodule "<submodule path>"]` sections* in `.gitmodules`. <br/>

Also, it turns out that Cachito handles Git submodules better than Git itself does.
Git actually does not provide the contents inside of submodules in its [tarball](https://github.com/cachito-testing/git-submodule-pip/tarball/6ff2f48835a224c0b170c2c79f48d8507aed89d7).
This particular case is handled with [another repository](https://github.com/cachito-testing/git-submodule-pip-tarball) which contains the same exact contents, but treats the submodule as a normal directory. <br/>

There are **3** of these repos - for package managers pip, npm, and Yarn: <br/>
1. **pip repo with a pip Git submodule** <br/>
2. [npm repo with a npm Git submodule](https://github.com/cachito-testing/git-submodule-npm) <br/>
3. [Yarn repo with a Yarn Git submodule](https://github.com/cachito-testing/git-submodule-yarn) <br/>

This particular repo is essentially [cachito-pip-without-deps](https://github.com/cachito-testing/cachito-pip-without-deps) containing [cachito-pip-with-deps](https://github.com/cachito-testing/cachito-pip-with-deps) as a submodule. <br/>
<br/>*`git-submodule-pip/.gitmodules`:
```
[submodule "cachito-pip-with-deps"]
	path = cachito-pip-with-deps
	url = https://github.com/cachito-testing/cachito-pip-with-deps.git
```
