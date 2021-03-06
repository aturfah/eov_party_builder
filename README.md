# eov_party_builder
<h2>This repo contains two related projects</h2>
<ul>
<li>Etrian Odyssey 5 Party Builder</li>
<li>Skill Data FAQ</li>
</ul>

## Etrian Odyssey V Party Builder
### Details
<p>This is a tool built to allow people to plan out their parties, keeping track of the different damage types their party can deal, any binds/ailments, buffs/debuffs, and also different ways to heal. This tool is intended to, for example, see if you can inflict enough debuffs to consistently use Ephemeral Reap. In addition, this tool is meant to help identify which roles are already filled on a team so you can more easily see what new party members should invest in.</p>
<p>This is <b>not</b> meant to act as a skillsim; that has already been done. The tool will have the skill data availible, but will not keep track of SP allocated.</p>

### How to use
<p><b>Online</b>: <a href="https://aturfah.github.io/eov-party-builder/">https://aturfah.github.io/eov-party-builder/</a>
</p>
<p><b>Locally</b>: Download the repository and open /index.html in your favourite web browser.</p>

### Known Issues/Shortcomings
<p>See the issues section of the repository.</p>

## Scraper

> Feel free to use the scraper for your own projects, but please attribute it back to this repo.

<p>The data for this tool comes from HououinMakise's <a href="https://www.gamefaqs.com/3ds/893659-etrian-odyssey-v-beyond-the-myth/faqs/75200">guide</a> on GameFAQs. Initially I was going through the FAQ by hand and typing the information into the data.js file, but soon found it to be tedious and time-consuimg. So, the scraper got built. It parses the HTML files from the FAQ (need to be saved to a local directory), and outputs json file with the skill data. This data includes:</p>
<ul>
<li>Classes and Specializations</li>
<li>Skill Name</li>
<li>Description</li>
<li>Level progression data</li>
</ul>

### How to use
<b>Requires:</b> Python, BeautifulSoup
<ol>
<li>Make sure to change the directory in `mypath` to wherever you have the html files stored (denoted with the `# CHANGE ME` comment) </li>
<li>In addition, set the output file (denoted with the `# CHANGE ME` at the bottom of the scraper.py file) to the location you want the output to be.</li>
<li>Run `python scraper.py`, which should output the file as desired.</li>
</ol>

### Known Issues
<p>Known issues/shortcomings include not dropping \t and \n from the data, and also the Necromancer pages don't come out super clean so that needs to be manually cleaned. In addition, any other information (binds, damage types, etc) also needs to be manually imported.</p>
