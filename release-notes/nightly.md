**The newest work, less tested.** Use the stable release for your main
adventure; try this one in its own folder with a copy of your save.

**New in nightly4**
- **Export the game's songs** (Mods menu): every song as a WAV file in
  `music\export`, with its loop points, so you can hear which name is which
  song and line a recording up with its loop. Music packs also play WAV
  files (with a sampler loop), so an exported song can be edited and put
  back.
- **Widescreen: the sepia memory scenes** are sepia across the whole
  picture (the right side was darker, with a seam; #18). Thanks to celvrc
  for the report.

**New in nightly3**
- **The European version** (Europe, game code YDQP) builds and plays,
  in English, French, German, Italian or Spanish: **Game > Language**.
  Thanks to romusan495.
- **Linux**: an AppImage that builds the game from your ROM, with a window
  to choose it and follow the build. Thanks to rakmahefa.
- **HD text** (new, off at first: Graphics > HD text, or F1): the game's
  letters drawn again at full resolution with real fonts. Thanks to Arthur
  Ferreira Soares.
- **Mods menu**:
  - **Texture packs**: PNG pictures in the `textures` folder are drawn
    instead of the game's textures. To make one, turn on *Dump textures*
    and play: every texture shown lands in `textures\dump`. Redraw them,
    keep their names, put them in `textures`, then *Reload*.
  - **Upscale the 3D textures** (off at first): xBR, 4x.
  - Hold **`** (left of 1) to see the game's own textures, to compare.
  Thanks to romusan495, whose code the texture packs are built on.
  - **Music packs**: OGG or FLAC recordings in the `music` folder play
    instead of the game's songs, each named after the song it replaces
    (`BG_012.ogg`). *Open the music folder* lists every song in
    `songs.txt`, and *Show each song's name as it starts* tells you which
    one is playing. Songs loop on the usual `LOOPSTART` / `LOOPLENGTH`
    tags (else the whole file); jingles (`ME_`) play once. The game's
    fades, pauses and stops carry over, and the original keeps its timing
    silently, so nothing waits differently. `music_pack_volume` in
    settings.ini sets their level. While playing together, the game's own
    music plays.
- **Widescreen**:
  - The poison bog's flash, the "Some days later..." card, the Battle
    Records card and white flashes cover the sides too (they reached one
    side only).
  - The game's movies (the sacred tree) show both screens stacked, as on
    the DS.
  - **Battle HUD** (experimental, off at first: Modern > Widescreen: battle
    HUD): the party's panels stacked in the bottom left over the 3D, the
    experience and level-up windows big at the top. Thanks to romusan495.
- **Graphics > Soft shadows and glows** can be turned off (the DS's stepped
  look).
- **Show on Discord what I'm playing** (Modern menu): Dragon Quest IX and
  the version on your Discord profile while the game runs.

Still being looked into: in widescreen, the sepia memory scenes show a
darker strip at the right side (#18), and the Zoom menu can smear in the
dynamic widescreen (#16).

**New in nightly2**
- **The menu bar in fullscreen works**: it was greyed out and wouldn't open.
- **Outlines only on models' edges**: nightly1's smooth outlines also traced
  fire, people drawn as flat pictures and speech bubbles. Not any more.
- **No flash of misplaced scenery in widescreen**: something coming into
  view at the sides (the railing by Coffinwell's well) could be drawn in the
  wrong place for one frame.
- **The turnstile in Gortress's prison no longer pops in** across the
  middle of the picture in widescreen: very large things are now drawn a
  good way before they can come into view (the game only checks a small box
  around their centre). Thanks to celvrc for the report.
- **No flicker of sleeping people as the camera turns**: Enhanced drew each
  frame a moment too early and showed the old angle's picture for a frame.

Still being looked into: the light from the window in Upover's inn
flickers (#19). It isn't widescreen: it does it with the sides off too.

**New since stable v31**

Installing
- **The installer fixes broken or old MSYS2 setups by itself.** If you saw
  `target not found: mingw-w64-ucrt-x86_64-gcc` and then
  `No module named 'yaml'`, your MSYS2 was older than the packages the build
  needs: it now gets them added. It also uses an MSYS2 you already have on
  any drive and installs only what's missing, clears the lock an
  interrupted update leaves behind ("unable to lock database"), installs
  MSYS2 without winget when needed, and never deletes an old MSYS2 (it asks
  first and keeps it renamed). Thanks to everyone on the Discord who
  tracked this down.
- **A ROM inside a .zip works**: pick the zip, no unzipping needed.

Fixes
- **Game > Controls works**: changing a key or controller button now
  finishes (it didn't at all in v31).
- **Leaving fullscreen** gives the window back its title bar and borders.
- **Fullscreen**: the menu bar shows over the top of the picture instead of
  shrinking it.
- **Quitting asks first** (Esc, the window's X, Alt+F4, File > Exit), so a
  stray key can't lose your progress. "Don't ask again" turns it off.
- **Walking with the stick** no longer goes the wrong way after a menu, a
  battle or a scene change while the stick is held.
- **Widescreen**:
  - Places made only for the DS's width (the starry sky at the start, the
    way up to the Observatory) get black sides instead of showing past the
    edge of the scene. Found another one? Modern > "Widescreen: black sides
    in this place".
  - The background behind menus and the title screen continues into the
    sides instead of being smeared into stripes.

Enhanced graphics
- **Character outlines** are an even, smooth line instead of jagged steps
  at the models' corners. Graphics > Character outlines: Thin (the
  default), Medium, or Like the DS.
- **Soft shadows** stay a smooth gradient instead of rings of flat steps.

New
- **Tab turns fast forward on and off** (three arrows in the bottom left
  while it's on). Prefer holding it? Set `fast_forward = hold` in
  settings.ini.
- **Game > Save file**: export your save, or import one (also DeSmuME's
  .dsv and melonDS saves). Your current save is backed up first.
- **The controller's Share button** takes a screenshot.
- **Bug reports attach themselves**: after Send, the report is on your
  clipboard, so on the GitHub page it's just **Ctrl+V**, then **Create**
  (or paste it on the Discord). Reports now include a picture of the window
  as you saw it and your display settings.

**How to install**: download *Source code (zip)* below, unzip it and
double-click `Install Dragon Quest IX.bat`. Already playing? Use Help >
Check for updates instead.
