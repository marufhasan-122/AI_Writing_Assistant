# AI Writing Assistant

A simple AI-powered writing assistant built with Python and Hugging Face Transformers.  
It can:
- Check grammar and spelling
- Suggest better vocabulary
- Provide paraphrases
- Adjust tone (formal or informal)

---

## Tools Used

| Tool / Library | Purpose |
|----------------|---------|
| `transformers` (T5 model) | Generate paraphrases and tone-adjusted text |
| `nltk` | Tokenization, POS tagging, and WordNet synonyms for vocabulary suggestions |
| `language_tool_python` | Grammar and spelling correction |
| `torch` | Runs T5 model efficiently on CPU/GPU |
| Google Colab | Notebook environment for running the assistant interactively |

---

## Features & Usage

1. **Grammar Check** → Automatically corrects spelling, punctuation, and common errors.  
2. **Vocabulary Suggestions** → Suggests alternative words using WordNet synonyms.  
3. **Paraphrasing** → Generate multiple ways to rephrase a sentence or paragraph.  
4. **Tone Adjustment** → Modify text to be formal or informal.

### Example Usage

```python
text = "i dont know what to write. this is not good english and it seem wrong."
options = {"paraphrase": True, "paraphrase_count": 2, "tone": "formal", "vocab_suggest": True}

output = decide_and_run_agent(text, request_options=options)

print("Original:", output["original"])
print("Grammar-corrected:", output["grammar"]["corrected"])
print("Vocabulary suggestions:", output["vocabulary_suggestions"])
print("Paraphrases:", output["paraphrases"])
print("Tone variations:", output["tone_variations"])
```
### Sample Output:
Original: i dont know what to write. this is not good english and it seem wrong.

Grammar-corrected: I don't know what to write. This is not good English and it seems wrong.

Vocabulary suggestions: {'write': ['compose', 'pen', 'indite'], 'good': ['estimable', 'honorable']}

Paraphrases: ['I am unsure what to write. This sentence is not proper English.', ...]

Tone variations: ['I am unsure what to write. This sentence is not proper English and appears incorrect.', ...]
