# sd-turbo-in-telugu
Fine-tuning the SD-Turbo model with a custom Pokémon dataset and integrating Telugu prompt support using automatic translation. Generates images from Telugu text using a localized text-to-image pipeline.
# 🧠 SD-Turbo Fine-Tuning with Pokémon Dataset + Telugu Prompt Translation

A text-to-image generation project using the powerful [SD-Turbo](https://huggingface.co/stabilityai/sd-turbo) model fine-tuned on a custom Pokémon dataset and enhanced with Telugu prompt support via translation.

---

## 🚀 What This Project Does

This project fine-tunes the **Stable Diffusion Turbo (SD-Turbo)** model to generate Pokémon-style images from textual prompts. It also supports **prompts in Telugu**, making it accessible for native users by integrating an automatic translation layer.

---

## 💡 Why SD-Turbo?

- **Ultra-Fast Inference**: SD-Turbo generates images in a single U-Net step, unlike traditional multi-step diffusion models.
- **High-Quality Outputs**: Even with its speed, SD-Turbo retains impressive image quality.
- **Hugging Face Support**: Easily loadable and extendable using Hugging Face 🤗 Transformers and Diffusers libraries.

---

## 🧪 How Fine-Tuning Was Done

- A custom Pokémon dataset was used, consisting of images paired with textual descriptions.
- The model was fine-tuned using a low-RAM setup (Colab CPU) by saving and updating only the text encoder weights.
- The fine-tuned model learns domain-specific features (Pokémon shapes, colors, styles) to generate more accurate images on similar prompts.

---

## 🌐 How Telugu Prompt Translation Is Handled

We added multilingual support by using an automatic translation layer:
- Telugu prompts are translated to English using a translation model/library (`transformers` or `googletrans`).
- The translated English prompt is fed to the SD-Turbo model for image generation.
- This enables a **Telugu → Image** pipeline without needing a multilingual model.



