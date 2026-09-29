# tmt-loader-games

The copies of the games that [tmt-loader](https://github.com/PeerInfinity/tmt-loader) serves. The loader includes
this repository as a git submodule at `games/`. On its own it does nothing; to play a game, use the loader.

Each directory `<id>/` holds one game, as the loader serves it:

- it keeps its **author's own licence files and credits**, exactly as the author published them;
- it is a copy of the author's repository **at one commit**. The loader records that commit and every original file
  of the copy in `manifests/<id>.json` (`upstream.repo`, `upstream.commit`) and `games-pristine/<id>.json`;
- the only change from the author's files is to media, under the same filenames: images are re-encoded as WebP at
  the same pixel size, and audio files are replaced by a short silent stub. Code, markup, text and licence files are
  byte-identical to the author's; the loader's `check-manifest` gate holds that.

Everything else lives in the loader repository: the manifests, the tools that add and update a game, the tests, and
the site.

This repository may be removed later if the loader switches to loading each game from its author's own repository.

## For the authors of these games

This is an early, low-priority side project. It may change a lot or be taken down.

**If one of these is your game and you'd like it removed,
[open an issue on tmt-loader](https://github.com/PeerInfinity/tmt-loader/issues) and I'll take it down.** You don't
need to give a reason. Issues opened here are read too.
