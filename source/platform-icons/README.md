# Platform badge icons

Source SVGs for `media/marty/platform/*.png`, drawn to be legible at the size
they are actually used: 26px tall, on a translucent chip in the corner of a
game tile.

The first attempt reused each emulator core's own `icon.png` from
`game.libretro.*`. That looked reasonable at 512px and failed completely at
badge size - they are *core* logos, not platform logos, and several are
wordmarks (`PCSX`, `DOSBox`, `M+`), which is exactly the "just words" the
badges were meant to replace. They also had no visual consistency with each
other.

These are silhouettes instead: one bold shape per platform, no text, no thin
strokes. Re-render after editing with

    for f in *.svg; do
      convert -background none "$f" -resize 64x64 "../../media/marty/platform/${f%.svg}.png"
    done

Black fills are deliberate: they are cut-outs that read against the dark chip
the badge sits on.
