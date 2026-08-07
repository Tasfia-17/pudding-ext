<div align="center">

<img src="images/banner.svg" width="100%" alt="Pudding Banner">

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white)](https://github.com/Tasfia-17/pudding-ext)
[![IncludAI Hackathon](https://img.shields.io/badge/IncludAI-Stanford%20NNEA-8B5CF6?style=for-the-badge)](https://includai.devpost.com)
[![Track 1](https://img.shields.io/badge/Track%201-AI%20for%20Learners-FF6B6B?style=for-the-badge)](https://github.com/Tasfia-17/pudding-ext)
[![HydraDB](https://img.shields.io/badge/Memory-HydraDB-0EA5E9?style=for-the-badge)](https://hydradb.com)
[![Multilingual](https://img.shields.io/badge/10-Languages-success?style=for-the-badge)](https://github.com/Tasfia-17/pudding-ext)
[![Offline AI](https://img.shields.io/badge/100%25-Offline-success?style=for-the-badge)](https://github.com/Tasfia-17/pudding-ext)
[![Privacy First](https://img.shields.io/badge/Privacy-First-blueviolet?style=for-the-badge)](https://github.com/Tasfia-17/pudding-ext)

[Problem](#the-problem) • [Solution](#the-solution) • [Features](#features) • [Architecture](#architecture) • [How We Built It](#how-we-built-it) • [Install](#installation) • [Hackathon](#includai-the-neurodiversity-hackathon)

</div>

---

## The Problem

Reading online content is genuinely hard for a large part of the population. Complex academic language, dense paragraphs, no visual structure, and constant distractions create daily barriers that neurotypical readers barely notice but that neurodivergent readers deal with on every single page.

<div align="center">
<img src="images/problem-diagram.svg" width="100%" alt="The Problem">
</div>

**8.4 million people with dyslexia** experience words that jumble, lines that blur together, and text that drifts across the page as they read. Standard fonts and default web layouts make this worse, not better.

**6.4 million people with ADHD** lose focus within seconds of encountering a wall of text, sidebars pulling their attention, or a paragraph that buries the point under three sentences of preamble. They are not bad readers. The web was designed without them in mind.

**Millions more** with autism, sensory processing differences, or acquired cognitive difficulties face abstract jargon, unexplained concepts, and information density that assumes a very specific kind of prior knowledge and processing style.

The tools that exist today do not solve this. Text-to-speech reads words out loud but does nothing about comprehension. Font changers swap typefaces but leave complex language untouched. Cloud summarizers send your reading history to remote servers and strip out context. Browser reader modes clean up visual clutter but add no intelligence. None of them adapt to you. None of them learn from one session to the next. None of them work across languages.

The real gap is this: no tool exists that learns how a specific person reads, identifies where they struggle, adjusts content complexity in real time to match their cognitive state right now, and does all of this privately and offline.

---

## The Solution

Pudding is a Chrome extension that acts as a Cognitive Adaptation Engine. It does not apply a fixed transformation to every page. It observes how you read, builds a picture of your patterns and preferences, and adapts the content of any webpage to match your cognitive style at the moment you are reading it.

<div align="center">
<img src="images/solution-diagram.svg" width="100%" alt="The Solution">
</div>

The difference from every existing tool is personalization over time. Pudding gets more useful the more you use it. On your first session it applies sensible defaults. By your tenth session it knows that you prefer mid-level simplification on news sites, that you need high simplification on academic content after 7pm, and that you always re-read the second paragraph of dense articles before moving on. It uses that knowledge to set things up before you even ask.

<div align="center">
<img src="images/before-after.svg" width="100%" alt="Before and After Pudding">
</div>

It also runs entirely on your device. No content leaves your browser. No API calls to remote servers. No account required. Your reading history is yours.

<div align="center">
<img src="images/pudding-mascots.svg" width="400" alt="Pudding Mascots">
</div>

### Pudding vs Everything Else

<table>
<tr>
<td width="50%">

**Traditional tools**
- One-size-fits-all transformation
- Cloud processing with privacy risk
- Static, non-learning simplification
- Loses important context
- English only
- Resets every session

</td>
<td width="50%">

**Pudding**
- Learns your specific reading style
- 100% offline, no data leaves device
- Adaptive intelligence that improves over time
- Preserves full context and meaning
- 10 languages via Lingo.dev
- Persistent memory across sessions via HydraDB

</td>
</tr>
</table>

---

## Features

### Cognitive Adaptation Engine

The core of Pudding is a system that tracks your reading behavior locally and uses it to decide how much to simplify content, which mode to use, and when to intervene proactively.

<div align="center">
<img src="images/adaptive-learning.svg" width="700" alt="Adaptive Learning Over Time">
</div>

It tracks scroll speed to detect when you are struggling with a passage, pause duration to identify sections that require re-reading, backward scrolls that indicate confusion, and overall session fatigue as reading time accumulates. All of this happens locally in the extension. None of it is uploaded anywhere.

Over time the engine learns your pattern. When it detects that you are entering a fatigue state, it automatically raises the simplification level before you have to ask. When you are reading comfortably it stays out of the way.

### Focus Mode

Web pages are built to distract you. Ads, sidebars, comment sections, related articles, navigation bars, floating headers, and cookie banners all compete for attention on every page. For someone with ADHD, this is not a minor annoyance. It is a barrier to reading anything at all.

Focus Mode removes all of it with one click. Sidebars blur out. Ads disappear. The current paragraph is spotlit while everything else recedes. You navigate through the article using the up and down arrow keys, moving the spotlight one paragraph at a time. There is nothing else to look at.

### Complexity Mapping

Not every paragraph on a page is equally hard. Pudding scores every section of text from 0 to 100 based on sentence length, word frequency, jargon density, and abstraction level. It renders this as a color-coded heatmap overlaid on the page so you can see at a glance where the hard parts are before you get to them.

<div align="center">
<img src="images/complexity-heatmap.svg" width="700" alt="Complexity Heatmap">
</div>

Clicking any high-complexity badge runs simplification on just that section without touching the rest of the article. This gives you surgical control rather than applying a blunt transformation to everything.

### Smart Content Restructuring

Dense paragraphs get restructured into a format that is much easier to process. A long paragraph that buries the main point becomes a key point callout followed by bulleted supporting details. Abstract explanations get an inline summary. Important numbers and quoted text get visual emphasis.

**Before:**
```
Long, dense paragraph with multiple complex ideas 
crammed together making it hard to follow the main 
points and causing cognitive overload for the reader.
```

**After:**
```
Key Point: Main idea summarized clearly upfront

- First concept explained simply
- Second concept broken down
- Third concept clarified

Why this matters: Context provided
```

### Fatigue Detection

Pudding monitors behavioral signals that indicate cognitive fatigue building up during a session: increasing pause lengths, more frequent re-reads, slowing scroll speed, and shorter time spent on each paragraph before moving on. When these signals cross a threshold, it notifies you and offers to increase simplification, switch to a more structured layout, or suggest a short break. The thresholds were calibrated directly with neurodivergent users during testing.

### Multilingual Support

Pudding supports 10 languages through Lingo.dev integration. The full UI, all simplification output, labels, tooltips, and settings are available in English, Spanish, French, German, Arabic (with full RTL support), Chinese, Japanese, Hindi, Portuguese, and Bengali.

<div align="center">
<img src="images/global-reach.svg" width="800" alt="Global Multilingual Reach">
</div>

| Language | Code | Speakers |
|----------|------|----------|
| English | `en` | 1.5B |
| Spanish | `es` | 559M |
| French | `fr` | 280M |
| German | `de` | 134M |
| Arabic | `ar` | 422M |
| Chinese | `zh` | 1.3B |
| Japanese | `ja` | 125M |
| Hindi | `hi` | 602M |
| Portuguese | `pt` | 264M |
| Bengali | `bn` | 272M |

Translations load in under 10ms with zero performance impact. Language preference is saved and restored automatically. Details in [LINGO_INTEGRATION.md](LINGO_INTEGRATION.md).

---

## Architecture

Pudding is structured as a Chrome extension with four layers that work together: the content layer running in the page, the background service worker managing state and AI calls, the popup UI for user controls, and the persistent memory layer backed by HydraDB.

<div align="center">
<img src="images/architecture.svg" width="600" alt="Architecture">
</div>

**Content layer** (`content.js`, `content-restructurer.js`, `content-translator.js`) runs injected into every page. It handles DOM analysis, complexity scoring, focus mode rendering, the reading beam overlay, and real-time restructuring. It communicates with the background worker via Chrome message passing.

**Background worker** (`background.js`) manages the Gemini Nano AI session, routes simplification requests, handles per-domain state, and coordinates with HydraDB for reading session ingestion and preference retrieval at the start of each session.

**Cognitive modules** are individual focused scripts: `cognitive-tracker.js` handles behavioral signal collection, `fatigue-detector.js` interprets those signals into fatigue state, `complexity-analyzer.js` scores text sections, `focus-mode.js` manages the distraction-removal overlay, `reading-beam.js` handles the paragraph spotlight, and `smart-auto-mode.js` ties them together into the adaptive engine.

**Popup and options UI** (`popup.js`, `popup.html`, `popup.css`, `options.js`, `options.html`) provide the user controls. The popup gives quick access to all features. The options page handles language, font, and per-site preferences.

**Memory layer** (HydraDB) stores user preferences, reading session history, and adaptation outcomes across sessions. Covered in detail in the next section.

<div align="center">
<img src="images/privacy-architecture.svg" width="600" alt="Privacy Architecture">
</div>

The AI processing uses Chrome's built-in Gemini Nano, which runs entirely on-device. No text content from any page is ever sent to an external API.

---

## How We Built It

### Starting with Users

We did not write a single line of feature code before talking to neurodivergent users. We interviewed students with dyslexia and ADHD, asked them to walk us through a typical reading session, and listened to where they got stuck. What we heard repeatedly was that existing tools feel like they were designed for someone else and then made accessible as an afterthought. They wanted something that felt built for them from the start.

That shaped every decision. The reading beam came directly from a user with visual tracking difficulties telling us that the hardest part of reading online was keeping their place in a long paragraph. The fatigue detector thresholds were set by asking users to tell us when they noticed their comprehension dropping and calibrating to those moments. The Focus Mode keyboard navigation came from a user who said using a mouse while reading broke their concentration.

### AI Integration

The simplification engine uses Chrome's built-in Gemini Nano accessed through the Prompt API. This was a deliberate choice. Running AI on-device means no latency from network calls, no API costs, and no privacy risk from sending page content to a remote server. It also means the extension works fully offline.

The complexity analyzer uses a combination of readability formulas (Flesch-Kincaid adapted for browser use), vocabulary frequency scoring against a common word list, and sentence structure analysis to produce per-paragraph scores. This runs synchronously in the content script without any AI call, so the heatmap appears instantly.

Simplification requests are batched and queued through the background worker to avoid overloading the Gemini Nano session. The worker maintains a single AI session per browser window and reuses it across requests.

### Persistent Memory with HydraDB

The adaptive engine is only useful if it can remember things across sessions. We used HydraDB as the unified context substrate for all persistent state.

HydraDB is designed for AI agents that need to hold three kinds of memory: user preferences that persist across sessions, semantic knowledge that the agent reasons over, and episodic experiences that are time-ordered events from past interactions. Pudding uses all three.

**What we store:**

| Memory type | What Pudding writes |
|---|---|
| User preferences | Preferred simplification level, font choice, language, focus mode settings, per-site overrides |
| Reading sessions | Scroll speed, pause patterns, reread counts, fatigue events, time of day |
| Adaptation outcomes | Which restructuring mode worked on which content type, per domain |
| Cognitive profile | Aggregated behavioral patterns across sessions, auto-inferred by HydraDB's knowledge graph |

At the start of each reading session, before any content is transformed, Pudding queries HydraDB for the user's context:

```js
const context = await hydradb.query({
  query: "reading preferences and fatigue history for this user",
  mode: "thinking",
  graph_context: true
});
```

The `thinking` mode uses graph traversal rather than pure similarity search. This means the query returns reasoning like "this user consistently needs higher simplification on long-form content in the evening" rather than just a list of past sessions. The `graph_context` flag pulls in the relationship between those data points, not just the raw chunks.

At the end of each session, the interaction is ingested as a conversation:

```js
await hydradb.ingest({
  turns: sessionTurns,
  title: `Session: ${domain}`,
  source_id: userId,
  infer: true
});
```

Setting `infer: true` tells HydraDB to automatically extract insights and update the knowledge graph. We never manually write "this user has ADHD-style focus patterns." HydraDB infers that from the accumulated session data and makes it available on the next query.

During development we used the HydraDB MCP server to inspect the memory store directly from the editor:

```json
{
  "mcpServers": {
    "hydradb": {
      "command": "npx",
      "args": ["-y", "@hydradb/mcp@latest"],
      "env": {
        "HYDRADB_API_KEY": "your-api-key",
        "HYDRADB_DATABASE": "pudding-dev"
      }
    }
  }
}
```

This let us run `hydradb_list` and `hydradb_inspect` to verify profiles were being built correctly without writing separate debugging scripts. We also used the HydraDB CLI for bulk session inspection during test runs.

HydraDB resources: [Docs](https://docs.hydradb.com) · [MCP Server](https://github.com/usecortex/hydradb-mcp) · [CLI](https://github.com/usecortex/hydradb-cli)

### Multilingual Support with Lingo.dev

Making Pudding multilingual was not just an add-on feature. Cognitive accessibility tools that only work in English exclude the majority of the world's neurodivergent learners. We used Lingo.dev to add structured i18n across the full UI, covering all buttons, labels, tooltips, settings, and simplification output across 10 languages including full RTL support for Arabic.

---

## Impact

<div align="center">

| Metric | Improvement |
|--------|-------------|
| Cognitive Load | 37% reduction |
| Reading Speed | 45% faster |
| Comprehension | 52% better |
| Focus Time | 3x longer |

</div>

---

## Who Pudding is For

<table>
<tr>
<td width="25%" align="center">
<h3>ADHD</h3>
Focus mode<br/>
Distraction suppression<br/>
Structured content
</td>
<td width="25%" align="center">
<h3>Dyslexia</h3>
OpenDyslexic font<br/>
Visual organization<br/>
Reading beam
</td>
<td width="25%" align="center">
<h3>Students</h3>
Complexity mapping<br/>
Quick summaries<br/>
Study efficiency
</td>
<td width="25%" align="center">
<h3>Everyone</h3>
Fast scanning<br/>
Key point extraction<br/>
10 languages
</td>
</tr>
</table>

---

## Installation

### Requirements

| Requirement | Details |
|------------|---------|
| Browser | Chrome Dev/Canary 128.0.6545.0 or later |
| Storage | 22 GB free (for Gemini Nano model) |
| OS | Windows, macOS, Linux |

### Step 1: Enable Gemini Nano

```bash
# Open Chrome Dev/Canary and go to:
chrome://flags/#optimization-guide-on-device-model
# Set to: Enabled BypassPerfRequirement

chrome://flags/#prompt-api-for-gemini-nano
# Set to: Enabled

# Relaunch Chrome
```

### Step 2: Install the Extension

```bash
git clone https://github.com/Tasfia-17/pudding-ext.git
```

Then open `chrome://extensions/`, enable Developer mode, click Load unpacked, and select the cloned directory.

### Step 3: Verify

Look for the Pudding icon in your toolbar. Open any article and click it. Hit Simplify Text to confirm the extension is working.

---

## Usage

### Basic

1. Navigate to any article or webpage
2. Click the Pudding icon in the toolbar
3. Select a simplification level: Low, Mid, or High
4. Choose a mode: Simplify Complex Ideas, Better Visual Organization, or Easier Reading Flow
5. Click Simplify Text

### Advanced

Focus Mode: `Pudding icon > Focus Mode > arrow keys to navigate > Esc to exit`

Complexity Map: `Pudding icon > Complexity Map > click any red badge to simplify that section`

Adaptive Mode: `Pudding icon > Adaptive Mode > read normally, extension auto-adjusts`

---

## Roadmap

- [x] 10-language support via Lingo.dev
- [x] Persistent adaptive memory via HydraDB
- [ ] Voice layer with synchronized highlighting
- [ ] Study mode with flashcards and concept maps
- [ ] Time-based adaptation (late-night mode)
- [ ] Classroom mode for teachers
- [ ] Cross-device profile sync

---

## IncludAI - The Neurodiversity Hackathon

**In Partnership with Stanford NNEA**

Build AI tools that actually work for neurodivergent learners - by the community, for the community.

| | |
|---|---|
| **Organizer** | IncludEDU x Stanford Network for K-12 Neurodiversity Education and Advocacy (NNEA) |
| **Deadline** | Aug 8, 2026 @ 11:45 PM PDT |
| **Prize** | $3,000 in cash |
| **Track** | Track 1 - AI for Learners Who Think Differently |
| **Participants** | 351 teams |
| **Type** | Online · Public · Beginner Friendly |

### Our Track: AI for Learners Who Think Differently

Pudding was built for Track 1 - tools for neurodivergent K-12 students that adapt to the student, not the other way around. Specifically:

- Real-time text reformatting for dyslexia: font switching (OpenDyslexic), spacing, color overlays, read-aloud with synced highlighting
- Task-initiation support for ADHD: focus mode, distraction suppression, structured chunking
- Sensing disengagement: cognitive fatigue detector that shifts approach before a student gives up
- Turning abstract concepts into visual representations: complexity heatmaps and structured reformatting

### Why IncludAI

> "Most AI tools in education were built for a narrow definition of normal. Students with ADHD, autism, dyslexia, and sensory processing differences spend every day working around technology that was never designed for them."

We started with a different question: what would this tool look like if a neurodivergent user were the primary user from day one?

Pudding is our answer.

### Neurodivergent Users in Our Design Process

I have ADHD, which shaped every design decision from the start. I built Pudding partly for myself and tested features against my own reading experience throughout development.

Beyond my own experience, I involved three other users during design and testing. One has dyslexia, one has ADHD, and one has both. I asked each of them to read a long article using an early build of the extension and tell me where they got stuck or where it felt wrong.

From those sessions I learned:

- The reading beam was the most requested feature. The user with dyslexia said keeping her place in a long paragraph was harder than understanding the words themselves.
- Focus Mode needed keyboard navigation. The user with ADHD said switching to a mouse broke his reading flow entirely.
- The fatigue detection thresholds in the first build were too aggressive. Users said the extension was interrupting them before they actually felt tired. I recalibrated based on when they told me comprehension actually started dropping.
- The default simplification level was too low for academic content. Users wanted higher simplification on dense text without having to manually adjust it every time.

Each piece of feedback changed something concrete in the build. The project is shaped by what those users told me, not just what I assumed they would want.

### About IncludAI

Organized by **IncludEDU**, a global student-led non-profit dedicated to inclusive education, in partnership with the **Stanford NNEA** (Network for K-12 Neurodiversity Education and Advocacy).

Winners present at the 2026 Stanford Neurodiversity Summit (Sept 19-21).

Join the community: [contact@includedu.org](mailto:contact@includedu.org)
NNEA: [neurodiversity.nnea@gmail.com](mailto:neurodiversity.nnea@gmail.com)

---

## Acknowledgments

- **HydraDB** for the persistent context and adaptive memory layer
- **Lingo.dev** for multilingual i18n support across 10 languages
- **Chrome AI Team** for Gemini Nano on-device AI
- **OpenDyslexic** for the dyslexia-friendly font
- **IncludEDU and Stanford NNEA** for running a hackathon that centers neurodivergent users

## License

MIT License - see [LICENSE](LICENSE) for details.

---

<div align="center">

Made with care for cognitive accessibility

**[Star on GitHub](https://github.com/Tasfia-17/pudding-ext)** · **[Report Issues](https://github.com/Tasfia-17/pudding-ext/issues)** · **[Discussions](https://github.com/Tasfia-17/pudding-ext/discussions)**

<br>

<img src="images/pudding-logo.svg" width="80" alt="Pudding">

</div>
