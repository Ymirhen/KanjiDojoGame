# Marugoto Kanji Dojo

Kanji drawing practice, 10,000 rewrite sentences and pop quizzes for the kanji in
まるごと 入門 A1 りかい and 初級1 A2 りかい. One static page, no build step, no server.

## Put it on GitHub Pages

1. Create a repository (public, or private on a plan that allows Pages) and push these files
   to its default branch: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`.
2. In the repository: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   branch `main`, folder `/ (root)`. Save.
3. After a minute the app is at `https://<your-user>.github.io/<repo>/`.
   On a phone, open it in the browser and use "Add to Home Screen"; it then works offline too.

## Keeping progress in sync between phone and PC

Progress is saved in the browser automatically. To share it across devices, open
**Progress → Settings → Sync between devices with a GitHub Gist**, and paste a
fine-grained personal access token that has only the **Gists: read and write** permission
(GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens).
The app stores your progress in one secret gist named `kanji-dojo-progress.json` and merges
by "newest wins". The token never leaves your browser. Do the same on each device.

Without a token you can still move progress by hand with Export / Import.

## Updating the app

Replace `index.html` and bump `CACHE` in `sw.js` (for example `kanji-dojo-v2`) so installed
copies pick up the new version.

## Credits

- Stroke data: [hanzi-writer-data-jp](https://github.com/chanind/hanzi-writer-data-jp), derived from
  [animCJK](https://github.com/parsimonhi/animCJK) (LGPL) and Make Me a Hanzi / Arphic Public License.
- Handwriting recognition and stroke animation: [Hanzi Writer](https://github.com/chanind/hanzi-writer) (MIT).
- Kanji selection follows the lesson tables of the Marugoto coursebooks (The Japan Foundation).
  The practice sentences were generated from each unit's grammar patterns and vocabulary.
