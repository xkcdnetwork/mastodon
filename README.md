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

## Repository layout

This repository is organised into the following branches, most of
which will be rebased at some point or another.

- the `upstream` branch tracks upstream tootsuite mastodon development.

- the `local` branch includes instance-local changes, such as our favicon and
this README.

- the `feature/*` branches each contain one of the feature mentioned above.

- the `production` branch is the code which is running live on
[xkcd.network](https://xkcd.network), and is combined of a merge of the upstream
release tag, the local changes and the feature branches.

