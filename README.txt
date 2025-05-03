# Efficient Image Captioning using CLIP, GANs, and T5

> **Refining CLIP-Based Fine-Grained Image Captioning with T5 Summarization**
>
> XXX-X-XXXX-XXXX-X/XX/$XX.00 ©20XX IEEE

**Authors:**
- Hemant Prakash S (244101021), IIT Guwahati
- Mani Deep G (244101027), IIT Guwahati
- Ishan Varshney (244101022), IIT Guwahati
- Priyanshu Srivastav (244101033), IIT Guwahati
- P Sai Kiran Chary (244101031), IIT Guwahati

---

## 📝 Abstract

This study addresses the challenges of generating accurate and concise image captions by exploring three distinct approaches: fine-tuning state-of-the-art (SOTA) models on a custom dataset, employing a Generative Adversarial Network (GAN) for enhanced caption diversity, and utilizing the T5 model for text summarization. The custom dataset and fine-tuning process allow for captions tailored to highlight essential image details while omitting irrelevant background elements. However, certain images produced overly lengthy captions, capturing minor background objects that diminished cosine similarity accuracy. To address this, the T5 model was applied to reduce these extraneous details, resulting in shorter captions that preserved core semantics. This refinement improved cosine similarity by 0.002% on a test set of 500 images. This paper discusses the architecture and effectiveness of each approach and presents a comparative analysis of their impact on caption quality. citeturn0file0

**Keywords:** GAN, fine-tuning, T5 model

---

## 🎯 Objective

Generate semantically rich, grammatically correct, and concise captions for images with minimal computational overhead by using:
- Pretrained vision-language models like **CLIP**
- Fine-tuned caption generators
- **GAN**-based improvements
- **T5** for caption summarization

---

## 📌 Problem Statement

Traditional image captioning systems often rely on training with reference captions, which can result in:
- Generic outputs
- Repetitive or ungrammatical sentences
- High training costs

Our aim is to enhance the distinctiveness and grammatical quality of captions while reducing resource demands.

---

## 🧩 Approaches

### 🔹 1. Fine-tuning CLIP with Custom Dataset
- Uses CLIP’s image-text similarity metric to guide training.
- Improves caption distinctiveness through a **CLIP reward** mechanism.
- Incorporates grammar-aware fine-tuning of CLIP’s text encoder.

### 🔹 2. GAN-based Image Captioning
- Generator-Discriminator setup to refine caption quality.
- Challenges include training instability, high computational cost, and limited performance gains.

### 🔹 3. T5 for Caption Summarization
- Converts verbose captions into concise ones using the T5 model.
- Benefits from pretrained transformer architecture and large-scale language modeling.
- Produces fluent and semantically rich outputs.

---

## 🏗️ Architecture Diagrams

Refer to the presentation slides (`Image_Captioning_PPT.pptx`) or the Jupyter notebooks for detailed architecture overviews.

---

## 📊 Evaluation Criteria

- **Caption Quality**: Fluency, grammaticality, and descriptiveness.
- **Efficiency**: Training/inference time, memory usage.
- **Scalability**: Ease of adaptation to new datasets or domains.

---

## ✅ Results and Discussion

- **CLIP Reward** significantly improves relevance without relying on traditional reference captions.
- **T5** effectively reduces verbosity while preserving semantic integrity.
- **GANs** offer marginal performance gains at high cost and complexity.

---

## 🔍 Future Work

- Explore lightweight transformer variants for faster summarization.
- Fine-tune the CLIP reward to align better with human judgment.
- Improve GAN training stability with newer stabilization techniques.

---

## 📂 Repository Structure

```bash
├── GAN.ipynb                       # GAN-based image captioning
├── CLIP_improved_with_dataset.ipynb  # CLIP fine-tuning and reward integration
├── t5_model.ipynb                  # Caption summarization using T5
├── Image_Captioning_PPT.pptx      # Presentation slides
├── Report.pdf                      # Full project report (IEEE format)
└── README.txt                       # Project overview

---

## 🙏 Acknowledgements

- OpenAI CLIP model
- HuggingFace Transformers (T5)
- NVIDIA for computing resources
