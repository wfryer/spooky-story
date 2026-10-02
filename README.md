🎃 Spin a Spooky Story

A triple spinning wheel tool that randomly rolls a Character, a Setting, and a Plot into a complete spooky story starter — sparking creative writing, Scratch animations, and classroom storytelling.

Originally built to replace SpinTheWheel.io's "Spin a Spooky Story" wheel (created by Tony Vincent at shapegrams.com) after our school network blocked spinthewheel.io. This version runs entirely offline as a single HTML file, no dependencies, no login, and no internet required after the initial Google Fonts load.

View and use this code / spinner on this GitHub webpage

🎮 How to Use
Open spooky-story-spin.html in any modern web browser.
Click ✦ Spin All Three ✦ to spin all the wheels at once, or use the individual 🎃 Spin buttons under each wheel.
When all three wheels land, your combined Spooky Story Result sentence appears at the bottom, for example: "A whining witch, in a corn maze, kissed a frog."
Click 📋 Copy Story Result to copy that sentence straight to your clipboard, ready to paste into your Scratch project's Notes and Credits.
Not happy with one wheel's result? Click ✕ Remove & Re-spin under that wheel to clear just that one and try again.
Click ↺ Reset Everything to start completely fresh.
✏️ Customizing the Wheels

All customization happens in the <script> section near the bottom of the HTML file. Look for the clearly marked CONFIGURATION block — you don't need to touch anything else.

Changing an existing item

Each wheel item looks like this:

js
{ name: "a whining witch", color: "#cc5500" },
name — The label shown on the wheel, and the exact phrase used in the final story sentence. Write it so it reads naturally as "Character, Setting, Plot." (e.g. a character phrase, a setting phrase starting with a preposition like "in" or "while," and a plot phrase that reads like the end of a sentence).
color — A hex color code for that slice. Any valid CSS hex color works.
Adding a new item

Copy any existing line and paste it inside the same array (wheel1Items, wheel2Items, or wheel3Items), then edit the name and color values.

Removing an item

Delete the line (including the trailing comma) for any item you want to remove.

Changing wheel titles

Search for Character, Setting, and Plot in the HTML (inside the wheel-title divs) to rename any wheel.

🎨 Customizing the Look

Near the top of the <style> block you'll find a :root section with CSS variables:

css
:root {
  --bone:         #f3ead3;   /* main background color of panels */
  --pumpkin:      #ff7518;   /* primary accent (headings, buttons) */
  --witch:        #7b2cbf;   /* secondary accent (character wheel, Spin All button) */
  --slime:        #7cb518;   /* tertiary accent (plot wheel, copy button) */
  --ink:          #241433;   /* main text color */
}

Adjust these to completely re-theme the page without hunting through the CSS.

📚 Classroom Ideas
Activity	Description
Spooky Scratch Story	Spin all three, then build a Scratch animation that tells the resulting story with sprites, speech bubbles, and sound
Story Swap	Spin once as a class, then have every student write their own 3-sentence version of the same prompt
Illustrate It	Draw or collage a single scene from your spun story
Sequel Spin	Spin again for "What happened next?" and continue the story
Genre Remix	Spin, then rewrite the same Character/Setting/Plot as a comedy instead of a spooky story
🛠 Technical Notes
Single file — everything is self-contained in one .html file (HTML + CSS + JS)
No frameworks — vanilla JavaScript with HTML5 Canvas for the wheels
Fonts — loads Creepster and Baloo 2 from Google Fonts on first use; works offline otherwise with system font fallbacks
No server needed — open directly from your file system
Clipboard copy — uses the browser's Clipboard API; if a browser blocks it, the result text is still fully visible to select and copy by hand
Tested in Chrome, Firefox, Safari, and Edge
📁 File Structure
spooky-story-spin.html   ← the entire app, one file
README.md                ← this file
🙏 Credits
Story structure and most wheel content adapted from Tony Vincent's "Spin a Spooky Story" wheel
Built from the same codebase as wfryer/creature-spin, another classroom spinning-wheel tool
Built as a classroom tool for a middle school Computer Programming Scratch unit
Created with assistance from Claude (Anthropic)
📄 License

Feel free to use, modify, and share this freely for educational purposes. A credit link back is appreciated but not required.
