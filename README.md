

---

# 🛰️ GPT-OSS Vision — Enhancing OpenAI’s GPT-OSS with Multimodal Vision Capabilities

### Smart India Hackathon 2025

**Problem Statement ID:** SIH25170
**Theme:** Space Technology
**Category:** Software
**Team:** Solution_Architects (ID: 79440)
**Prototype/Demo Link:** [Watch Here](https://youtu.be/y-UwhRt8GXo)
**Code Base:** [GitHub Repository](https://github.com/sandeshlavshetty/GPT_OSS20B.git)

---

## 🧠 Problem Statement

While **GPT-OSS** excels at text reasoning and instruction-following, it lacks the ability to process **visual information** — a major limitation for real-world tasks involving both **images and text**.

### Key Challenges:

* No visual understanding in GPT-OSS.
* Inability to perform **Visual Question Answering (VQA)** or **image captioning**.
* Lack of multimodal alignment for **Earth Observation (EO)** data interpretation.

---

## 🚀 Our Solution

We introduce **GPT-OSS Vision**, a **multimodal GPT-OSS** model that integrates **visual perception** through a **lightweight projection-based adapter** between a **vision encoder (CLIP)** and the **LLM backbone (GPT-OSS-20B)**.

### Core Capabilities:

* 🖼️ **Image Captioning:** Describe images in natural language.
* ❓ **Visual Question Answering (VQA):** Answer questions about images.
* 💬 **Multimodal Instruction Following:** Combine text and visual reasoning.
* 🌍 **ISRO EO Data Integration:** Extendable for satellite imagery analysis.

---

## 🧩 System Architecture

### Phase 1 — Efficient Multimodal Foundation

| Component            | Description                                   |
| -------------------- | --------------------------------------------- |
| **Base LLM**         | GPT-OSS-20B *(Frozen)*                        |
| **Adapter**          | CLIP2LLM Linear + LayerNorm (Trainable)       |
| **Dataset**          | LLaVA-Instruct-58K *(Image-Instruction Data)* |
| **Hardware**         | NVIDIA H100 GPU (80GB VRAM)                   |
| **Precision**        | Bfloat16 (Efficient Compute)                  |
| **Trainable Params** | < 1% of total                                 |

---

## 🌐 Phase 2 — ISRO EO Linkage

Integrating **Remote Sensing Encoders (e.g., SatMAE)** allows GPT-OSS Vision to interpret raw **Earth Observation (EO)** data.
This enables **Conversational EO**, where GPT-OSS can generate **natural language reports from satellite imagery** for ISRO’s data analysis systems.

---

## ⚙️ Phase 3 — Beyond Single-Point Fusion

Adopting the **Florence-VL inspired approach**, the architecture supports **multi-level cross-modal reasoning**, improving performance on spatially complex imagery.

---

## 🧱 Tech Stack

* **Language Model:** GPT-OSS-20B
* **Vision Encoder:** CLIP / SatMAE (for EO imagery)
* **Training:** PyTorch + LoRA + Mixed Precision
* **Data:** LLaVA-Instruct-58K + Open EO Datasets (Sentinel-2, Landsat)
* **Deployment:** Modular FastAPI interface for inference

---

## 🧪 Training Pipeline

The training process is implemented in **`Final_training_script (1).ipynb`**, consisting of:

1. **Vision Encoder Loading** (CLIP / SatMAE)
2. **Adapter Initialization** (Linear + LayerNorm)
3. **Feature Projection Alignment**
4. **LoRA-Based Fine-Tuning** (<1% parameters)
5. **Evaluation on VQA & Captioning Tasks**

---

## 🔐 Feasibility & Viability

| Aspect                   | Description                                                     |
| ------------------------ | --------------------------------------------------------------- |
| **Modular Design**       | Vision and language modules are independently updatable.        |
| **Lightweight Training** | Efficient LoRA adapters allow fine-tuning on a single 80GB GPU. |
| **Open Source**          | Built using open datasets and models for full reproducibility.  |
| **Scalable Integration** | Designed for ISRO’s EO systems and scalable deployments.        |

---

## ⚠️ Potential Challenges & Mitigation

| Challenge                  | Mitigation                                        |
| -------------------------- | ------------------------------------------------- |
| Limited EO multimodal data | Use open-source datasets (Sentinel-2, Landsat).   |
| Risk of LLM degradation    | Freeze GPT-OSS core layers.                       |
| Compute constraints        | Use mixed precision & gradient checkpointing.     |
| Data sensitivity           | Apply strict data governance and access controls. |

---

## 💡 Impact

* **ISRO & Earth Observation:** Enables GPT-OSS to describe and interpret satellite images.
* **Sustainability:** Reduces manual analysis effort and improves decision-making efficiency.
* **Scalable Open-Source Framework:** Paves the way for multimodal research within India’s space data ecosystem.

---

## 🧑‍💻 Contributors

**Team Name:** Solution_Architects
**Team ID:** 79440

| Name                     | Role                       |
| ------------------------ | -------------------------- |
| Sandesh Lavshetty        | Lead Developer & Architect |
| [Add other team members] | [Their roles]              |

---

## 🪄 How to Run

1. Clone the repo:

   ```bash
   git clone https://github.com/sandeshlavshetty/GPT_OSS20B.git
   cd GPT_OSS20B
   ```
2. Open the training notebook:

   ```
   Final_training_script (1).ipynb
   ```
3. Run cells sequentially to train the adapter model.
4. Use the provided FastAPI endpoint for multimodal inference.

---

## 📺 Demo & Resources

* **Prototype/Demo:** [Watch Here](https://youtu.be/y-UwhRt8GXo)
* **Code Base:** [GitHub Repository](https://github.com/sandeshlavshetty/GPT_OSS20B.git)

---

## 🏁 Acknowledgements

Special thanks to **ISRO** and **Smart India Hackathon 2025** organizers for providing the platform to innovate in **Space Technology** and **AI research**.

---
