# sd-turbo-in-telugu
Fine-tuning the SD-Turbo model with a custom Pokémon dataset and integrating Telugu prompt support using automatic translation. Generates images from Telugu text using a localized text-to-image pipeline.
#  SD-Turbo Fine-Tuning with Pokémon Dataset + Telugu Prompt Translation

A text-to-image generation project using the powerful [SD-Turbo](https://huggingface.co/stabilityai/sd-turbo) model fine-tuned on a custom Pokémon dataset and enhanced with Telugu prompt support via translation.

---

##  What This Project Does

This project fine-tunes the **Stable Diffusion Turbo (SD-Turbo)** model to generate Pokémon-style images from textual prompts. It also supports **prompts in Telugu**, making it accessible for native users by integrating an automatic translation layer.

---

## 💡 Why SD-Turbo?

- **Ultra-Fast Inference**: SD-Turbo generates images in a single U-Net step, unlike traditional multi-step diffusion models.
- **High-Quality Outputs**: Even with its speed, SD-Turbo retains impressive image quality.
- **Hugging Face Support**: Easily loadable and extendable using Hugging Face 🤗 Transformers and Diffusers libraries.

---

## 🧪 How Fine-Tuning Was Done

- A Pokémon-style dataset was used: [`reach-vb/pokemon-blip-captions`](https://huggingface.co/datasets/reach-vb/pokemon-blip-captions)
- Each data sample includes a Pokémon image and a corresponding BLIP-generated caption.
- The model was fine-tuned on **Google Colab (CPU)** by modifying only the **text encoder** using a lightweight approach (e.g., LoRA or selective parameter updates).
- The result is a domain-adapted model that better understands Pokémon-related concepts when generating images.

---

## 🌐 How Telugu Prompt Translation Is Handled

We added multilingual support using an automatic translation mechanism:

- Telugu prompts are translated to English using a translation library like `transformers`, `googletrans`, or `deep-translator`.
- The translated prompt is passed into the SD-Turbo pipeline to generate images.
- This allows users to give **prompts in Telugu**, while maintaining compatibility with English-only models.

### ✨ Example

Input (Telugu): `ఒక అందమైన పల్లెటూరు వీధి`

→ Translated: `"A beautiful village street"`

→ Output: <img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/db903db4-2ada-437c-9615-3fbd365857bf" />


---

## 🛠️ How to Use This Project

### 💻 Try it in Google Colab

[![Open In Colab]
(https://colab.research.google.com/drive/1AsHCLbUn49PnWHAedwVxrc8Nen0vB4DF?usp=sharing)



### 🧾 Requirements

- Python 3.8+
- `diffusers`, `transformers`, `torch`, `accelerate`, `googletrans` or equivalent for translation

### 📦 Installation (if running locally)

```bash
pip install diffusers transformers torch accelerate googletrans==4.0.0-rc1



