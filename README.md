---
license: apache-2.0
language:
- en
- ru
base_model:
- openai-community/gpt2
library_name: transformers
---
---
license: mit
library_name: transformers
language: en
tags:
  - gpt2
  - morse-code
  - text-to-morse
  - tars-humor
  - mini-llm
  - fine-tuned
---

<!-- markdownlint-disable first-line-h1 -->
<!-- markdownlint-disable html -->
<!-- markdownlint-disable no-duplicate-header -->

<div align="center">
  <h1>Morsent-128T</h1>
  <p><i>Compact GPT-2 model for Morse code translation, decoding, and sci-fi humor — all in 128 tokens or less.</i></p>
  <img src="https://media.githubusercontent.com/media/MayaDispeler/Morsent-128-Mini/main/morsent-banner.png" width="70%" />
</div>

---

## 🧠 About the Model

**Morsent-128T** is a tiny fine-tuned language model based on GPT-2 that's trained to:

- 🔡 Translate English → Morse Code
- 📻 Decode Morse Code → English
- 🤖 Respond with quirky sci-fi humor (inspired by TARS from *Interstellar*)
- 🧩 Work within just **128 tokens** (perfect for small devices or fast inference)

It's meant to be small, weird, and a little bit wonderful.

---

## 💡 Key Highlights

| Feature                     | Details                      |
|----------------------------|------------------------------|
| **Base Model**             | GPT-2                        |
| **Context Length**         | 128 tokens                   |
| **Tokenizer**              | Custom-trained               |
| **Fine-tuned Tasks**       | Morse translation, decoding, TARS-style humor |
| **Intended Use**           | Educational, demo, fun!      |
| **License**                | MIT                          |

---

## 🚀 Example Usage

```python
from transformers import GPT2LMHeadModel, GPT2TokenizerFast

model = GPT2LMHeadModel.from_pretrained("SrihariV/Morsent-128T")
tokenizer = GPT2TokenizerFast.from_pretrained("SrihariV/Morsent-128T")

prompt = "Translate: emergency to Morse code [/INST]"
inputs = tokenizer(prompt, return_tensors="pt")
outputs = model.generate(**inputs, max_new_tokens=50)

print(tokenizer.decode(outputs[0], skip_special_tokens=True))
```

##🧪 Known Issues
🚫 Max length is short: 128 tokens only
🤯 Sometimes responds with hallucinated or surreal outputs
😅 TARS-style jokes may be too weird

#📦 Files
pytorch_model.bin — fine-tuned weights
tokenizer.json, tokenizer_config.json — custom tokenizer
config.json — model architecture

## 📚 Inspiration
Morse code from historical datasets
Instruction-tuning format inspired by [LLaMA-Instruct]
TARS-style humor inspired by sci-fi language modeling

## 🤝 Citation

```
@misc{morsent2025,
  title = {Morsent-128T: A Tiny Morse & Humor LLM},
  author = {Srihari Venkatesan},
  year = 2025,
  howpublished = {\url{https://huggingface.co/SrihariV/Morsent-128T}},
}
```
🗣 Contact
Questions? Bugs? Want to collab?

📫 Reach me at: srihariv4942@gmail.com

# "Sometimes the smallest minds deliver the weirdest wonders." – Morsent
