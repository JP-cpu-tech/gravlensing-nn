# gravlensing-nn
A Google Colab ML project using a PyTorch two-stage CNN with a MobileNetV3-Small feature extractor to detect and classify gravitational lensing profiles (strong, weak, microlensing). Developed with Claude AI; includes a companion gravitational lensing research journal.

## Research & Project Context
Alongside the machine learning model, I conducted an independent literature review analyzing academic papers on strong lensing, weak lensing, and microlensing. I tracked my learning journey, summaries, and personal qualitative analyses in a dedicated research journal.

* **Research Journal & Literature Review:** 

## Model Architecture
The network is structured around a multi-task framework to maximize efficiency:
1. **Shared Feature Extractor:** Uses a pre-trained **MobileNetV3-Small** backbone to process astronomical images while remaining computationally efficient within Google Colab's virtual hardware limits.
2. **Detection Head:** A fully connected layer performing binary classification (`lensed` vs. `non-lensed`).
3. **Classification Head:** A secondary fully connected layer that maps lensed images into three distinct physical profiles: `strong`, `weak`, or `microlensing`.

## AI Collaboration Methodology
To maintain absolute academic transparency, the workflow for this project was divided:
* **My Role (Project Architect):** I defined the structural pipeline, selected the multi-task dual-head objective, managed the data environment, tracked the optimization loops (loss curves), and connected the outputs back to my physics literature review.
* **AI's Role (Syntax Translator):** Claude AI translated my conceptual logic into explicit PyTorch/Python syntax and resolved internal tensor dimension mismatches between the shared base and the dual heads.

## Repository Contents
* `lensing_neural_network.ipynb` - The complete Google Colab notebook containing data loops and model structures.
* `/results` - Saved loss curves and model prediction outputs.
