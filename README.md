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

**2\. Audio Album (Original)**

- **Album:** _The Dark Side of the Moon_
- **Artist:** Pink Floyd
- **Year:** 1973
- **Medium:** Compact Disc
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
**Conclusion**

This project successfully demonstrates a **fully self-hosted generative AI workflow** for media cover design.
All requirements were satisfied, including offline execution, workflow transparency, and reproducibility, making the solution suitable for academic evaluation in **Advanced Generative AI**.

Github: <https://github.com/azizkuchkarov/cap.stone-pr-2-adv.gen.ai>
