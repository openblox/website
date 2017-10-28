---
title: "Contributing"
---
You can contribute to OpenBlox in many ways. You can fix mistakes you see while browsing the wiki, and you can improve content or write new content about OpenBlox. If you’re a programmer, you can contribute to the game engine or the other tools that are developed as part of the OpenBlox project.

## Donation

We accept donations in the form of Bitcoin, Litecoin, and PayPal payments. You can find our [current addresses](/donate.asc) signed by the project leader, John Harris. Monetary contributions help keep our servers running, pay for our domain name, and internet access, among other things.

### Hardware

We also accept hardware donations including, but not limited to, the following hardware devices:

* Rackmount servers
* Workstation computers
* Laptop computers
* 10/100 or gigabit managed ethernet switches
* Uninterruptible power supplies

Donated hardware does not have to be in working condition, but it would be preferable if we don’t have to take our system administrator away from other work to fix devices. Send hardware offers to [hardware-donation@openblox.org](mailto:hardware-donation@openblox.org).

## Documentation

Documentation of the OpenBlox game engine and related software is done on [the OpenBlox wiki](https://wiki.openblox.org). To contribute, you only need to create an account. As a measure against spam and vandalism, new accounts cannot upload files, create pages other than talk pages, or move pages. Accounts that have existed for more than five days and have more than fifteen contributions are marked as autoconfirmed and can do all these things. If you need help editing the wiki, you can see the [MediaWiki help pages](https://www.mediawiki.org/wiki/Help:Contents) or ask on [talk pages](https://www.mediawiki.org/wiki/Help:Talk_pages).

Class documentation is done using the [Infobox class](https://wiki.openblox.org/wiki/Template:Infobox_class), [Property](https://wiki.openblox.org/wiki/Template:Property), [Method](https://wiki.openblox.org/wiki/Template:Method), and [Event](https://wiki.openblox.org/wiki/Template:Event) templates. You can find documentation for each of these templates on the template pages.

## Translation

We’re always looking for translators for this website and the wiki, as well as the engine and client. If you wish to translate the wiki, contact [mark@openblox.org](mailto:mark@openblox.org). Translation of the engine, client, and studio is all done through Qt Linguist. If you need any help with that, contact [johnmh@openblox.org](mailto:johnmh@openblox.org).

## Development

The OpenBlox source code is hosted at [git.openblox.org](https://git.openblox.org). You will need the Git version control system installed on your system to contribute. You can choose one of the repositories listed and use the `git clone` command to clone the repository using one of the URLs given. For example, to clone the code repository for the game engine, you could run `git clone https://git.openblox.org/openblox/libopenblox.git`.

This will create a directory containing the source code where you can make changes, stage them, and commit them. If you are not familiar with Git, you can see the Git tutorial with the command `git help tutorial`, or you can see the [Git tutorial](https://www.kernel.org/pub/software/scm/git/docs/gittutorial.html) and the [Git User’s Manual](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html) in a web browser. After making changes, you will need to build OpenBlox to test them. This is done with the `make all` command after installing the dependencies.

Once you have commits you would like to submit for review, run `git format-patch --to=devel@lists.openblox.org <var>commit</var>`. Git will generate a patch for every commit done after (and including) the commit designated by <var>commit</var>, which can be the commit’s hash, `HEAD~1` for the previous commit, `HEAD~2` for the commit before that commit,&nbsp;etc., or `origin/master` if you want to include all commits added to your local repository that are not in the upstream repository. The command will give you the name of the patch files created. Send these messages as email to [devel@lists.openblox.org](mailto:devel@lists.openblox.org) for review, keeping the subject and message content generated by Git. You can use any mail client, but we recommend you use `git send-email` (see `git help send-email`), which on Debian and Fedora you can get from the `git-email` package. You can add an introductory message with the `--compose` option, which is likely to be desirable for nontrivial patches.

When you are creating a commit for another user, you can use `git commit --author="AUTHOR"` to specify the change’s author. Each line in commit messages should be 71&nbsp;characters or less. Commit messages should contain only printable UTF-8 characters. Always use present tense. If a commit has multiple authors, for example altered patches, prepend an empty line to your commit message followed by “Co-Authored-By: Name &lt;email&gt;”.

### Bug tracker

The OpenBlox project hosts [a Bugzilla installation](https://bugs.openblox.org) which is to be used for the OpenBlox engine and related projects.