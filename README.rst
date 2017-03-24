======================================
[DEPRECATED] scrapinghub-stack-hworker
======================================

.. warning:: **This stack is deprecated.** Please use `scrapinghub-stack-scrapy <https://github.com/scrapinghub/scrapinghub-stack-scrapy/releases>`_ instead.

Software stack fully compatible with Scrapy Cloud 1.0.

Versioning
==========

Versioning is done in the following manner:

- latest version of the stack marked with `latest` tag;
- each published version of the stack is also marked with `<release date>` tag.

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

3. Push the changes and the tag to the repo::

    git push origin master <tag>

  Example::

    git push origin master 20160731

  Tags should be pushed at the same time when pushing changes (or before it) because otherwise build will not be triggered and developer will be required to find the build in drone and trigger it manually again after tags are pushed.


5. After release it's necessary to check that tag is updated both in github and hub.docker.com:

  - https://github.com/scrapinghub/scrapinghub-stack-hworker/releases
  - https://hub.docker.com/r/scrapinghub/scrapinghub-stack-hworker/tags/
