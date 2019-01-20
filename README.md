# [xkcd.network](https://xkcd.network) Mastodon

This repository contains the Mastodon fork which is used on the
[xkcd.network](https://xkcd.network) instance.

## Feature changes

The following changes have been made from upstream. The sources of changes are
noted in parentheses.

- Increase profile bio length to 1000 chars (combined patch from
[Interlinked](https://mst3k.interlinked.me) and [Cybre
Space](https://cybre.space)).

- Increase number of profile metadata tags from 4 to 16
([Interlinked](https://mst3k.interlinked.me)).

- Increase the display name length from 30 to 48 characters
([Interlinked](https://mst3k.interlinked.me)).

- Increase toot length to 1024 chars (adapted from
[mastodon.host](https://mastodon.host)'s patches).

- Use the Node.js `ws` module for handling websocket connections instead of the
`uws` module, as some people have concerns about source code availability of the
latter (adapted from the patch presented in [this
issue](https://github.com/tootsuite/mastodon/issues/7710))


## Repository layout

This repository is organised into the following branches. Note that most or all
of these branches will be rebased upon major version bumps of upstream Mastodon,
however the patched versions of the codebase which are run in production will be
tagged.

- the `upstream` branch tracks upstream tootsuite mastodon development.

- the `local` branch includes instance-local changes, such as our favicon and
this README.

- the `feature/*` branches each contain one of the feature mentioned above.

- the `production` branch is the code which is running live on
[xkcd.network](https://xkcd.network), and is combined of a merge of the upstream
release tag, the local changes and the feature branches.

