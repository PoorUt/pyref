# 🐍 Python Libraries — Reference Tree

A clean, interactive reference site for popular Python libraries. Each library is documented as a collapsible API tree so you can explore modules, classes, functions, and attributes at a glance — without digging through official docs.

**Live site →** https://PoorUt.github.io/pyref/

---

## Libraries Included

| Library | File | Topics |
|---|---|---|
| 🔢 NumPy | `numpy_tree.html` | Arrays, linear algebra, FFT, random, broadcasting |
| 🐼 Pandas | `pandas_tree.html` | DataFrames, groupby, merging, time series, IO |
| 🤖 Scikit-learn | `sklearn_tree.html` | ML algorithms, pipelines, metrics, cross-validation |
| 📊 Matplotlib | `matplotlib_tree.html` | Figures, axes, colormaps, animations, pyplot |
| 🌊 Seaborn | `seaborn_tree.html` | Statistical plots, themes, distributions, facet grids |
| 🔥 PyTorch | `pytorch_tree.html` | Tensors, autograd, nn modules, optimizers, CUDA |
| 🔗 AI & Scientific Stack | `lang Chain, Sci py, Google ADK, Lang Graph.html` | LangChain, SciPy, LangGraph, Google ADK |

---

## Features

- **Interactive home page** — dots respond to your mouse like a gravitational black hole
- **White + dotted grid theme** across all pages
- **Search & filter** within each library tree
- **Expand / Collapse All** controls on every page
- **← Home** button on every library page
- **Data-driven** — home page renders from a simple JavaScript array, no server needed

---

## Adding a New Library

1. Add your new `.html` file to the root of this folder
2. Open `index.html` and find the `LIBRARIES` array near the top of the `<script>` block
3. Add a new entry:

```js
{
  icon: "🧪",
  name: "Your Library Name",
  libs: "import-name",
  desc: "One sentence describing what the library covers.",
  file: "your_file.html",
  accent: "#6366f1",       // card accent color (hex)
  accentLight: "#e0e7ff"   // lighter tint for hover border
},
```

4. Save — the card appears on the home page instantly.

> Pick any hex color you like for `accent`. A good pairing is a vivid mid-tone for `accent` and a pale tint of the same hue for `accentLight`.

---

## Running Locally

Because the home page uses a JavaScript array (no `fetch`), you can open `index.html` directly in any browser:

```
# Option 1 — just double-click index.html

# Option 2 — serve with Python (recommended, avoids any browser quirks)
cd "Python Lib Tree"
python -m http.server 8000
# then open http://localhost:8000
```

---

## Hosting on GitHub Pages

1. Push all files to a **public** GitHub repository
2. Go to **Settings → Pages**
3. Set source to **Deploy from a branch → main → / (root)**
4. Your site goes live at `https://your-username.github.io/your-repo-name/` within ~60 seconds

---

## File Structure

```
.
├── index.html                                  # Home page (data-driven, blackhole effect)
├── libraries.json                              # Library metadata reference
├── numpy_tree.html
├── pandas_tree.html
├── sklearn_tree.html
├── matplotlib_tree.html
├── seaborn_tree.html
├── pytorch_tree.html
└── lang Chain, Sci py, Google ADK, Lang Graph.html
```

---

## Tech Stack

Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build step, no dependencies.
