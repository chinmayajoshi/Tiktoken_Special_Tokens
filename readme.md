# Tiktoken Token Analysis Notebooks

Jupyter notebooks for analyzing [OpenAI's tiktoken tokenizer](https://github.com/openai/tiktoken), focusing on special tokens and pattern matching.

## Notebooks

### special_tokens.ipynb
- Shows special tokens for different OpenAI models
- Explores model-to-encoding mappings
- Examines tiktoken extensions

### pattern_matching_tokens.ipynb  
- Analyzes tokens matching specific patterns like:
 - Tokens with `<|...|>` and `<...>` syntax
 - Sequences of dots, hashes, and underscores

## Setup
```bash
pip install tiktoken
```

## Key Findings
The GPT-4 tokenizer contains approximately 100,277 tokens. Notable findings include:
### Special Tokens

- `<|endoftext|>` (ID: 100257)<br>
- `<|fim_prefix|>` (ID: 100258)<br>
- `<|fim_middle|>` (ID: 100259)<br>
- `<|fim_suffix|>` (ID: 100260)<br>
- `<|endofprompt|>` (ID: 100276)<br>

### Pattern Tokens
The tokenizer includes various single tokens for:

Repeated sequences of dots (e.g `.`, `...`, `....`, etc.)<br>
Repeated hash symbols (e.g. `##`, `###`, etc.)<br>
Repeated underscores (e.g. `__`, `___`, etc.)<br>
Special bracket patterns (e.g. `<?>`, `<()>`, `<?>>` etc.)<br>