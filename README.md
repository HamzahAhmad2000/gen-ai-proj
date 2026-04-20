# Generative AI Project Collection

`gen-ai-proj` is a notebook-driven collection of experiments covering multiple generative AI directions, including text-to-image generation, GAN-based image synthesis, Stable Diffusion workflows, and a T5-based text generation pipeline. Rather than being a single packaged app, the repository acts as a working lab of research notebooks, pretrained assets, generated outputs, and third-party model code.

## Repository focus

This project brings together several generative AI experiments in one place:

- AttnGAN exploration
- BigGAN experimentation
- DCGAN training workflows
- Stable Diffusion generation
- custom model experimentation
- T5 fine-tuning for structured text generation from JSON inputs

## Key contents

### Core notebooks

- `AttnGAN.ipynb` clones and sets up the AttnGAN repository for text-to-image generation experiments.
- `BigGANs.ipynb` explores BigGAN-based workflows using the Hugging Face `pytorch-pretrained-BigGAN` codebase.
- `DCGAN_Training[.ipynb` contains DCGAN-related model training steps, including dataset loading and model-saving logic.
- `stableDiffusion.ipynb` experiments with Stable Diffusion and the `diffusers` ecosystem.
- `GenAIProject.ipynb`, `GenProjectDataPreprocessing.ipynb`, and `genCode.ipynb` focus on preparing JSON data and fine-tuning a T5 model for text generation.
- `GenAIProjectCustomModel.ipynb` and `GenAIProjectModelTraining.ipynb` document higher-level comparisons and planning around custom and pre-trained generative models.

### Model and data assets

- `fine_tuned_t5_model/` stores tokenizer and model artifacts for a fine-tuned T5 workflow.
- `input.json` and `output.json` provide structured source and generated data for the text-generation pipeline.
- `output_0.png`, `output_1.png`, and `output_2.png` are generated image outputs.

### Bundled upstream repositories

- `AttnGAN/`
- `pytorch-pretrained-BigGAN/`

These folders indicate that the project reuses established external implementations as part of the experimentation workflow.

## T5 text-generation workflow

One major thread in the repository is a Hugging Face T5 pipeline that:

- loads structured JSON input and target data
- prepares paired training examples
- defines a custom `Dataset`
- tokenizes inputs and targets
- fine-tunes a T5 model
- saves the resulting tokenizer and model artifacts into `fine_tuned_t5_model/`
- performs inference for new descriptions

This makes the repository broader than image generation alone. It also includes a practical text-generation and model-fine-tuning component.

## Technologies used

- Python
- PyTorch
- Hugging Face Transformers
- Diffusers
- AttnGAN
- BigGAN
- DCGAN
- Jupyter Notebook / Google Colab workflows

## How to use the repository

Because this repo is notebook-centered, the usual workflow is:

1. Open the notebook that matches the experiment you want to run.
2. Install the dependencies referenced by that notebook.
3. Mount data or load local assets if the notebook assumes a Colab environment.
4. Run the notebook cell by cell.
5. Review generated images, saved checkpoints, or model artifacts.

## Notes on project structure

- Some notebooks assume Google Colab and Google Drive paths.
- Some experiments depend on cloned third-party repositories.
- The repository is best treated as an experimental portfolio rather than a polished production package.
- There is overlap between notebooks, which is common in iterative research projects.

## Good follow-up improvements

- add a shared `requirements.txt` or environment file at the root
- document dataset sources and expected folder structure
- separate image-generation and text-generation work into clearly named subfolders
- add example commands for reproducing each notebook workflow
- clean up duplicate notebooks and unused artifacts

## Summary

This repository is a multi-model generative AI lab that combines GAN-based experiments, Stable Diffusion workflows, and T5 fine-tuning for structured text generation. It is most valuable as a research and learning repository that shows hands-on work across several important generative AI techniques.
