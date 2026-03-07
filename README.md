# Portfolio Templates

A collection of self-contained, single-file portfolio templates. Each one is a standalone `index.html` — no build step, no dependencies to install. Pick a style, fill in your details, and ship.

Live gallery: **[kickash.github.io/portfolio-templates](https://kicka5h.github.io/portfolio-templates)**

---

## Templates

### Available

| Template | Description | Tags |
|---|---|---|
| **Simple Responsive** | Clean, minimal layout with scroll animations, a typewriter hero, and a warm orange accent. | Minimal · Animated · Light |
| **Quirky Colorful** | Playful desktop-OS aesthetic with draggable windows and bold neo-brutalist cards. | Playful · Colorful · Fun |
| **Fantasy Character** | TTRPG character sheet aesthetic — your skills as stats, your projects as quests. | Funny · Quirky · Playful |
| **Arcade Game** | Pixel art Asteroids-style shooter where your portfolio *is* the game. Fly between sections, destroy enemies. | Game · Pixel Art · Interactive |
| **Terminal Session** | Colorful terminal emulator with keyboard navigation, command history, tab-autocomplete, and a typewriter output effect. | Terminal · Colorful · Keyboard |

### Coming Soon

| Template | Description |
|---|---|
| **Minimal Dark** | Sleek dark-mode portfolio with subtle glow effects and refined micro-interactions. |
| **Creative Bold** | High-contrast layout with oversized typography and an asymmetric project grid. |
| **Clean Classic** | Timeless two-column layout with elegant serif typography and generous whitespace. |

---

## Customising a Template

Every template has a clearly marked data section at the top of its `<script>` block — usually a `const P = { ... }` object. Fill in your name, role, bio, skills, projects, and contact info there. No other files to touch.

```js
const P = {
  name:  'Your Name',
  role:  'Full Stack Developer',
  // ...
};
```

---

## Adding a New Template

1. Create a folder under `docs/` — e.g. `docs/My-Theme/`
2. Add a single `index.html` inside it
3. Register it in `docs/index.html` by adding an entry to the `TEMPLATES` array:

```js
{
  id:        'my-theme',
  name:      'My Theme',
  path:      'My-Theme/index.html',
  desc:      'One sentence description.',
  tags:      ['Tag1', 'Tag2'],
  accent:    '#hexcolor',
  available: true,
},
```

The gallery will automatically render a live iframe preview and link to the full page.

---

## Structure

```
docs/
├── index.html              # Gallery page
├── Simple-Responsive/
│   └── index.html
├── Quirky-Colorful/
│   └── index.html
├── Fantasy-Character/
│   └── index.html
├── Arcade-Game/
│   └── index.html
└── Terminal-Session/
    └── index.html
```

---

## Running Locally

No build step needed. Serve the `docs/` folder with any static server:

```bash
npx serve docs
# or
python3 -m http.server --directory docs
```

Then open `http://localhost:3000` (or whichever port the server uses).
