# Mouse House — Incremental Build Prompts

Feed these to Copilot one at a time, in order. Each builds on the previous.
Wait for each to complete before sending the next.

---

## Prompt 1: Scaffold + Core Engine
Create the file C:\Users\rmauceri\mousehouse\index.html with just the foundation: HTML structure, CSS styling (warm cozy palette, responsive layout), canvas setup, game loop, title screen with "Mouse House" and a "click to start" prompt. Use a warm color scheme (soft browns, creams, warm grays). Include the CONFIG object with mouse names (Shadow/Cloud), twin names (Nico/Rose), and birthday message. Include the save/load system using LocalStorage. No rooms, no mice, no gameplay yet — just the shell that everything else plugs into. The HUD should have placeholders for coins, room tabs, shop button, games button, and letter button but they don't need to work yet.

## Prompt 2: Rooms + Warm Visuals
Add 3 rooms to the existing index.html: Bedroom, Kitchen, Living Room. Render them as a cozy cross-section cutaway with warm colors — soft purple/lavender for bedroom, warm green/sage for kitchen, warm orange/brown for living room. Add visual depth: a window with stars/moonlight, baseboards, subtle wall texture, ambient floating dust particles. Add working room-switching tabs in the HUD. Make it look like a charming little dollhouse.

## Prompt 3: Mouse Sprites + Basic Movement
Add the two mice (Shadow = dark grey, Cloud = light grey) to the existing index.html. Draw them as cute, expressive pixel-art sprites (~24px tall) with big round ears, tiny pink noses, and long tails. They should have idle animation (gentle breathing/bobbing), walking animation (legs moving, body bouncing), and sleeping animation (curled up with zzz). Basic AI: randomly pick idle/walking/sleeping states, walk to random positions within the current room, occasionally switch rooms. Show their name and current state at the bottom of the screen.

## Prompt 4: Mouse Personality + Speech Bubbles
Enhance the mice in index.html with personality and speech bubbles. Shadow is the chaotic gremlin (more likely to get zoomies, more sarcastic quotes). Cloud is the chill one (more likely to sleep, wholesome quotes). Add speech bubbles that pop up every 8-15 seconds with gen-Z meme-y one-liners like "no thoughts head empty", "this is giving cozy", "bestie wake up", "living my best cheese life", "slay", "it's giving... mouse", "not me napping again", "caught in 4k 📸". When both mice are in the same room, add interactions: they nuzzle, play-chase each other, or one judges the other. Add a click/tap-to-pet feature — clicking a mouse makes hearts float up and they squeak-emote.

## Prompt 5: Furniture System + Placement
Add the furniture/decoration system to index.html. Define 20 items as data (matchbox bed, thimble cup, bottle-cap plate, fairy lights, tiny laptop, yoga mat, "Live Laugh Cheese" sign, sourdough starter, ring light, cardboard couch, spool table, eraser TV, ethernet jump rope, cork stool, tiny plant, disco ball, sus beanbag, cheese wheel, stamp painting, tiny hoodie rack). Each item has an emoji icon, name, funny ironic description, price in cheese coins, grid size, and a color. Render placed items in rooms with shadows and depth. Add tap-to-place mode: when activated, show a grid overlay, tap a cell to place the item. Add remove mode. Make mice react to placed furniture — walk over to new items curiously, then do the associated behavior (laptop = doomscrolling, bed = sleeping, yoga mat = yoga poses, etc).

## Prompt 6: Shop UI (Moustazon)
Add the Moustazon shop to index.html. It's an HTML overlay modal with a grid of purchasable items showing their emoji, name, ironic description, and price. Items you already own show as "Owned — tap to place". Include a "Loot Crumbs" button (free mystery box that gives a random unowned item). The shop header should say "Moustazon Prime™" with the tagline "Free 2-day delivery to any mouse hole". Show current coin balance. Wire up buying (deducts coins, adds to owned), and tapping owned items enters placement mode.

## Prompt 7: Happiness + Goals System
Add a mouse happiness system to index.html. Show a small heart meter in the HUD. Happiness increases when you pet mice, place new furniture, or play mini-games. It slowly decreases over time (very slowly — this shouldn't be stressful). Add a simple goals/wishes system: occasionally a mouse says something like "Shadow wants a cozy bed 🛏" or "Cloud is craving cheese 🧀" — if you place that item, bonus coins and happiness. Show 1 active goal at a time in the HUD.

## Prompt 8: Mini-game — Cheese Chase
Add the Cheese Chase mini-game to index.html. It's a simple endless runner: the player controls a mouse (Shadow) moving up/down to dodge obstacles (mousetraps, cats) and collect cheese. On phone: drag finger to move. On PC: arrow keys or mouse position. Speed increases over time. Display score (cheese collected) and distance. When you hit an obstacle, game over — show results and award coins (2x cheese collected). Use warm colors consistent with the rest of the game.

## Prompt 9: Mini-game — Doomscroll
Add the Doomscroll mini-game to index.html. It's an HTML overlay: show social media posts one at a time. Each has a username and post text. The player taps "Like ❤️" or "Skip ⏭". Good posts (about mice, cheese, wholesome stuff) should be liked. Bad posts (cringe, ratio, sigma grindset) should be skipped. Correct = +3 coins. Wrong = strikes (3 strikes = game over). Show 10 posts per round. Include at least 10 good and 10 bad posts with gen-Z humor. Award coins at the end.

## Prompt 10: Birthday Event + Polish
Add the birthday event and final polish to index.html. On first load: auto-place a party banner and birthday cake in the living room, give 100 bonus coins, put party hats on the mice, show a toast "Happy Birthday Nico & Rose!". The 💌 button opens a letter overlay with a personal message from Dad (use CONFIG.birthdayMessage). Add coin-earning animations (coins float up when earned). Make sure all systems work together, save/load preserves everything, and the game is responsive on both phone and desktop.
