=========================
scrapinghub-stack-hworker
=========================

Software stack fully compatible with Scrapy Cloud 1.0.

Versioning
==========

Versioning is done in the following manner:

- latest version of the stack marked with `latest`
- each published version of the stack is also marked with `<release date>` tag
- some versions are pinned, check CHANGELOG for changes

All stack versions are listed correspond to a Docker image listed at:

- https://hub.docker.com/r/scrapinghub/scrapinghub-stack-hworker/tags/

Release procedure
=================

When you're going to release a new version of the stack, you should:

1. Do not forget to pull latest changes from master::

    git pull origin

2. Tag it with a correct tag string (see Versioning section above)::

    git tag <tag>

  Example::

    git tag 20160731

3. Push tags to the repo::

    git push -f --tags

  Tags should be pushed before pushing changes because otherwise build will not be triggered and developer will be required to find the build in drone and trigger it manually again after tags are pushed.

  Tags should be pushed with ``-f`` almost all the time because we override tags frequently.

4. Push the changes only after tags::

    git push

5. After release it's necessary to check that tag is updated both in github and hub.docker.com:

  - https://github.com/scrapinghub/scrapinghub-stack-hworker/releases
  - https://hub.docker.com/r/scrapinghub/scrapinghub-stack-hworker/tags/
