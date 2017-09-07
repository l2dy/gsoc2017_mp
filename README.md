# GSoC 2017 Work Product Summary

## Tasks

I implemented and deployed two bots for [the MacPorts ports tree repository](https://github.com/macports/macports-ports).

1. CI bot: tests pull requests on Travis CI
2. PR bot: mention port maintainers and add labels

The design documents for the two bots can be found [here](https://github.com/l2dy/gsoc2017_mp/tree/master/design).

## Repositories Involved

I've created a GitHub organization https://github.com/macports-staging and 5 repositories under it for testing purposes (I don't want to mistakenly mention unrelated people or assign wrong labels to PRs).

* [mpbot-github](https://github.com/macports-staging/mpbot-github) (Future development should happen in develop branch of [macports/mpbot-github](https://github.com/macports/mpbot-github).)
* [macports-ports](https://github.com/macports-staging/macports-ports) (Staging and testing area.)
* [macports-base](https://github.com/macports-staging/macports-base) (Future improvements should happen in travis-ci branch of [macports/macports-base](https://github.com/macports/macports-base).)
* [getopt](https://github.com/macports-staging/getopt) (Replaced by [macports/getopt](https://github.com/macports/getopt).)
* [pure-getopt](https://github.com/macports-staging/pure-getopt) (Replaced by getopt.)

Real deployment happened in the following repositories.

### New Repositories and Branches

* https://github.com/macports/mpbot-github (source code of the PR and CI bots)
* https://github.com/macports/macports-base/tree/travis-ci (CI bot dependency, macports-base binaries)
* https://github.com/macports/getopt (CI bot dependency, for [mpbb](https://github.com/macports/mpbb))

### Updates to Existing Repositories

* https://github.com/macports/macports-ports/tree/master/_ci and [.travis.yml](https://github.com/macports/macports-ports/blob/master/.travis.yml) (Travis CI setup for the ports tree)
* https://github.com/macports/macports-infrastructure/blob/master/jobs/build_deploy_prbot.sh (PR bot auto deployment, by mentor @neverpanic)

## Travis CI Limitations Met

* [Build timeouts](https://docs.travis-ci.com/user/customizing-the-build#Build-Timeouts)
* [Log length limit](https://docs.travis-ci.com/user/common-build-problems/#Log-Length-exceeded)

## Future Plans

Some features in the design documents aren't implemented during this GSoC.

1. Mailing in PR bot (As development moved to GitHub, we can assume that GitHub logins of active maintainers can be found by the PR bot.)
2. Communication between the two bots (Not enough time left for a secure implementation, but also because that this feature is proven to be less important than initially thought.)

## Other Contributions to the MacPorts Project

During the coding period, I've also made the following contributions to the MacPorts Project:

* Made 256 commits [[1]](https://github.com/macports/macports-ports/graphs/contributors?from=2017-05-30&to=2017-08-21&type=c) and sent 82 PRs [[2]](https://github.com/macports/macports-ports/pulls?utf8=%E2%9C%93&q=is%3Apr%20author%3Al2dy%20created%3A2017-05-30..2017-08-21%20) to the ports tree.
* Reviewed and merged many PRs sent to the ports tree.
* Created 54 tickets and closed many tickets on Trac. [[3]](https://trac.macports.org/query?reporter=~l2dy&time=May+30%2C+2017..Aug+21%2C+2017&col=id&col=summary&col=time&col=status&col=owner&col=type&col=priority&col=changetime&col=port&order=priority)
* Updated 2 wiki pages on Trac. [[4]](https://trac.macports.org/wiki/PortfileRecipes?action=diff&version=96) [[5]](https://trac.macports.org/wiki/XcodeVersionInfo?action=history)
