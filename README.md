

# 🔍 Fine-Tuning Qwen2-VL for LaTeX OCR (with Unsloth)

This project fine-tunes the 4-bit Qwen2-VL-7B-Instruct vision-language model using the [Unsloth](https://github.com/unslothai/unsloth) framework to convert images of mathematical formulas into LaTeX.

---

## 🚀 Key Features
- Uses **Unsloth** for efficient 4-bit LoRA fine-tuning.
- Model: `unsloth/Qwen2-VL-7B-Instruct-bnb-4bit`
- Dataset: [`unsloth/Latex_OCR`](https://huggingface.co/datasets/unsloth/Latex_OCR)
- Task: **Image-to-LaTeX text generation**

---

## 🛠 Quick Setup
```bash
pip install --no-deps bitsandbytes accelerate xformers==0.0.29.post3 peft trl triton cut_cross_entropy unsloth_zoo
pip install sentencepiece protobuf datasets huggingface_hub hf_transfer
pip install --no-deps unsloth
📚 Pipeline Summary
##Load Qwen2-VL with Unsloth:

1.Apply LoRA (Low-Rank Adaptation).

2.Preprocess dataset into chat-style messages.

3.Fine-tune using SFTTrainer for 30 steps (demo).

4.Run inference with image + prompt.

✨ Example Prompt:

"Write the LaTex representation for this image."


✅ Future Ideas:

1.Train on handwritten formulas.

2.Extend to Bengali or multilingual OCR.

3.Deploy as an interactive app.
