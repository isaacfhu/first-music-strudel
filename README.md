# first-music-strudel

First time making music with strudel

Copy and paste into `strudel.cc/`:

```
// "happy sunny day"
// @license CC BY-NC-SA 4.0 https://creativecommons.org/licenses/by-nc-sa/4.0/
// @by Isaac Fischer
// @url https://github.com/isaacfhu/first-music-strudel

setcpm(24)

const sdrums = sound("bd mt [bd bd] sd, hh*8").bank("RolandTR909")

const sbass = note(`<[36 - 36 [- 36]] [41 - 41 [ - 41]]
  [43 - 43 [43]] [33 - 33 [33]]>
  `)
  .sound("gm_acoustic_bass")

const slead = note(`<[55 52 -]*2 [57 50 -]*2
  [59 48 -]*2 [60 45 -]*2>,

  48 50 52 [53 55 57 59 60 62]/2
`).sound("gm_agogo")

const svariation = note(`<[e5 - g5 [e5 c5]] [e5 - g5 [c6 a5]]
  [g5 - b5 [d6 b5]] [a5 - c6 [e6 [c6 a5]]]
>`)
  .sound("gm_celesta")
  .gain(0.7)

lead: slead

bass: arrange(
  [4, silence],
  [12, sbass]
)

drums: arrange(
  [8, silence],
  [8, sdrums]
)

variation: arrange(
  [8, silence],
  [8, svariation]
)
```

Made during aria.hackclub.com <br />
My timelapse link (ordered by session):

1. https://lapse.hackclub.com/timelapse/jnl-Z4R7A2fk
2. https://lapse.hackclub.com/timelapse/ZCLT-ajB5dxO
3. https://lapse.hackclub.com/timelapse/vCWRGViL55_i
