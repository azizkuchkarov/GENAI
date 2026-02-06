**Capstone Project 2 - ART**

**Advanced Generative AI**

**Objective**

The objective of this project is to design alternative cover artwork for iconic media using a **fully self-hosted image generation workflow**.  
All images were generated **locally**, without using any public image generation services or APIs.

The project includes:

- One **book cover**
- One **audio album cover (Compact Disc)**

**Original Works**

**1\. Book (Original)**

- **Title:** _The Great Gatsby_
- **Author:** F. Scott Fitzgerald
- **Year:** 1925
- **Medium:** Book cover

The original cover is used only as a **visual reference** for comparison purposes.

<img width="372" height="583" alt="image" src="https://github.com/user-attachments/assets/c8cab24f-c3bb-4ed4-8425-ab6b8127931e" />
<img width="384" height="577" alt="image" src="https://github.com/user-attachments/assets/d0d8639d-bd33-44b0-abe1-368d09c6d545" />


**2\. Audio Album (Original)**

- **Album:** _The Dark Side of the Moon_
- **Artist:** Pink Floyd
- **Year:** 1973
- **Medium:** Compact Disc
The original album cover is referenced due to its iconic minimalist and symbolic design.
  <img width="400" height="302" alt="image" src="https://github.com/user-attachments/assets/48804da6-4865-4da5-a825-3b3cb70ff8f9" />
  
<img width="335" height="336" alt="image" src="https://github.com/user-attachments/assets/f5fa4215-41a5-402f-bf18-9cc58ef3a332" />

**AI-Generated Works**

**1\. AI-Generated Book Cover**

- **Format:** Book
- **Resolution:** 512 × 768
- **Concept:**  
    A modern reinterpretation inspired by art-deco aesthetics, featuring a symbolic night cityscape and surreal visual elements.  
    Typography was intentionally excluded to avoid diffusion-based text artifacts.

**2\. AI-Generated Audio Album Cover (CD)**

- **Format:** Compact Disc
- **Resolution:** 512 × 512
- **Concept:**  
    A modern AI-generated reinterpretation inspired by _The Dark Side of the Moon_, preserving the symbolic prism/light concept while avoiding direct replication of the original artwork.

**Workflow Description**

A node-based workflow was implemented using **ComfyUI**, ensuring transparency and reproducibility.

**Workflow stages:**

- Text prompts encoded using CLIP
- Latent space initialization
- Diffusion sampling using KSampler
- Latent decoding via VAE
- Local image saving

The workflow was fully executed **offline** on a local machine.

<img width="974" height="458" alt="image" src="https://github.com/user-attachments/assets/e0ddd405-9daa-431e-b75e-d37a4420a6fc" />


**Image Generation Model**

- **Model:** Stable Diffusion 1.5 (Realistic Vision v1.4)
- **Base Architecture:** Stable Diffusion 1.5
- **Format:** .safetensors
- **Source:** Hugging Face (open-weight checkpoint)
- **Inference Mode:** CPU-only, local execution

**LoRAs / Adapters / Extensions**

- **LoRAs:** None
- **Adapters:** None
- **Extensions:** None

Only the base model was used to ensure reproducibility and simplicity.

**Technical Generation Details**

| **Parameter** | **Value** |
| --- | --- |
| Sampler | Euler a |
| Steps | 20  |
| CFG Scale | 7   |
| Seed | Fixed (for reproducibility) |
| Book Resolution | 512 × 768 |
| CD Resolution | 512 × 512 |

**Prompts Used**

**Book Cover - Positive Prompt**

art deco inspired illustrated book cover,

deep blue night sky, stylized city skyline,

symbolic glowing eyes in the sky,

elegant, minimalist, clean composition,

professional book cover illustration, no text

**CD Album Cover - Positive Prompt**

minimalist album cover inspired by classic progressive rock,

dark black background, abstract prism-like geometric form,

glowing spectrum of light, modern reinterpretation,

clean and symbolic composition,

high contrast, professional CD album artwork,

no text, no logos

**Negative Prompt (All Generations)**

blurry, low quality, watermark, logo, text,

distorted, ugly, noisy

**Pipeline Screenshots**

Screenshots were captured after execution to demonstrate the complete workflow:

- Full ComfyUI node graph
- KSampler configuration (steps, CFG, sampler, seed)

**Resources Used**

- **WebUI:** ComfyUI
- **Execution Mode:** Local, self-hosted
- **Hardware:**
  - CPU-only system
  - No dedicated GPU (Intel integrated graphics)
- **Operating System:** Windows
- **Internet Usage:** Model download only (no cloud inference)
<img width="974" height="381" alt="image" src="https://github.com/user-attachments/assets/db73b9b4-f2c5-4c97-aaf7-ac432cadeb40" />

**Conclusion**

This project successfully demonstrates a **fully self-hosted generative AI workflow** for media cover design.
<img width="974" height="379" alt="image" src="https://github.com/user-attachments/assets/35753889-00db-4268-b07d-c7c06c4d8f95" />

All requirements were satisfied, including offline execution, workflow transparency, and reproducibility, making the solution suitable for academic evaluation in **Advanced Generative AI**.

Github: <https://github.com/azizkuchkarov/cap.stone-pr-2-adv.gen.ai>
