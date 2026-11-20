# Liquid Volume Estimation and LLM Post-Training for a Healthcare AI Product

**Vergio Consulting, Computer Vision & LLMs for Healthcare Intern, May to August 2026, Clichy, France**

## Context

For my second internship at Vergio Consulting, I led the technical side of a proof-of-concept AI application for the healthcare market, end to end. The point of the setup was that senior leadership could stay focused on the consulting business while I owned everything technical: architecture, training, evaluation, and deployment decisions.

## What I built

**Liquid volume estimation pipeline.** I built and deployed a pipeline that estimates liquid volume from images, combining a YOLOv8 detection stage with a weighted least squares (WLS) estimation model. The pipeline reached a mean absolute error of 3.94 to 5.28 mL, and building it in-house saved the firm roughly 30,000 EUR in beta development costs compared to market alternatives.

**Small language model fine-tuning.** I fine-tuned Mistral NeMo 12B and Qwen models with qLoRA, running training on OVHcloud GPUs and locally on Apple Silicon through MLX. The training data was sensitive, so I worked on encrypted datasets and set up multi-turn sequential conversational training.

**Autonomous RL post-training loop.** I engineered a reinforcement learning post-training loop connected through an LLM gateway API bridge. The loop automates evaluation and applies Python-based safety gating, so the system can keep improving without a human babysitting every cycle while still failing safe.

## Stack

Python, PyTorch, YOLOv8, qLoRA, MLX, OVHcloud, WLS, API integration, automated evaluation and safety gating

## Results

- Volume estimation MAE of 3.94 to 5.28 mL, accurate enough for the product's healthcare use case.
- About 30,000 EUR saved in beta development costs by building in-house.
- A scalable, autonomous post-training system with automated evaluation and safety gates.

## What I took away

Owning a proof of concept end to end is different from owning a model. Data security, evaluation, cost, and safety gating all turned out to be as much work as the training itself, and they are what make a demo into something a business can actually use.
