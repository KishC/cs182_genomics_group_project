Deep Learning for Splice Site Prediction in Grass Genomes

This repository contains the code, data curation pipeline, and model checkpoints for a deep learning approach to splice site prediction using Mamba architecture. The work supports the findings of our CS182 course project at UC Berkeley, focusing on genome annotation in Zea mays and generalization to other species.

Overview

Our project uses a Mamba-based sequence model to classify DNA windows as donor, acceptor, or non-splice sites. The model achieves state-of-the-art performance on Zea mays and demonstrates strong cross-species generalization to Sorghum bicolor.

Repository Structure

cs182_project_mamba_only_modeling_working.ipynb:
Complete training and evaluation pipeline, reproduces all results and figures from our final report. Includes data loading, model definition, training, and evaluation.
splice_pipeline.ipynb:
Dataset curation notebook that downloads genomic data and annotations from the NCBI GenBank. By default, it processes Zea mays and Sorghum bicolor but can be easily configured for any species available on GenBank.
model_checkpoints_half_window_800/:
Contains saved model checkpoints from training using a 1602-length sequence window (half-window = 800).

Data

The curated datasets used for training and testing are derived from publicly available assemblies via NCBI GenBank. Our pipeline automatically handles formatting and negative sampling to create balanced datasets for splice site classification.

Model Architecture

Performance metrics and confusion matrices can be replicated by the final notebook, as seen in the paper.
