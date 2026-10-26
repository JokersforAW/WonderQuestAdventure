# WonderQuest — Paper Adventure
A static, offline-ready atlas with 14 illustrated wonders.

## Open locally
Extract the ZIP completely and open index.html in Chrome or Edge. Keep css/, js/ and assets/ beside index.html. No installation, account, API key, or build step is needed.

## Publish with GitHub Pages
1. Create a public GitHub repository (for example wonderquest).
2. Extract this ZIP, then upload its CONTENTS to the repository. index.html must be at the repository root, beside css/, js/ and assets/. Do not upload only the ZIP.
3. Commit the files to main.
4. Open Settings → Pages → Build and deployment.
5. Set Source to Deploy from a branch. Choose main and /(root), then Save.
6. Wait for GitHub's deployment to complete; use the URL shown in Pages to share your game.

Official guide: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Play
- Choose New Seven Wonders or Ancient Wonders.
- Explore: select map illustrations or tray entries. Field notes collect a passport stamp.
- Place the pin: drag a token or tap a location. Adjust it, then check. Seven rounds; up to 7,000 points. Hints are free.
- Discovery quiz: seven shuffled questions and answers with explanations, one per landmark.
- My passport: tap a collectible card to flip between artwork and facts.
- Drag to pan; wheel or +/- to zoom; home resets the view.
- Keyboard: tab to the map; arrow keys move a crosshair, Shift increases the step, Enter places the guess. Buttons support keyboard use.
- On phones, tap the panel heading to collapse it and expose more map.

## Edit the project
index.html — page structure
css/style.css — layout, paper style and responsive rules
js/data.js — embedded Natural Earth geography and both landmark collections
js/game.js — map, gameplay, quizzes and passport interactions
js/vendor.js — locally bundled D3 and TopoJSON
assets/modern-0.png ... modern-6.png — new wonders
assets/ancient-0.png ... ancient-6.png — ancient reconstructions
CREDITS.md — sources, attribution and third-party licence text

## Scoring and historical uncertainty
Distance uses great-circle distance on a spherical Earth (radius 6,371 km).
Points = round(1000 × exp(-distance_km / 2000)).
Pins approximate landmark sites; the Great Wall pin represents Mutianyu.
Hanging Gardens uses a conventional Babylon reference point; its existence and location are disputed.
Colossus uses a representative Rhodes harbour point; its precise original location is unknown.
Ancient artworks are imaginative reconstructions, not archaeological evidence. Countries use modern names.
Nearby landmarks are visually spread with leader lines; the small anchor dot is the geographic location.

## Privacy and availability
Exploration progress stays in this browser's localStorage; it is not an online account or shared leaderboard.
If storage is blocked, the game still works without persistent stamps.
All running assets are bundled. External source links need internet.
This package is ready to deploy but has not been uploaded to your GitHub account.

## Validation
Browser tested in installed Chrome at 1440×960 and 390×844:
both full pin-placement games (7,000/7,000 at exact reference points),
both full quizzes (7/7), passport flips, token drag placement,
keyboard placement, pan without changing guesses, and collection switching.
No JavaScript page errors observed. Mobile layout tested using browser emulation, not a physical phone.
