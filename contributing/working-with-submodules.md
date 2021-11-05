# Grida and submodule packages

> Sorry. We use it lot. Wich makes this more elegant, but may make things harder to work with. It's best for us until our foundation techs grows mature.



## Why using submodule?

For best modularity of each features and ui components, we are spearating all the functionalities down to related repositories. You may feel some of the modules are redundant / inefficient to have as submodule. Yes, that is true. Such like [editor-ui](https://github.com/reflect-ui/reflect-editor-ui) can be used as a npm package, but most of the work is happening in this Grida repo, so we are going to use submodule for a while. After the project gets mature enought, we will detatch submodule and use as a npm package.



## Contributor's notice

When contributing to Grida, you might end up editing bunch lines of code under submodule packages. This workflow makes PR and branch management harder. We recommand you to contact us and join as our managed collaborator to get github access for direct PRs (not forking).



## Forking & PR to repository that uses git submodule as package.

**TL;DR**

Fork the submodules as well before commiting. (If you are a heavy contributor)

**Steps**

1. fork the main repo that you are trying to work on.
2. when you edit package source (which upstream is other reposutory than your original main fork), You'll end up unable to push changes - VSCode will ask you to fork the submodule too.
3. Once you fork submodule, You'll have to modify `.gitmodules` file to look at your submodule's remote.
4. Make PR as that

**How Merging works**

TL;DR - Your job is done! - We'll do the rest for merging

1. Our maintainers will manage the open PR - check the main repo's code.
2. If that turns ok, we'll take a look into your submodule fork.
   1. We'll force create a PR from your GitHub fork (We ask for you this first of course) & Merge it.
3. Comming back to main PR, we'll modify the `.gitmodules` file to look up the merged submodule's remote.
4. Finally merging as usual.

As you can see, the process are complex. We made all the demos and environments this to not happen - You'll find just ok with working with single repository without touching submodule packages. I.e. [Design To Code](https://github.com/gridaco/designto-code) project has it's own demo website to develop & contribute on it on a isolated environment.

