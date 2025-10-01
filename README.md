# Lakoff Lens (Rhetoric & Framing Analyzer)

> A prototype AI workflow that analyzes political text for **sentiment** and **metaphorical framing**, inspired by George Lakoff’s work on conceptual metaphors.

---

## Demo
🎥 [Watch the Loom demo](https://www.loom.com/share/f34e4e9244334cc59e138f54d33221c5?sid=64444e61-fe79-43fd-aaa6-db3e02579fdf)


## Run the Agent
👉 Want to try it yourself?  
[Run Lakoff Lens in MindStudio](https://app.mindstudio.ai/agents/rhetoric--framing-analyzer-18659ffe)  

*(MindStudio account required )*  


## Remix the Workflow
🔧 Interested in customizing this workflow for your own use?  
[Remix in MindStudio](https://app.mindstudio.ai/agents/rhetoric--framing-analyzer-18659ffe/remix)  

*(Requires MindStudio account. Remix lets you fork this workflow into your own workspace.)*  

---

## Why I Built It
This project started as an experiment in applying AI to **qualitative research methods**.  
The goal was to see if an agent could:  
- Tag **sentiment** (positive / neutral / negative)  
- Identify **metaphorical framing** (e.g., War, Journey, Family, Marketplace, etc.)  
- Provide structured outputs usable for research databases **and** human-friendly views.  

---

## Features & Stack
- Input: any political text (article, speech, transcript snippet)  
- **MindStudio workflow** with two stages:  
  1. **Analysis block** → JSON output (quotes, metaphors, sentiment, analysis notes, confidence, character spans)  
  2. **Formatter block** → Markdown for human-friendly display  
- Outputs both **structured JSON** and **formatted Markdown**  
- JSON fields include:  
  - `document_sentiment` (overall)  
  - `findings` (quotes, metaphors, sentiment, analysis, confidence, spans)  

---

## Sample Outputs

### JSON Output
```json
{
  "document_sentiment": "Negative",
  "findings": [
    {
      "quote": "the Supreme Court just made that task exceedingly difficult",
      "metaphors": ["Obstacle/Barriers"],
      "sentiment": "Negative",
      "analysis": "The phrase frames the situation as a barrier, emphasizing obstacles faced by Congress.",
      "confidence": "High",
      "char_span": [424, 460]
    },
    {
      "quote": "the Republican justices bear as much blame for that dysfunction as anyone",
      "metaphors": ["War/Conflict"],
      "sentiment": "Negative",
      "analysis": "This frames politics as conflict, with justices cast as combatants in a struggle.",
      "confidence": "High",
      "char_span": [960, 1005]
    }
  ]
}
```
### Markdown View

**Overall sentiment:** Negative  

| # | Quote | Metaphors | Sentiment | Confidence |
|---|-------|-----------|-----------|------------|
| 1 | “the Supreme Court just made that task exceedingly difficult” | Obstacle/Barriers | Negative | High |
| 2 | “the Republican justices bear as much blame for that dysfunction as anyone” | War/Conflict | Negative | High |

**1.** “the Supreme Court just made that task exceedingly difficult”  
→ Frames the problem as a barrier, stressing the difficulty of progress.  

**2.** “the Republican justices bear as much blame for that dysfunction as anyone”  
→ Uses conflict framing, casting justices as adversaries and assigning blame.  


## Limitations
- Prototype only — not benchmarked or systematically evaluated
- May over- or under-identify metaphors
- Works best on short- to medium-length political texts

⚠️ Note: Running this agent requires a MindStudio account.  
If you’d like to try this workflow directly in MindStudio, here’s my referral link:  
[Run in MindStudio](https://get.mindstudio.ai/0wp8cavjwegg-8drt) (referral link, requires account) 
