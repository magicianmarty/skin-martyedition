# Marty Edition (Kodi skin)

A fork of Kodi's **Estuary** skin, for a CoreELEC box on a television driven
by a remote.

## This is a separate project

Estuary is by **phil65** and **Ichabod Fletchman** and essentially all of this
is their work: <https://github.com/xbmc/skin.estuary>. It is the skin most
people should use. This edition is maintained separately by **magicianmarty**
and changes only the things an add-on cannot change for itself.

## Why a skin at all

A Kodi plugin hands the skin a list of items and the skin decides what they
look like. That is a hard boundary, and it is where three separate requests
kept running aground:

* **Tile size.** A plugin can ask for a view, but not for a bigger one.
  Estuary's video wall tile is 300x301; ours is 410x316 with a 16:9 thumbnail.
* **What is written under a tile.** Estuary's wall draws one label plus a
  small overlay on the artwork. Ours draws the title and the channel on
  separate lines, so neither has to be squeezed into the other.
* **One home screen.** Plex and YouTube are two add-ons sharing a television.
  Leaving one drops you into the other, because nothing owns the space
  between them. Only a skin can.

## What is different so far

| | |
|---|---|
| **Bigger video tiles** | A dedicated `MartyVideoTile` layout in the wall view, rather than editing Estuary's shared `InfoWallEpisodeLayout` - that one is used by three other views and the home screen. |
| **Title and channel** | Two lines under the tile instead of one label and an overlay. |

## Licence

CC BY-SA 4.0 and GPL-2.0, the same as Estuary.
