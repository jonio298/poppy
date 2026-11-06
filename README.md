# Charles Ross Memorial Slideshow

A full-screen photo slideshow created in loving memory of Charles “Charlie” “Dad” “Poppy” Ross.

## Two modes

**Play mode** is the clean slideshow.
- Tap or click **Begin slideshow** to start. It begins on the opening slide (“In Loving Memory”), which stays for 12 seconds (adjustable on the Show tab) before the photos start. The photos are timed evenly across the 22:24 playlist by default.
- **Controls:** the play/pause bar stays at the bottom center, on the intro slide too, whenever the page is not full screen. In full screen it disappears and comes back when you move the mouse (or tap on a phone).
- **Phones:** swipe left/right to change photos.
- **Home:** the house button at the upper left of the slideshow goes back to the opening slide and stops, like Esc.
- **Keyboard:** arrow keys to move, space to pause, **R** to restart, **F** for full screen, **E** to switch to Edit mode, **Esc** to leave full screen and pause; press **Esc** again (outside full screen) to go back to the opening page, where Edit mode is.
- **Restart:** the ↻ button (or **R**) starts over from the first photo. When the show ends, a **Restart slideshow** button appears.
- **Auto-scroll:** the loop button (or the checkbox on the Show tab) keeps the show playing continuously, starting over after the last photo.

**Edit mode** opens a side menu (a bottom sheet on phones). Switch back with **▶ Play** at the top of the menu.
- **Slides:** **＋ Add my own photos** (or drag picture files onto the page) adds pictures from your device. They are shrunk to a sensible size and kept in this browser, then behave like any other slide. Below that, the full list of photos with thumbnails. Drag any slide up or down to reorder (press and hold on a phone, or focus the **⠿** handle and use the up/down arrow keys), tap a slide to preview it, **✎** to edit it, or the red **✕** to delete it (with Undo, and a Restore list for deleted slides).
- **Slide:** grouped into Text, How the photo looks, When it plays, Position, and “Use this slide’s choices on every slide” (copies its transition, style or filter to all slides). For the selected photo, change its date, add a caption, resize it, pick a photo style (thin white border, plain, polaroid, gold frame, film strip), pick a filter (black & white, sepia, vintage, warm, cool, vivid, faded, noir, soft glow) and its strength, pick its transition and preview it, set how many seconds it stays and its Ken Burns motion, apply its transition or style to all slides, move it earlier/later, reset it, or delete it.
- **Show:** (it ends with **Restore these settings to the defaults**, which resets everything on this tab but leaves your slides, text and theme alone) the opening text, default transition and photo style, seconds per photo, Ken Burns motion, photo size, and the vintage film look.
- **Theme:** colour presets (or any background/accent colour) and font.
- **Versions:** every **Save** keeps a dated, timed version here. **Open** one to edit it (it then opens on reload), **Rename**, **Download** it (with your own photos inside) or **Delete** it. The original slideshow is always listed too.

## Songs and the timeline

The slideshow is timed to seven songs (What a Wonderful World, When I Fall in Love, Only You, Can't Help Falling in Love, In the Mood, Goodnight My Love, The Prayer; about 22:34 together). **This page does not play the songs.** Start them on your own device; the page shows which song each slide belongs to and times the slides to match.

- Edit mode → **Slides** tab: a colored timeline bar (with a marker for the selected slide) and a colored section for each song showing its time range, how many slides it has and how many seconds each slide gets.
- **Reorder the songs:** drag a song bar (by its ⠿ handle, or anywhere on the bar; press and hold on a phone) to move the whole song, with all its slides. While you drag, every song folds so only the bars show. With the handle focused, Up/Down arrows also move it. Numbers show the order the songs play in.
- **✦ Suggested slide show:** the button under Play/Edit in the Edit bar (also in the Versions tab, with the reasoning for each song) opens a ready-made show built around the mood of each song and Poppy's life: *What a Wonderful World* (where he came from), *When I Fall in Love* (courtship and the 1959 wedding), *Only You* (building a family), *In the Mood* (joy: dancing, weddings, parties), *Can't Help Falling in Love* (a love that lasted), *Goodnight My Love* (the gentle later years), *The Prayer* (blessing and legacy, ending on his portrait). It is a starting point: open it, change anything, then Save. It comes from `suggested-shows.json`.
- **Fold a song:** click a song's colored bar to collapse its slides into it (click again to open). The arrow shows the state, **Collapse all songs / Expand all** are above the list, and the choice is remembered on that device. A folded song still shows its slide count and a marker if the current slide is inside it, and you can still drop a slide onto it.
- **Default sections:** the dancing, wedding, party, birthday-celebration and playful photos (36 of them, marked with `"song": 5` in `photos.json`) are in **In the Mood**; the other photos are shared across the remaining songs in order. Change any of it with Send to / drag, or edit the `song` values in `photos.json` to change the default for everyone.
- **Send to a song:** the ♪ button on any slide in the list, or **Send to…** at the top of the Slide tab, moves a slide into a song. You can also drag a slide into another song's section.
- **Now playing:** outside full screen, a bar under the slideshow shows the current song, its artist and the time within it (“Up next” on the opening slide, “Paused on” when paused).
- **Show** tab → **Songs:** turn the song timing on or off and change a song's length if your recording is a different length.

## Look

By default the transitions are shuffled randomly (never the same one twice in a row; each slide can be assigned its own). Older photos (before 1990, adjustable on the Show tab) get a Polaroid look and newer ones rotate through thin white, rounded white, gold frame and cream mat borders. Every photo sits over a blurred copy of itself, a slow Ken Burns zoom and drift, and a subtle vintage film finish (grain, vignette, warm tone). Photos are shown as large as fit the screen and are never cropped, and the Ken Burns motion never pushes a photo past the screen edge.

## Saving

Press **Save** at the top of the Edit menu to keep a version. Versions, and any pictures added, are stored in that person's own browser (localStorage plus a second IndexedDB copy; a small cookie lists the saved versions so the page can tell if browser data was cleared), and the slideshow opens as the most recently saved or opened version every time, even after a reload. Unsaved changes are not kept on reload. **Reset** throws away unsaved changes and goes back to the last saved version (or, if nothing is unsaved, back to the original, which is only kept if you press Save). Ctrl+S also saves. Each person sees their own version, and the original is never changed. Use **Download my version** (Slides tab) to back one up or move it to another device.

`photos/thumbs/` holds small previews used by the slide list.
