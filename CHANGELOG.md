# Change Log

## [0.9.0](https://github.com/nodegit/nodegit/releases/tag/v0.9.0) (2016-01-21)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.8.0...0.9.0)

- Thread safe fix to stop crashing on releasing mutexes [PR #876](https://github.com/nodegit/nodegit/pull/876)
- `Submodule#setIgnore`, `Submodule#setUpdate`, and `Submodule#setUrl` are now all async. `Submodule#status` and `Submodule#location` are now available [PR #867](https://github.com/nodegit/nodegit/pull/867) and [PR #870](https://github.com/nodegit/nodegit/pull/870)
- `Remote#defaultBranch` is now available [PR #872](https://github.com/nodegit/nodegit/pull/872)
- `Repository#mergeBranches` now takes in a `MergeOptions` parameter [PR #873](https://github.com/nodegit/nodegit/pull/873)
- Remove a NodeGit specific hack to make `Index#addAll` faster since that is fixed in libgit2 [PR #875](https://github.com/nodegit/nodegit/pull/875)

## [0.8.0](https://github.com/nodegit/nodegit/releases/tag/v0.8.0) (2016-01-15)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.7.0...0.8.0)

- Thread safe locking has been added and currently is defaulted to off. Use `NodeGit.enableThreadSafety()` to turn on
- NodeGit no longer requires a specific Promise object from the `nodegit-promise` library to be passed in. You can now use whatever you want!
- `Repository#stageFilemode` now can accept an array of strings for files to update
- `Submodule#addToIndex`, `Submodule#addFinalize`, `Submodule#init`, `Submodule#open`, `Submodule#sync`, and `Submodule#update` are now all async methodss

## [0.7.0](https://github.com/nodegit/nodegit/releases/tag/v0.7.0) (2016-01-08)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.6.3...0.7.0)

- Bumped openssl to 1.0.2e to fix issues with prebuilts on linux platforms
- Fixed a bug with GIT_ITER_OVER breaking rebase and other iterative methods
- Make GraphDescendentOf asynchronous
- Fixed line length of utf8 stringss

## [0.6.3](https://github.com/nodegit/nodegit/releases/tag/v0.6.3) (2015-12-16)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.6.2...0.6.3)

 - Fixed a bug where manually building for vanilla node would fail without explicitly
   setting the target

## [0.6.2](https://github.com/nodegit/nodegit/releases/tag/v0.6.2) (2015-12-16)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.6.1...0.6.2)

 - Fixed a bug where manually building on windows would fail (if unable to download a prebuilt binary)

## [0.6.1](https://github.com/nodegit/nodegit/releases/tag/v0.6.1) (2015-12-14)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.6.0...0.6.1)

 - Fixed Treebuilder.create to have an optional source
 - Added Repository.getSubmoduleNames
 - Added Submodule.Foreach

## [0.6.0](https://github.com/nodegit/nodegit/releases/tag/v0.6.0) (2015-12-08)

 - Added file mode staging
 - Added a fast rev walk to do the rev walk in C++ and bubble the result up to JS
 - Updated to latest libgit2
 - Updated to latest openssl
 - Updated to latest nodegit-promise
 - Removed c++11 dependency
 - Fixed weirdness in lifecycle scripts
 - Added downloading prebuilt binaries for electron

## [0.4.1](https://github.com/nodegit/nodegit/tree/0.4.1) (2015-06-02)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.4.0...0.4.1)

**Closed issues:**

- Error: Module did not self-register [\#593](https://github.com/nodegit/nodegit/issues/593)

- A guide on how to create a new branch, switch to it and delete it. [\#588](https://github.com/nodegit/nodegit/issues/588)

- A way to get "gone" branches [\#583](https://github.com/nodegit/nodegit/issues/583)

- Missing documentation pages for BranchIterator and NodeIterator [\#581](https://github.com/nodegit/nodegit/issues/581)

- ELIFECYCLE error on `npm rebuild` [\#578](https://github.com/nodegit/nodegit/issues/578)

- npm rebuild fails \(lifecycleScripts/clean should not delete lifecycleScripts!\) [\#576](https://github.com/nodegit/nodegit/issues/576)

- Unable to compile and install v0.4.0 on Windows [\#575](https://github.com/nodegit/nodegit/issues/575)

- Doesn't work with Electron [\#574](https://github.com/nodegit/nodegit/issues/574)

- Doesn't work with io.js 2.x [\#573](https://github.com/nodegit/nodegit/issues/573)

- Getting an exception during a fetchAll in defaultSignature in repository.js [\#572](https://github.com/nodegit/nodegit/issues/572)

- tree\_entry path function not working when calling getEntry with a path including subdir [\#570](https://github.com/nodegit/nodegit/issues/570)

- Build is broken on windows [\#565](https://github.com/nodegit/nodegit/issues/565)

- Cloning git sub modules using "nodegit" npm module [\#560](https://github.com/nodegit/nodegit/issues/560)

- How to get remote latest commit? [\#559](https://github.com/nodegit/nodegit/issues/559)

- npm install fails for nw.js [\#558](https://github.com/nodegit/nodegit/issues/558)

- nodegit and nw.js [\#557](https://github.com/nodegit/nodegit/issues/557)

**Merged pull requests:**

- Cherrypick tests [\#595](https://github.com/nodegit/nodegit/pull/595) ([jdgarcia](https://github.com/jdgarcia))

- Fix for issue \#591.  TreeEntry.path\(\) throws when TreeEntry came from Tree.entries\(\) [\#592](https://github.com/nodegit/nodegit/pull/592) ([tomruggs](https://github.com/tomruggs))

- Standard merge [\#589](https://github.com/nodegit/nodegit/pull/589) ([jdgarcia](https://github.com/jdgarcia))

- Add `git\_index\_conflict\_get` and test [\#586](https://github.com/nodegit/nodegit/pull/586) ([johnhaley81](https://github.com/johnhaley81))

- Bump nan [\#584](https://github.com/nodegit/nodegit/pull/584) ([johnhaley81](https://github.com/johnhaley81))

- Fix CI false positives [\#582](https://github.com/nodegit/nodegit/pull/582) ([johnhaley81](https://github.com/johnhaley81))

- Added NodeGit.Checkout.index [\#579](https://github.com/nodegit/nodegit/pull/579) ([jdgarcia](https://github.com/jdgarcia))

- Check for existence to avoid throwing an error when there is no default signature [\#577](https://github.com/nodegit/nodegit/pull/577) ([tomruggs](https://github.com/tomruggs))

- Fix path function in tree\_entry \(fix for issue \#570\) [\#571](https://github.com/nodegit/nodegit/pull/571) ([jfremy](https://github.com/jfremy))

- Fix Rebase issues [\#568](https://github.com/nodegit/nodegit/pull/568) ([jdgarcia](https://github.com/jdgarcia))

- Fix build issues with 0.4.0 [\#566](https://github.com/nodegit/nodegit/pull/566) ([maxkorp](https://github.com/maxkorp))

- stop cleaning on post-install [\#562](https://github.com/nodegit/nodegit/pull/562) ([maxkorp](https://github.com/maxkorp))

## [v0.4.0](https://github.com/nodegit/nodegit/tree/v0.4.0) (2015-05-07)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.3.3...v0.4.0)

**Closed issues:**

- Error installing nodegit as dependency of an atom-shell app [\#556](https://github.com/nodegit/nodegit/issues/556)

- New version of nan is breaking compile [\#554](https://github.com/nodegit/nodegit/issues/554)

- Install error from openssl [\#551](https://github.com/nodegit/nodegit/issues/551)

- How to get Tag instance by tag\_name? [\#543](https://github.com/nodegit/nodegit/issues/543)

- ELIFECYCLE Error on install [\#540](https://github.com/nodegit/nodegit/issues/540)

- Remote.delete returns -3 [\#539](https://github.com/nodegit/nodegit/issues/539)

- Repository.init should accept boolean value for is\_bare [\#538](https://github.com/nodegit/nodegit/issues/538)

- getStatus hangs [\#537](https://github.com/nodegit/nodegit/issues/537)

- Unable to compile or install with npm install nodegit [\#536](https://github.com/nodegit/nodegit/issues/536)

- `options` not reusable, nodegit destroys it [\#533](https://github.com/nodegit/nodegit/issues/533)

- 'Error: 'directory' exists and is not an empty directory' \(but it doesn't exist\) [\#530](https://github.com/nodegit/nodegit/issues/530)

- hey !:-\) problem with Branch.iteratorNew  \(support\) [\#528](https://github.com/nodegit/nodegit/issues/528)

- hey !:-\) problem with Branch.iteratorNew [\#527](https://github.com/nodegit/nodegit/issues/527)

- hey !:-\) problem with Branch.iteratorNew [\#526](https://github.com/nodegit/nodegit/issues/526)

- hey !:-\) problem with Branch.iteratorNew [\#525](https://github.com/nodegit/nodegit/issues/525)

- Error: Reference 'refs/remotes/user/foo/HEAD' not found [\#523](https://github.com/nodegit/nodegit/issues/523)

- Path issues windows [\#522](https://github.com/nodegit/nodegit/issues/522)

- Issues on scientific linux 6.6 [\#521](https://github.com/nodegit/nodegit/issues/521)

- It's looking for node-typ under `/Users/johnh/.node-gyp` [\#518](https://github.com/nodegit/nodegit/issues/518)

- Not working with iojs [\#516](https://github.com/nodegit/nodegit/issues/516)

- Cred.sshKeyNew not working: Too many redirects or authentication replays [\#511](https://github.com/nodegit/nodegit/issues/511)

- Open a Repo from a subfolder [\#509](https://github.com/nodegit/nodegit/issues/509)

- Create git-like CLI [\#508](https://github.com/nodegit/nodegit/issues/508)

- Cannot create an instance of Packbuilder [\#507](https://github.com/nodegit/nodegit/issues/507)

- Cannot find module '../build/Debug/nodegit' [\#506](https://github.com/nodegit/nodegit/issues/506)

- Bug with oid implicit cast inside C++ [\#501](https://github.com/nodegit/nodegit/issues/501)

- Failed to `require` on Ubuntu 12.04LTS [\#493](https://github.com/nodegit/nodegit/issues/493)

- Enable `git\_config`  [\#449](https://github.com/nodegit/nodegit/issues/449)

- Pull example doesn't fully update the index [\#389](https://github.com/nodegit/nodegit/issues/389)

**Merged pull requests:**

- There is an incompatibility with NaN 1.8.x, keeping 1.7.x for now. [\#552](https://github.com/nodegit/nodegit/pull/552) ([wiggzz](https://github.com/wiggzz))

- A wrapper for git\_diff\_blob\_to\_buffer [\#550](https://github.com/nodegit/nodegit/pull/550) ([bleathem](https://github.com/bleathem))

- Update to 0.4.0 [\#548](https://github.com/nodegit/nodegit/pull/548) ([tbranyen](https://github.com/tbranyen))

- Removed the superflous "line" argument [\#547](https://github.com/nodegit/nodegit/pull/547) ([bleathem](https://github.com/bleathem))

- This fixes polling sync promises in callbacks. [\#546](https://github.com/nodegit/nodegit/pull/546) ([johnhaley81](https://github.com/johnhaley81))

- Add get/set config string methods and tests [\#545](https://github.com/nodegit/nodegit/pull/545) ([johnhaley81](https://github.com/johnhaley81))

- Make `Remote.delete` async and return error messages correctly [\#544](https://github.com/nodegit/nodegit/pull/544) ([johnhaley81](https://github.com/johnhaley81))

- Bump "nodegit-promise" version [\#542](https://github.com/nodegit/nodegit/pull/542) ([johnhaley81](https://github.com/johnhaley81))

- Introduced a new ConvenientLine class to wrap the lines returned from ConvenientHunk. [\#541](https://github.com/nodegit/nodegit/pull/541) ([bleathem](https://github.com/bleathem))

- Fix some things missed by the generating scripts [\#535](https://github.com/nodegit/nodegit/pull/535) ([johnhaley81](https://github.com/johnhaley81))

- Attempt remove the delete keyword [\#534](https://github.com/nodegit/nodegit/pull/534) ([tbranyen](https://github.com/tbranyen))

- Fix freeing a `GitOid` that was passed as a string [\#531](https://github.com/nodegit/nodegit/pull/531) ([johnhaley81](https://github.com/johnhaley81))

- fix typo: "byes" [\#529](https://github.com/nodegit/nodegit/pull/529) ([rutsky](https://github.com/rutsky))

- Add convenience methods to status file [\#524](https://github.com/nodegit/nodegit/pull/524) ([maxkorp](https://github.com/maxkorp))

- Lots of complaints of missing build/Debug/nodegit [\#520](https://github.com/nodegit/nodegit/pull/520) ([tbranyen](https://github.com/tbranyen))

- Add `Graph.aheadBehind` and tests [\#517](https://github.com/nodegit/nodegit/pull/517) ([johnhaley81](https://github.com/johnhaley81))

- Update to use libgit2 v0.22.2 [\#515](https://github.com/nodegit/nodegit/pull/515) ([johnhaley81](https://github.com/johnhaley81))

- Add `Repository.prototype.fetchheadForeach` and tests [\#514](https://github.com/nodegit/nodegit/pull/514) ([johnhaley81](https://github.com/johnhaley81))

- Converted create methods to be synchronous [\#513](https://github.com/nodegit/nodegit/pull/513) ([tbranyen](https://github.com/tbranyen))

- Fix atom-shell build on windows [\#512](https://github.com/nodegit/nodegit/pull/512) ([johnhaley81](https://github.com/johnhaley81))

- Update Checkout and Merge [\#505](https://github.com/nodegit/nodegit/pull/505) ([orderedlist](https://github.com/orderedlist))

- Add note tests [\#504](https://github.com/nodegit/nodegit/pull/504) ([tbranyen](https://github.com/tbranyen))

- Revert "Guide navigation is currently confusing" [\#503](https://github.com/nodegit/nodegit/pull/503) ([thgaskell](https://github.com/thgaskell))

- Improve coverage [\#502](https://github.com/nodegit/nodegit/pull/502) ([tbranyen](https://github.com/tbranyen))

- Adds in CPP code coverage and joined JS [\#499](https://github.com/nodegit/nodegit/pull/499) ([tbranyen](https://github.com/tbranyen))

- Add twitter username to README.md [\#498](https://github.com/nodegit/nodegit/pull/498) ([johnhaley81](https://github.com/johnhaley81))

- Fix symbolic reference handling in getReferences [\#496](https://github.com/nodegit/nodegit/pull/496) ([billt2006](https://github.com/billt2006))

- Enable `git\_stash\_foreach` [\#495](https://github.com/nodegit/nodegit/pull/495) ([johnhaley81](https://github.com/johnhaley81))

- Guide navigation is currently confusing [\#494](https://github.com/nodegit/nodegit/pull/494) ([tbranyen](https://github.com/tbranyen))

- Fix gitter badge for npm [\#492](https://github.com/nodegit/nodegit/pull/492) ([billt2006](https://github.com/billt2006))

- Add automatically generated change log file. [\#465](https://github.com/nodegit/nodegit/pull/465) ([skywinder](https://github.com/skywinder))

## [v0.3.3](https://github.com/nodegit/nodegit/tree/v0.3.3) (2015-03-16)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.3.2...v0.3.3)

**Merged pull requests:**

- Download all dev dependencies before build [\#491](https://github.com/nodegit/nodegit/pull/491) ([johnhaley81](https://github.com/johnhaley81))

## [v0.3.2](https://github.com/nodegit/nodegit/tree/v0.3.2) (2015-03-16)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.3.1...v0.3.2)

**Closed issues:**

- Amazon S3 CDN link is broken [\#482](https://github.com/nodegit/nodegit/issues/482)

**Merged pull requests:**

- Confirm builder exists before building [\#490](https://github.com/nodegit/nodegit/pull/490) ([johnhaley81](https://github.com/johnhaley81))

## [v0.3.1](https://github.com/nodegit/nodegit/tree/v0.3.1) (2015-03-14)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.3.0...v0.3.1)

**Merged pull requests:**

- Revert node-pre-gyp to install not build [\#486](https://github.com/nodegit/nodegit/pull/486) ([tbranyen](https://github.com/tbranyen))

## [v0.3.0](https://github.com/nodegit/nodegit/tree/v0.3.0) (2015-03-13)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.2.7...v0.3.0)

**Closed issues:**

- Push [\#463](https://github.com/nodegit/nodegit/issues/463)

- Suppress astyle errors [\#459](https://github.com/nodegit/nodegit/issues/459)

- io.js support [\#447](https://github.com/nodegit/nodegit/issues/447)

- Meteor: icon fonts not working \(Resource interpreted as Font but transferred with MIME type text/html\) [\#443](https://github.com/nodegit/nodegit/issues/443)

- AnnotatedCommit.x listing as Annotated.commitX [\#437](https://github.com/nodegit/nodegit/issues/437)

- fetchAll\(\) fails unless a default signature is available [\#431](https://github.com/nodegit/nodegit/issues/431)

- Question: Is there a certificateCheck option available for pushing to a remote repository? [\#420](https://github.com/nodegit/nodegit/issues/420)

- Repository.open returns empty object [\#412](https://github.com/nodegit/nodegit/issues/412)

- Missing documentation for Tree.walk\(\) [\#411](https://github.com/nodegit/nodegit/issues/411)

- comparing from 0.1.4 to 0.2.0 [\#410](https://github.com/nodegit/nodegit/issues/410)

- Potential example issue in add-and-commit.js L45-48 [\#409](https://github.com/nodegit/nodegit/issues/409)

- failed to install on ubuntu 14.04 [\#408](https://github.com/nodegit/nodegit/issues/408)

- Return promises instead of nesting them [\#407](https://github.com/nodegit/nodegit/issues/407)

- segfault when cloning from private BitBucket repo [\#406](https://github.com/nodegit/nodegit/issues/406)

- Subtrees + custom error handling [\#400](https://github.com/nodegit/nodegit/issues/400)

- How to use nodegit in atom shell ..... [\#393](https://github.com/nodegit/nodegit/issues/393)

- Cannot create a new branch [\#391](https://github.com/nodegit/nodegit/issues/391)

- Remove fixappveyor from clone tests [\#385](https://github.com/nodegit/nodegit/issues/385)

- Commit isn't working [\#381](https://github.com/nodegit/nodegit/issues/381)

- Rename combyne folder to templates [\#378](https://github.com/nodegit/nodegit/issues/378)

- Cloning SSH repos seem to fail  [\#372](https://github.com/nodegit/nodegit/issues/372)

- Commit.getDiff is backwards? [\#368](https://github.com/nodegit/nodegit/issues/368)

- List all files in repo \(git ls-tree\) [\#365](https://github.com/nodegit/nodegit/issues/365)

- Checking out a branch [\#361](https://github.com/nodegit/nodegit/issues/361)

- nodegit no longer builds in nwjs [\#360](https://github.com/nodegit/nodegit/issues/360)

- Module install/build fails on Heroku  [\#332](https://github.com/nodegit/nodegit/issues/332)

- 2 Step Authentication [\#323](https://github.com/nodegit/nodegit/issues/323)

**Merged pull requests:**

- Rename `Annotated` to `AnnotatedCommit` [\#485](https://github.com/nodegit/nodegit/pull/485) ([johnhaley81](https://github.com/johnhaley81))

- Bump version to 0.3.0 [\#484](https://github.com/nodegit/nodegit/pull/484) ([johnhaley81](https://github.com/johnhaley81))

- Remove unneeded connect call from push example [\#483](https://github.com/nodegit/nodegit/pull/483) ([johnhaley81](https://github.com/johnhaley81))

- Update push example [\#481](https://github.com/nodegit/nodegit/pull/481) ([billt2006](https://github.com/billt2006))

- Fix trailing space in atom-shell windows install [\#480](https://github.com/nodegit/nodegit/pull/480) ([johnhaley81](https://github.com/johnhaley81))

- Fix atom-shell install on windows [\#479](https://github.com/nodegit/nodegit/pull/479) ([johnhaley81](https://github.com/johnhaley81))

- Updated API documentation link to work with NPM's markdown renderer.  [\#477](https://github.com/nodegit/nodegit/pull/477) ([hughfdjackson](https://github.com/hughfdjackson))

- Add option to `fetch` to prune the remote afterwards [\#476](https://github.com/nodegit/nodegit/pull/476) ([johnhaley81](https://github.com/johnhaley81))

- Make index.addAll use status to increase performance [\#475](https://github.com/nodegit/nodegit/pull/475) ([maxkorp](https://github.com/maxkorp))

- Add defaults to `Remote.prototype.push` [\#474](https://github.com/nodegit/nodegit/pull/474) ([johnhaley81](https://github.com/johnhaley81))

- Fix `createCommitOnHead` [\#473](https://github.com/nodegit/nodegit/pull/473) ([johnhaley81](https://github.com/johnhaley81))

- Move guides around to remove subindexes [\#472](https://github.com/nodegit/nodegit/pull/472) ([orderedlist](https://github.com/orderedlist))

- Put `Remote.Push` on the remote prototype [\#470](https://github.com/nodegit/nodegit/pull/470) ([johnhaley81](https://github.com/johnhaley81))

- Change Repository.prototype.setHead to be asynchronous [\#469](https://github.com/nodegit/nodegit/pull/469) ([jrbalsano](https://github.com/jrbalsano))

- Test in Node 0.12 and io.js [\#468](https://github.com/nodegit/nodegit/pull/468) ([tbranyen](https://github.com/tbranyen))

- Add checkoutBranch convenience method [\#466](https://github.com/nodegit/nodegit/pull/466) ([johnhaley81](https://github.com/johnhaley81))

- Don't assign enums to \_\_proto\_\_ [\#464](https://github.com/nodegit/nodegit/pull/464) ([orderedlist](https://github.com/orderedlist))

- Fix push example [\#462](https://github.com/nodegit/nodegit/pull/462) ([johnhaley81](https://github.com/johnhaley81))

- Adds support for strarray in structs [\#461](https://github.com/nodegit/nodegit/pull/461) ([orderedlist](https://github.com/orderedlist))

- supress astyle warnings [\#460](https://github.com/nodegit/nodegit/pull/460) ([maxkorp](https://github.com/maxkorp))

- Template proto functions [\#458](https://github.com/nodegit/nodegit/pull/458) ([maxkorp](https://github.com/maxkorp))

- Remote push [\#457](https://github.com/nodegit/nodegit/pull/457) ([mattyclarkson](https://github.com/mattyclarkson))

- Include missing lib files in nodegit.js template [\#455](https://github.com/nodegit/nodegit/pull/455) ([orderedlist](https://github.com/orderedlist))

- StrArray memory fix [\#454](https://github.com/nodegit/nodegit/pull/454) ([mattyclarkson](https://github.com/mattyclarkson))

- Better cloning with NodeGit [\#453](https://github.com/nodegit/nodegit/pull/453) ([tbranyen](https://github.com/tbranyen))

- Add Diff.prototype.findSimilar [\#452](https://github.com/nodegit/nodegit/pull/452) ([orderedlist](https://github.com/orderedlist))

- Str array converter fix [\#451](https://github.com/nodegit/nodegit/pull/451) ([mattyclarkson](https://github.com/mattyclarkson))

- Default signature always returns valid signature [\#450](https://github.com/nodegit/nodegit/pull/450) ([johnhaley81](https://github.com/johnhaley81))

- Status.byIndex and StatusEntry [\#448](https://github.com/nodegit/nodegit/pull/448) ([orderedlist](https://github.com/orderedlist))

- Upgrade to nan 1.7.0 [\#446](https://github.com/nodegit/nodegit/pull/446) ([orderedlist](https://github.com/orderedlist))

- Added in an HTTP url for test [\#445](https://github.com/nodegit/nodegit/pull/445) ([tbranyen](https://github.com/tbranyen))

- Add examples [\#442](https://github.com/nodegit/nodegit/pull/442) ([johnhaley81](https://github.com/johnhaley81))

- hide callback payloads from javascript [\#441](https://github.com/nodegit/nodegit/pull/441) ([maxkorp](https://github.com/maxkorp))

- Fix transfer callback stats [\#440](https://github.com/nodegit/nodegit/pull/440) ([johnhaley81](https://github.com/johnhaley81))

- Automatically free repositories post clone [\#434](https://github.com/nodegit/nodegit/pull/434) ([tbranyen](https://github.com/tbranyen))

- Skip transfer progress test until it's fixed [\#433](https://github.com/nodegit/nodegit/pull/433) ([johnhaley81](https://github.com/johnhaley81))

- Change environment to default for upgraded service [\#428](https://github.com/nodegit/nodegit/pull/428) ([maxkorp](https://github.com/maxkorp))

- Make the `git\_remote\_push` function async [\#427](https://github.com/nodegit/nodegit/pull/427) ([johnhaley81](https://github.com/johnhaley81))

- Attempt to fix Windows file locking bug [\#425](https://github.com/nodegit/nodegit/pull/425) ([tbranyen](https://github.com/tbranyen))

- Fix seg faults [\#424](https://github.com/nodegit/nodegit/pull/424) ([johnhaley81](https://github.com/johnhaley81))

- Clean up the persisting of props [\#423](https://github.com/nodegit/nodegit/pull/423) ([johnhaley81](https://github.com/johnhaley81))

- Fix indexEntry construction and blobFromBuffer [\#422](https://github.com/nodegit/nodegit/pull/422) ([orderedlist](https://github.com/orderedlist))

- Allow for saving of props to an object [\#421](https://github.com/nodegit/nodegit/pull/421) ([johnhaley81](https://github.com/johnhaley81))

- Fixes segfault issue recorded in \#406 [\#419](https://github.com/nodegit/nodegit/pull/419) ([tbranyen](https://github.com/tbranyen))

- Update jsdoc and ignore some methods [\#418](https://github.com/nodegit/nodegit/pull/418) ([orderedlist](https://github.com/orderedlist))

- Converting Examples to Guides [\#417](https://github.com/nodegit/nodegit/pull/417) ([tbranyen](https://github.com/tbranyen))

- Fix callbacks with just return value and single payload [\#416](https://github.com/nodegit/nodegit/pull/416) ([johnhaley81](https://github.com/johnhaley81))

- Add `git\_reset` and `git\_reset\_default` [\#415](https://github.com/nodegit/nodegit/pull/415) ([johnhaley81](https://github.com/johnhaley81))

- Enable `git\_index\_remove\_all` and `git\_index\_update\_all` [\#414](https://github.com/nodegit/nodegit/pull/414) ([johnhaley81](https://github.com/johnhaley81))

- Added code for `git\_strarray` and enabled `git\_index\_add\_all` [\#413](https://github.com/nodegit/nodegit/pull/413) ([johnhaley81](https://github.com/johnhaley81))

- Tree Entry getBlob\(\) should also support the callback pattern. [\#405](https://github.com/nodegit/nodegit/pull/405) ([jeffwilcox](https://github.com/jeffwilcox))

- Adds in git\_checkout\_tree [\#402](https://github.com/nodegit/nodegit/pull/402) ([tbranyen](https://github.com/tbranyen))

- Made changes to the README [\#399](https://github.com/nodegit/nodegit/pull/399) ([tbranyen](https://github.com/tbranyen))

- Expose gc so all tests run in CI [\#398](https://github.com/nodegit/nodegit/pull/398) ([tbranyen](https://github.com/tbranyen))

- One more dependency update [\#397](https://github.com/nodegit/nodegit/pull/397) ([maxkorp](https://github.com/maxkorp))

- Update moar dependencies. [\#396](https://github.com/nodegit/nodegit/pull/396) ([maxkorp](https://github.com/maxkorp))

- Updated most dependencies to latest versions [\#394](https://github.com/nodegit/nodegit/pull/394) ([johnhaley81](https://github.com/johnhaley81))

- Index diffing [\#392](https://github.com/nodegit/nodegit/pull/392) ([orderedlist](https://github.com/orderedlist))

- Update to libgit2 v0.22.1 [\#390](https://github.com/nodegit/nodegit/pull/390) ([johnhaley81](https://github.com/johnhaley81))

- Fix test issues [\#388](https://github.com/nodegit/nodegit/pull/388) ([maxkorp](https://github.com/maxkorp))

- Fix building when a space is in the path [\#387](https://github.com/nodegit/nodegit/pull/387) ([billt2006](https://github.com/billt2006))

- General maintenance [\#386](https://github.com/nodegit/nodegit/pull/386) ([maxkorp](https://github.com/maxkorp))

- Add 2 convenience methods to revwalk [\#384](https://github.com/nodegit/nodegit/pull/384) ([maxkorp](https://github.com/maxkorp))

- Make all cred generators sync. [\#377](https://github.com/nodegit/nodegit/pull/377) ([maxkorp](https://github.com/maxkorp))

- Status and StatusList [\#374](https://github.com/nodegit/nodegit/pull/374) ([orderedlist](https://github.com/orderedlist))

- Fix the package scripts [\#373](https://github.com/nodegit/nodegit/pull/373) ([maxkorp](https://github.com/maxkorp))

- Removes Node 0.11 testing completely [\#371](https://github.com/nodegit/nodegit/pull/371) ([tbranyen](https://github.com/tbranyen))

- Allow null trees on Diff.treeToTree [\#370](https://github.com/nodegit/nodegit/pull/370) ([orderedlist](https://github.com/orderedlist))

- Atom shell support [\#369](https://github.com/nodegit/nodegit/pull/369) ([maxkorp](https://github.com/maxkorp))

- `Checkout.head` initializes options if none are passed [\#367](https://github.com/nodegit/nodegit/pull/367) ([johnhaley81](https://github.com/johnhaley81))

- INCLUDE\_UNTRACKED option not working for diffs [\#366](https://github.com/nodegit/nodegit/pull/366) ([kmctown](https://github.com/kmctown))

- Updated fs-extra to 0.15.0 [\#363](https://github.com/nodegit/nodegit/pull/363) ([johnhaley81](https://github.com/johnhaley81))

- Make remote\#download async [\#326](https://github.com/nodegit/nodegit/pull/326) ([tbranyen](https://github.com/tbranyen))

- Enable transfer progress [\#325](https://github.com/nodegit/nodegit/pull/325) ([tbranyen](https://github.com/tbranyen))

## [v0.2.7](https://github.com/nodegit/nodegit/tree/v0.2.7) (2015-01-21)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.2.6...v0.2.7)

## [v0.2.6](https://github.com/nodegit/nodegit/tree/v0.2.6) (2015-01-20)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.2.5...v0.2.6)

**Merged pull requests:**

- \[WIP\] Added in some diff functions from libgit2 [\#348](https://github.com/nodegit/nodegit/pull/348) ([johnhaley81](https://github.com/johnhaley81))

## [v0.2.5](https://github.com/nodegit/nodegit/tree/v0.2.5) (2015-01-20)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.2.4...v0.2.5)

**Closed issues:**

- Lookup a non existent commit crashes the process. [\#353](https://github.com/nodegit/nodegit/issues/353)

- Why node-git uses 90% rotated hexagon? [\#344](https://github.com/nodegit/nodegit/issues/344)

- Needed pull example or help with code [\#341](https://github.com/nodegit/nodegit/issues/341)

- Can't require nodegit without building it explicitly [\#340](https://github.com/nodegit/nodegit/issues/340)

- Tracking down bugs [\#331](https://github.com/nodegit/nodegit/issues/331)

- Document possible values of CloneOptions [\#330](https://github.com/nodegit/nodegit/issues/330)

- Require generating error [\#329](https://github.com/nodegit/nodegit/issues/329)

- Failed getting Banner [\#328](https://github.com/nodegit/nodegit/issues/328)

- Documentation broken [\#327](https://github.com/nodegit/nodegit/issues/327)

- Fetch doesn't seem to work with https urls. [\#322](https://github.com/nodegit/nodegit/issues/322)

**Merged pull requests:**

- Refactor installation and publication [\#359](https://github.com/nodegit/nodegit/pull/359) ([maxkorp](https://github.com/maxkorp))

- Lint examples [\#358](https://github.com/nodegit/nodegit/pull/358) ([maxkorp](https://github.com/maxkorp))

- Commit.getParents working with merge commits [\#357](https://github.com/nodegit/nodegit/pull/357) ([bjornarg](https://github.com/bjornarg))

- Fixed a typo in the debug build instruction. [\#356](https://github.com/nodegit/nodegit/pull/356) ([mcollina](https://github.com/mcollina))

- \[WIP\] Attempt at fixing appveyor [\#352](https://github.com/nodegit/nodegit/pull/352) ([johnhaley81](https://github.com/johnhaley81))

- Updated to nan 1.5.0 and fixed build errors [\#351](https://github.com/nodegit/nodegit/pull/351) ([johnhaley81](https://github.com/johnhaley81))

- Added debug build instructions. [\#349](https://github.com/nodegit/nodegit/pull/349) ([mcollina](https://github.com/mcollina))

- Added checkout head method and tests [\#347](https://github.com/nodegit/nodegit/pull/347) ([johnhaley81](https://github.com/johnhaley81))

- bump devDependencies [\#346](https://github.com/nodegit/nodegit/pull/346) ([PeterDaveHello](https://github.com/PeterDaveHello))

- Update dependency node-pre-gyp to ~0.6 [\#345](https://github.com/nodegit/nodegit/pull/345) ([PeterDaveHello](https://github.com/PeterDaveHello))

- Update dependency fs-extra to ~0.14.0 [\#343](https://github.com/nodegit/nodegit/pull/343) ([PeterDaveHello](https://github.com/PeterDaveHello))

- Add Dependency badge in readme [\#342](https://github.com/nodegit/nodegit/pull/342) ([PeterDaveHello](https://github.com/PeterDaveHello))

- Fixed promise chain on install [\#339](https://github.com/nodegit/nodegit/pull/339) ([johnhaley81](https://github.com/johnhaley81))

- Do not double free during callbacks. [\#338](https://github.com/nodegit/nodegit/pull/338) ([mcollina](https://github.com/mcollina))

- Use svg instead of png to get better image quality [\#337](https://github.com/nodegit/nodegit/pull/337) ([PeterDaveHello](https://github.com/PeterDaveHello))

- Update to libgit 0.21.4 [\#336](https://github.com/nodegit/nodegit/pull/336) ([johnhaley81](https://github.com/johnhaley81))

- Fix issue 333 [\#334](https://github.com/nodegit/nodegit/pull/334) ([johnhaley81](https://github.com/johnhaley81))

- Update appveyor.yml to remove project id [\#324](https://github.com/nodegit/nodegit/pull/324) ([vladikoff](https://github.com/vladikoff))

- moving some deps to devdeps [\#320](https://github.com/nodegit/nodegit/pull/320) ([maxkorp](https://github.com/maxkorp))

## [v0.2.4](https://github.com/nodegit/nodegit/tree/v0.2.4) (2014-12-05)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.2.3...v0.2.4)

**Closed issues:**

- Fetch does not really fetch [\#314](https://github.com/nodegit/nodegit/issues/314)

- Generate Missing Tests - Unable [\#313](https://github.com/nodegit/nodegit/issues/313)

- Unable to get reference for HEAD [\#311](https://github.com/nodegit/nodegit/issues/311)

- nodegit.Signature.now broken [\#306](https://github.com/nodegit/nodegit/issues/306)

- current branch [\#305](https://github.com/nodegit/nodegit/issues/305)

- Module fails to load [\#299](https://github.com/nodegit/nodegit/issues/299)

- How to list all tags? [\#298](https://github.com/nodegit/nodegit/issues/298)

- Building for ARM [\#292](https://github.com/nodegit/nodegit/issues/292)

- Next release checklist [\#256](https://github.com/nodegit/nodegit/issues/256)

**Merged pull requests:**

- Fixed fetch to be async and use callbacks [\#319](https://github.com/nodegit/nodegit/pull/319) ([johnhaley81](https://github.com/johnhaley81))

- Make contributing.md generic and add testing.md [\#318](https://github.com/nodegit/nodegit/pull/318) ([maxkorp](https://github.com/maxkorp))

- Fix repo init ext [\#317](https://github.com/nodegit/nodegit/pull/317) ([maxkorp](https://github.com/maxkorp))

- Fix 313 generate scripts [\#315](https://github.com/nodegit/nodegit/pull/315) ([xinUmbralis](https://github.com/xinUmbralis))

- Fix \#311 [\#312](https://github.com/nodegit/nodegit/pull/312) ([johnhaley81](https://github.com/johnhaley81))

- Fix publishing [\#310](https://github.com/nodegit/nodegit/pull/310) ([maxkorp](https://github.com/maxkorp))

- detect node-webkit and build with nw-gyp [\#309](https://github.com/nodegit/nodegit/pull/309) ([maxkorp](https://github.com/maxkorp))

- fix signature.now and add signature tests [\#308](https://github.com/nodegit/nodegit/pull/308) ([maxkorp](https://github.com/maxkorp))

- move nodegit.js to a template to remove idefs dependency [\#303](https://github.com/nodegit/nodegit/pull/303) ([maxkorp](https://github.com/maxkorp))

- Fixed tag list and added a test for it [\#300](https://github.com/nodegit/nodegit/pull/300) ([johnhaley81](https://github.com/johnhaley81))

- Convenience methods [\#297](https://github.com/nodegit/nodegit/pull/297) ([johnhaley81](https://github.com/johnhaley81))

- Clean up the contents of the generate folder [\#296](https://github.com/nodegit/nodegit/pull/296) ([maxkorp](https://github.com/maxkorp))

- Styling  [\#295](https://github.com/nodegit/nodegit/pull/295) ([maxkorp](https://github.com/maxkorp))

## [v0.2.3](https://github.com/nodegit/nodegit/tree/v0.2.3) (2014-11-25)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.2.2...v0.2.3)

## [v0.2.2](https://github.com/nodegit/nodegit/tree/v0.2.2) (2014-11-25)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.2.1...v0.2.2)

**Merged pull requests:**

- Moved some dependencies around to help the generate not fail [\#294](https://github.com/nodegit/nodegit/pull/294) ([johnhaley81](https://github.com/johnhaley81))

## [v0.2.1](https://github.com/nodegit/nodegit/tree/v0.2.1) (2014-11-25)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.2.0...v0.2.1)

**Merged pull requests:**

- Rewrite installer [\#293](https://github.com/nodegit/nodegit/pull/293) ([johnhaley81](https://github.com/johnhaley81))

## [v0.2.0](https://github.com/nodegit/nodegit/tree/v0.2.0) (2014-11-25)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.1.4...v0.2.0)

**Closed issues:**

- Find some way to automatically generate a list of missing tests. [\#272](https://github.com/nodegit/nodegit/issues/272)

- libgit2 creation methods have name collisions with internal V8 functions [\#271](https://github.com/nodegit/nodegit/issues/271)

- Enums are still being manually assigned in javascript [\#268](https://github.com/nodegit/nodegit/issues/268)

- We're using too many promise libraries [\#264](https://github.com/nodegit/nodegit/issues/264)

- unable to resolve symbolic references [\#262](https://github.com/nodegit/nodegit/issues/262)

- nodegit installation falls back when Python install dir contains spaces [\#261](https://github.com/nodegit/nodegit/issues/261)

- Probe features [\#245](https://github.com/nodegit/nodegit/issues/245)

- require\('path'\).Repo.open\(...\) returns {} [\#241](https://github.com/nodegit/nodegit/issues/241)

- RevWalk malloc error [\#239](https://github.com/nodegit/nodegit/issues/239)

- OS X tests in Travis-CI [\#237](https://github.com/nodegit/nodegit/issues/237)

- Fix RevWalk tests [\#236](https://github.com/nodegit/nodegit/issues/236)

- Simple clone fails. [\#231](https://github.com/nodegit/nodegit/issues/231)

- Create templates for remaining src and include files [\#230](https://github.com/nodegit/nodegit/issues/230)

- Error: SSL is not supported by this copy of libgit2. [\#228](https://github.com/nodegit/nodegit/issues/228)

- error while install nodegit latest version 0.1.4 [\#225](https://github.com/nodegit/nodegit/issues/225)

- error while install nodegit latest version 0.1.4 [\#224](https://github.com/nodegit/nodegit/issues/224)

- Did getReferences dissapear? [\#223](https://github.com/nodegit/nodegit/issues/223)

- Again for \#147 [\#218](https://github.com/nodegit/nodegit/issues/218)

- Update documentation on nodegit.org [\#217](https://github.com/nodegit/nodegit/issues/217)

- Stable = bump to 1.0 [\#215](https://github.com/nodegit/nodegit/issues/215)

- Example on nodegit.com homepage is invalid [\#211](https://github.com/nodegit/nodegit/issues/211)

- tree.diffWorkDir deprecated? [\#209](https://github.com/nodegit/nodegit/issues/209)

- Abort on getRemotes [\#201](https://github.com/nodegit/nodegit/issues/201)

- Generic Logging/Tracing mechanism [\#199](https://github.com/nodegit/nodegit/issues/199)

- Repo\#openIndex missing [\#197](https://github.com/nodegit/nodegit/issues/197)

- Documentation on http://www.nodegit.org/ out of date [\#196](https://github.com/nodegit/nodegit/issues/196)

- Remove extern "C" with 0.21 bump [\#193](https://github.com/nodegit/nodegit/issues/193)

- CloneOptions documentation lacking [\#192](https://github.com/nodegit/nodegit/issues/192)

- Webpage examples are not up to date [\#190](https://github.com/nodegit/nodegit/issues/190)

- Automatically generate structs from types array [\#187](https://github.com/nodegit/nodegit/issues/187)

- Error: connect ETIMEDOUT during install [\#179](https://github.com/nodegit/nodegit/issues/179)

- TODO [\#177](https://github.com/nodegit/nodegit/issues/177)

- Notes [\#176](https://github.com/nodegit/nodegit/issues/176)

- Integration improvements. [\#171](https://github.com/nodegit/nodegit/issues/171)

**Merged pull requests:**

- add history.md and update readme [\#291](https://github.com/nodegit/nodegit/pull/291) ([maxkorp](https://github.com/maxkorp))

- Added tests for commit [\#290](https://github.com/nodegit/nodegit/pull/290) ([nkt](https://github.com/nkt))

- Added editor config [\#289](https://github.com/nodegit/nodegit/pull/289) ([nkt](https://github.com/nkt))

- \[WIP\] Push example [\#288](https://github.com/nodegit/nodegit/pull/288) ([johnhaley81](https://github.com/johnhaley81))

- \[WIP\] Better installation flow [\#287](https://github.com/nodegit/nodegit/pull/287) ([tbranyen](https://github.com/tbranyen))

- Merge methods and tests and examples [\#286](https://github.com/nodegit/nodegit/pull/286) ([maxkorp](https://github.com/maxkorp))

- Add details-for-tree-entry [\#285](https://github.com/nodegit/nodegit/pull/285) ([johnhaley81](https://github.com/johnhaley81))

- Add repo init example [\#284](https://github.com/nodegit/nodegit/pull/284) ([maxkorp](https://github.com/maxkorp))

- update add-and-commit example to include new paths [\#283](https://github.com/nodegit/nodegit/pull/283) ([maxkorp](https://github.com/maxkorp))

- General cleanup [\#282](https://github.com/nodegit/nodegit/pull/282) ([maxkorp](https://github.com/maxkorp))

- Added osx for testing on Travis [\#281](https://github.com/nodegit/nodegit/pull/281) ([johnhaley81](https://github.com/johnhaley81))

- Added " around python path to help fix issues with spaces in path [\#280](https://github.com/nodegit/nodegit/pull/280) ([johnhaley81](https://github.com/johnhaley81))

- Tests for branch class [\#279](https://github.com/nodegit/nodegit/pull/279) ([johnhaley81](https://github.com/johnhaley81))

- Exposes the NodeGit Promise implementation [\#278](https://github.com/nodegit/nodegit/pull/278) ([tbranyen](https://github.com/tbranyen))

- \[WIP\] Update examples [\#276](https://github.com/nodegit/nodegit/pull/276) ([johnhaley81](https://github.com/johnhaley81))

- Added script to generate missing tests [\#274](https://github.com/nodegit/nodegit/pull/274) ([johnhaley81](https://github.com/johnhaley81))

- Rename new [\#273](https://github.com/nodegit/nodegit/pull/273) ([maxkorp](https://github.com/maxkorp))

- MSBUILD doesn't allow an array of size 0 [\#270](https://github.com/nodegit/nodegit/pull/270) ([johnhaley81](https://github.com/johnhaley81))

- \[WIP\] generate enum definitions [\#269](https://github.com/nodegit/nodegit/pull/269) ([maxkorp](https://github.com/maxkorp))

- add Refs.nameToId and test [\#267](https://github.com/nodegit/nodegit/pull/267) ([maxkorp](https://github.com/maxkorp))

- voidcheck string pointers and reenable attr test [\#266](https://github.com/nodegit/nodegit/pull/266) ([maxkorp](https://github.com/maxkorp))

- require --documentation flag to include text in idefs [\#265](https://github.com/nodegit/nodegit/pull/265) ([maxkorp](https://github.com/maxkorp))

- Added ability for callbacks to poll promises for fulfillment value [\#260](https://github.com/nodegit/nodegit/pull/260) ([johnhaley81](https://github.com/johnhaley81))

- Generate nodegit from libgit2 docs and refactor descriptor [\#259](https://github.com/nodegit/nodegit/pull/259) ([johnhaley81](https://github.com/johnhaley81))

- Fix revwalk tests [\#258](https://github.com/nodegit/nodegit/pull/258) ([maxkorp](https://github.com/maxkorp))

- Bump to latest libgit2 [\#257](https://github.com/nodegit/nodegit/pull/257) ([tbranyen](https://github.com/tbranyen))

- Use Start-Process to start pageant.exe [\#254](https://github.com/nodegit/nodegit/pull/254) ([FeodorFitsner](https://github.com/FeodorFitsner))

- Adds in a broken unit test for \#109 [\#252](https://github.com/nodegit/nodegit/pull/252) ([tbranyen](https://github.com/tbranyen))

- Added more git\_cred methods [\#251](https://github.com/nodegit/nodegit/pull/251) ([johnhaley81](https://github.com/johnhaley81))

- Refactor classes [\#250](https://github.com/nodegit/nodegit/pull/250) ([maxkorp](https://github.com/maxkorp))

- Update Readme, to improve example code [\#248](https://github.com/nodegit/nodegit/pull/248) ([nmn](https://github.com/nmn))

- \[TEST\] Appveyor agent [\#247](https://github.com/nodegit/nodegit/pull/247) ([tbranyen](https://github.com/tbranyen))

- Refactor classes [\#246](https://github.com/nodegit/nodegit/pull/246) ([maxkorp](https://github.com/maxkorp))

- Buf methods [\#244](https://github.com/nodegit/nodegit/pull/244) ([tbranyen](https://github.com/tbranyen))

- Branch methods [\#243](https://github.com/nodegit/nodegit/pull/243) ([tbranyen](https://github.com/tbranyen))

- Blame methods [\#242](https://github.com/nodegit/nodegit/pull/242) ([tbranyen](https://github.com/tbranyen))

- Add revwalk.hide and revwalk.simplifyFirstParent [\#235](https://github.com/nodegit/nodegit/pull/235) ([tbranyen](https://github.com/tbranyen))

- Add revwalk.hide and revwalk.simplifyFirstParent [\#234](https://github.com/nodegit/nodegit/pull/234) ([orderedlist](https://github.com/orderedlist))

- Moved wrapper/copy out of include/src [\#233](https://github.com/nodegit/nodegit/pull/233) ([johnhaley81](https://github.com/johnhaley81))

- Removed ejs dependency [\#232](https://github.com/nodegit/nodegit/pull/232) ([johnhaley81](https://github.com/johnhaley81))

- Bump to latest libgit2 [\#229](https://github.com/nodegit/nodegit/pull/229) ([tbranyen](https://github.com/tbranyen))

- WIP: Refactor source generation templates from EJS to Combyne [\#227](https://github.com/nodegit/nodegit/pull/227) ([tbranyen](https://github.com/tbranyen))

- Test fixes [\#226](https://github.com/nodegit/nodegit/pull/226) ([johnhaley81](https://github.com/johnhaley81))

- Added new methods in checkout and repository [\#207](https://github.com/nodegit/nodegit/pull/207) ([tbranyen](https://github.com/tbranyen))

- Added additional remote methods [\#206](https://github.com/nodegit/nodegit/pull/206) ([tbranyen](https://github.com/tbranyen))

- Added git\_remote\_url and git\_remote\_load [\#205](https://github.com/nodegit/nodegit/pull/205) ([tbranyen](https://github.com/tbranyen))

- Add in remote listing support and test [\#204](https://github.com/nodegit/nodegit/pull/204) ([tbranyen](https://github.com/tbranyen))

- Attr methods [\#203](https://github.com/nodegit/nodegit/pull/203) ([tbranyen](https://github.com/tbranyen))

- Support latest libgit2 v0.21.0 [\#200](https://github.com/nodegit/nodegit/pull/200) ([tbranyen](https://github.com/tbranyen))

- Add Repo.openIndex [\#198](https://github.com/nodegit/nodegit/pull/198) ([tbranyen](https://github.com/tbranyen))

- Clone methods [\#195](https://github.com/nodegit/nodegit/pull/195) ([tbranyen](https://github.com/tbranyen))

- Remove all unused vendor directories [\#194](https://github.com/nodegit/nodegit/pull/194) ([tbranyen](https://github.com/tbranyen))

- \[WIP\] Mocha integration [\#189](https://github.com/nodegit/nodegit/pull/189) ([tbranyen](https://github.com/tbranyen))

- Auto gen structs [\#188](https://github.com/nodegit/nodegit/pull/188) ([tbranyen](https://github.com/tbranyen))

- Add in support for repository init ext [\#186](https://github.com/nodegit/nodegit/pull/186) ([tbranyen](https://github.com/tbranyen))

- moved libgit2 gyp to separate dir [\#184](https://github.com/nodegit/nodegit/pull/184) ([deepak1556](https://github.com/deepak1556))

- Remove all generated source code. [\#181](https://github.com/nodegit/nodegit/pull/181) ([tbranyen](https://github.com/tbranyen))

- Better installation flow for developing. [\#180](https://github.com/nodegit/nodegit/pull/180) ([tbranyen](https://github.com/tbranyen))

## [v0.1.4](https://github.com/nodegit/nodegit/tree/v0.1.4) (2014-06-13)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.1.3...v0.1.4)

**Closed issues:**

- Redis Backend [\#173](https://github.com/nodegit/nodegit/issues/173)

- using "Branch" object results in "undefined" error =\> branch.cc missing from binding.gyp? [\#166](https://github.com/nodegit/nodegit/issues/166)

- Windows: Failure on install [\#158](https://github.com/nodegit/nodegit/issues/158)

- Can't install v0.1.2 under OSX [\#155](https://github.com/nodegit/nodegit/issues/155)

**Merged pull requests:**

- \[WIP\] Prebuilt binaries. [\#178](https://github.com/nodegit/nodegit/pull/178) ([tbranyen](https://github.com/tbranyen))

- NodeJS v0.11.13 compatibility [\#175](https://github.com/nodegit/nodegit/pull/175) ([3y3](https://github.com/3y3))

- Fixed: "ReferenceError: error is not defined" [\#169](https://github.com/nodegit/nodegit/pull/169) ([danyshaanan](https://github.com/danyshaanan))

## [v0.1.3](https://github.com/nodegit/nodegit/tree/v0.1.3) (2014-05-02)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.1.2...v0.1.3)

**Merged pull requests:**

- Fix erroneous OS detection for installation in OS X. [\#156](https://github.com/nodegit/nodegit/pull/156) ([tbranyen](https://github.com/tbranyen))

## [v0.1.2](https://github.com/nodegit/nodegit/tree/v0.1.2) (2014-05-02)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.1.1...v0.1.2)

**Closed issues:**

- gyp ERR cannot find -lgit2 [\#150](https://github.com/nodegit/nodegit/issues/150)

- Read file from git server [\#145](https://github.com/nodegit/nodegit/issues/145)

- "emulate git log" example error [\#144](https://github.com/nodegit/nodegit/issues/144)

- repo.workdir\(\) crashes \(SIGSEGV\) on a bare repo [\#128](https://github.com/nodegit/nodegit/issues/128)

- How to create Branch using the API? [\#124](https://github.com/nodegit/nodegit/issues/124)

- 'npm run-script gen && npm install' on Ubuntu 13.04 [\#122](https://github.com/nodegit/nodegit/issues/122)

- Error while installing Nodegit 0.1.0 [\#120](https://github.com/nodegit/nodegit/issues/120)

- Question: How would I implement the equivalent of `git status`? [\#117](https://github.com/nodegit/nodegit/issues/117)

- Sync versions of all the methods [\#115](https://github.com/nodegit/nodegit/issues/115)

- Tick version \# [\#107](https://github.com/nodegit/nodegit/issues/107)

- Windows support [\#71](https://github.com/nodegit/nodegit/issues/71)

- Create test for history with merge commits [\#64](https://github.com/nodegit/nodegit/issues/64)

**Merged pull requests:**

- Fixed OSX Directions [\#143](https://github.com/nodegit/nodegit/pull/143) ([nickpoorman](https://github.com/nickpoorman))

- Add ubuntu lib dependencies to the readme [\#141](https://github.com/nodegit/nodegit/pull/141) ([bigthyme](https://github.com/bigthyme))

- WIP New installer. [\#140](https://github.com/nodegit/nodegit/pull/140) ([tbranyen](https://github.com/tbranyen))

## [v0.1.1](https://github.com/nodegit/nodegit/tree/v0.1.1) (2014-03-23)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.1.0...v0.1.1)

**Closed issues:**

- Misleading Readme [\#138](https://github.com/nodegit/nodegit/issues/138)

-  Cannot find module './build/Debug/nodegit' [\#137](https://github.com/nodegit/nodegit/issues/137)

- Support for Node 0.11+ [\#134](https://github.com/nodegit/nodegit/issues/134)

- installer cant seem to find python [\#126](https://github.com/nodegit/nodegit/issues/126)

- Cannot build when parent directory contains space\(s\)  [\#123](https://github.com/nodegit/nodegit/issues/123)

- question: how cvv8 is used? [\#118](https://github.com/nodegit/nodegit/issues/118)

- question: gen.js does not generate wrapper.h and wrapper.cc [\#116](https://github.com/nodegit/nodegit/issues/116)

- tree.diffIndex: pointer being freed was not allocated [\#112](https://github.com/nodegit/nodegit/issues/112)

- Use as a dependency of another node project? [\#110](https://github.com/nodegit/nodegit/issues/110)

- Segmentation faults with concurrent access? [\#104](https://github.com/nodegit/nodegit/issues/104)

- tree.diffWorkDir [\#101](https://github.com/nodegit/nodegit/issues/101)

- getReference passes unexpected object into callback [\#98](https://github.com/nodegit/nodegit/issues/98)

- index.removeByPath stops execution [\#97](https://github.com/nodegit/nodegit/issues/97)

- Missing example: commit to a local repo \(i.e. git add, git commit\) [\#96](https://github.com/nodegit/nodegit/issues/96)

- Get contents of index entry? [\#94](https://github.com/nodegit/nodegit/issues/94)

- Failure to Build nodegit  at Commit 0aa9a3c120 on OS X 10.6.8 [\#92](https://github.com/nodegit/nodegit/issues/92)

- TypeError: Cannot call method 'clone' of undefined [\#91](https://github.com/nodegit/nodegit/issues/91)

- missing cstring [\#88](https://github.com/nodegit/nodegit/issues/88)

- Installing fails - can't find vendor/libgit2/build [\#80](https://github.com/nodegit/nodegit/issues/80)

- Improving JavaScript API [\#73](https://github.com/nodegit/nodegit/issues/73)

- Using code-generation to generate  [\#70](https://github.com/nodegit/nodegit/issues/70)

**Merged pull requests:**

- Fix and improve testing. [\#139](https://github.com/nodegit/nodegit/pull/139) ([tbranyen](https://github.com/tbranyen))

- Support for Node 0.11+ [\#135](https://github.com/nodegit/nodegit/pull/135) ([pierreinglebert](https://github.com/pierreinglebert))

- Added git\_diff\_delta\_dup to git\_diff\_get\_patch to fix a memory issue whe... [\#113](https://github.com/nodegit/nodegit/pull/113) ([kmctown](https://github.com/kmctown))

- Try requiring build/Debug/nodegit if build/Release/nodegit wasn't found. [\#108](https://github.com/nodegit/nodegit/pull/108) ([papandreou](https://github.com/papandreou))

- Updated v0.18.0.json to make the index and DiffOptions arguments in Inde... [\#106](https://github.com/nodegit/nodegit/pull/106) ([kmctown](https://github.com/kmctown))

- Duplicate git\_error struct before passing it on [\#105](https://github.com/nodegit/nodegit/pull/105) ([papandreou](https://github.com/papandreou))

- Changed v0.18.0.json so diffWorkDir DiffOptions argument is optional. Ad... [\#103](https://github.com/nodegit/nodegit/pull/103) ([kmctown](https://github.com/kmctown))

- Reviewd and fixed examples [\#102](https://github.com/nodegit/nodegit/pull/102) ([micha149](https://github.com/micha149))

- cmake 2.8 is required to build nodegit [\#100](https://github.com/nodegit/nodegit/pull/100) ([dcolens](https://github.com/dcolens))

- new add-and-commit.js and remove-and-commit.js examples [\#99](https://github.com/nodegit/nodegit/pull/99) ([dcolens](https://github.com/dcolens))

- Add missing fields to index entry [\#95](https://github.com/nodegit/nodegit/pull/95) ([papandreou](https://github.com/papandreou))

- Made the tests pass and making each test self-contained [\#90](https://github.com/nodegit/nodegit/pull/90) ([FrozenCow](https://github.com/FrozenCow))

- Fixed compile error: memcpy not defined [\#89](https://github.com/nodegit/nodegit/pull/89) ([FrozenCow](https://github.com/FrozenCow))

- Add system dependencies for OSX install [\#82](https://github.com/nodegit/nodegit/pull/82) ([philschatz](https://github.com/philschatz))

## [v0.1.0](https://github.com/nodegit/nodegit/tree/v0.1.0) (2013-09-07)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.79...v0.1.0)

**Closed issues:**

- The api in README is incorrect [\#87](https://github.com/nodegit/nodegit/issues/87)

- message\_encoding in documentation for Repo.createCommit [\#86](https://github.com/nodegit/nodegit/issues/86)

- How to retrieve blob with binary content? [\#83](https://github.com/nodegit/nodegit/issues/83)

- Incorrect commit oid's when aggregated from commit.history\(\) [\#81](https://github.com/nodegit/nodegit/issues/81)

- How do you list branches in repo? [\#76](https://github.com/nodegit/nodegit/issues/76)

- License? [\#74](https://github.com/nodegit/nodegit/issues/74)

- Nested walks scatter memory and cause SEGFAULTS [\#72](https://github.com/nodegit/nodegit/issues/72)

- feature request: Provide fileMode / getType method on tree entries [\#67](https://github.com/nodegit/nodegit/issues/67)

- Document DiffList [\#66](https://github.com/nodegit/nodegit/issues/66)

- Procedure for moving development to nodegit/nodegit [\#55](https://github.com/nodegit/nodegit/issues/55)

- Cannot install on OSX [\#49](https://github.com/nodegit/nodegit/issues/49)

**Merged pull requests:**

- Codegen [\#79](https://github.com/nodegit/nodegit/pull/79) ([nkallen](https://github.com/nkallen))

- Updated LICENSE to MIT [\#75](https://github.com/nodegit/nodegit/pull/75) ([tbranyen](https://github.com/tbranyen))

## [v0.0.79](https://github.com/nodegit/nodegit/tree/v0.0.79) (2013-04-05)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.778...v0.0.79)

**Closed issues:**

- Clarify commit.history documentation [\#63](https://github.com/nodegit/nodegit/issues/63)

- Python error on installing nodegit 0.0.77 [\#59](https://github.com/nodegit/nodegit/issues/59)

## [v0.0.778](https://github.com/nodegit/nodegit/tree/v0.0.778) (2013-03-26)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.77...v0.0.778)

**Merged pull requests:**

- See issue \#59 [\#60](https://github.com/nodegit/nodegit/pull/60) ([dctr](https://github.com/dctr))

## [v0.0.77](https://github.com/nodegit/nodegit/tree/v0.0.77) (2013-03-24)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.76...v0.0.77)

## [v0.0.76](https://github.com/nodegit/nodegit/tree/v0.0.76) (2013-03-24)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.75...v0.0.76)

## [v0.0.75](https://github.com/nodegit/nodegit/tree/v0.0.75) (2013-03-24)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.74...v0.0.75)

**Closed issues:**

- incomplete error reporting [\#57](https://github.com/nodegit/nodegit/issues/57)

- Segmentation Fault in raw-commit.js [\#56](https://github.com/nodegit/nodegit/issues/56)

- Another Mac OSX install fail [\#53](https://github.com/nodegit/nodegit/issues/53)

- unit tests broken in travis-ci [\#52](https://github.com/nodegit/nodegit/issues/52)

- "Image not found" with require\("nodegit"\) on Mac OS X [\#51](https://github.com/nodegit/nodegit/issues/51)

- Cannot Compile on 0.8.\* [\#47](https://github.com/nodegit/nodegit/issues/47)

- No suitable image found. [\#46](https://github.com/nodegit/nodegit/issues/46)

- Fails to require module on latest node version [\#43](https://github.com/nodegit/nodegit/issues/43)

- Compilation error node 0.6.1 [\#32](https://github.com/nodegit/nodegit/issues/32)

- commit.history work like slice [\#17](https://github.com/nodegit/nodegit/issues/17)

- Sync and Async methods [\#16](https://github.com/nodegit/nodegit/issues/16)

- Comment all code methods [\#1](https://github.com/nodegit/nodegit/issues/1)

## [v0.0.74](https://github.com/nodegit/nodegit/tree/v0.0.74) (2013-03-21)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.73...v0.0.74)

## [v0.0.73](https://github.com/nodegit/nodegit/tree/v0.0.73) (2013-03-21)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.72...v0.0.73)

**Closed issues:**

- pass through python flag to node-gyp [\#54](https://github.com/nodegit/nodegit/issues/54)

- update package.json [\#28](https://github.com/nodegit/nodegit/issues/28)

- Rewrite Notes [\#27](https://github.com/nodegit/nodegit/issues/27)

- Tree each method is synchronous [\#15](https://github.com/nodegit/nodegit/issues/15)

## [v0.0.72](https://github.com/nodegit/nodegit/tree/v0.0.72) (2013-03-06)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.71...v0.0.72)

## [v0.0.71](https://github.com/nodegit/nodegit/tree/v0.0.71) (2013-03-06)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.6...v0.0.71)

**Closed issues:**

- Unable to load shared library [\#39](https://github.com/nodegit/nodegit/issues/39)

- Expand Convenience Unit Tests [\#38](https://github.com/nodegit/nodegit/issues/38)

- repo has no method 'branch' [\#35](https://github.com/nodegit/nodegit/issues/35)

- update for node 0.5.9 [\#29](https://github.com/nodegit/nodegit/issues/29)

**Merged pull requests:**

- Converted from eio\_custom to uv\_queue\_work [\#48](https://github.com/nodegit/nodegit/pull/48) ([faceleg](https://github.com/faceleg))

- Fix Load-Order Bug [\#44](https://github.com/nodegit/nodegit/pull/44) ([fatlotus](https://github.com/fatlotus))

- Update documented commands needed to run tests [\#42](https://github.com/nodegit/nodegit/pull/42) ([shama](https://github.com/shama))

- Fix typo in README.md [\#41](https://github.com/nodegit/nodegit/pull/41) ([Skomski](https://github.com/Skomski))

- Issue 35: repo has no method 'branch' [\#40](https://github.com/nodegit/nodegit/pull/40) ([cholin](https://github.com/cholin))

- Refactor [\#37](https://github.com/nodegit/nodegit/pull/37) ([mmalecki](https://github.com/mmalecki))

## [v0.0.6](https://github.com/nodegit/nodegit/tree/v0.0.6) (2011-12-19)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.4...v0.0.6)

**Closed issues:**

- commit event with undefined commit [\#26](https://github.com/nodegit/nodegit/issues/26)

- Convenience methods are not convenience!  [\#24](https://github.com/nodegit/nodegit/issues/24)

**Merged pull requests:**

- Node 0.6x fixes [\#34](https://github.com/nodegit/nodegit/pull/34) ([moneal](https://github.com/moneal))

## [v0.0.4](https://github.com/nodegit/nodegit/tree/v0.0.4) (2011-05-14)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.3...v0.0.4)

**Closed issues:**

- repo.branch fails on empty repo [\#22](https://github.com/nodegit/nodegit/issues/22)

- example/convenience-repo.js errors [\#21](https://github.com/nodegit/nodegit/issues/21)

- Branch history each method is asynchronous [\#11](https://github.com/nodegit/nodegit/issues/11)

## [v0.0.3](https://github.com/nodegit/nodegit/tree/v0.0.3) (2011-04-13)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.2...v0.0.3)

**Closed issues:**

- error handling [\#18](https://github.com/nodegit/nodegit/issues/18)

- Windows link issue [\#12](https://github.com/nodegit/nodegit/issues/12)

## [v0.0.2](https://github.com/nodegit/nodegit/tree/v0.0.2) (2011-03-14)

[Full Changelog](https://github.com/nodegit/nodegit/compare/v0.0.1...v0.0.2)

## [v0.0.1](https://github.com/nodegit/nodegit/tree/v0.0.1) (2011-03-10)



\* *This Change Log was automatically generated by [github_changelog_generator](https://github.com/skywinder/Github-Changelog-Generator)*
