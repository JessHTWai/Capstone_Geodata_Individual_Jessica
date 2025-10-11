**Development of parts of pipeline for extraction of Geodata from PDFS**

This repository contains all code and notebooks for extracting, processing, and mapping main study areas and locality information from a collection of academic geoscience theses (PDFs).
The pipeline aims to produce evidence-based, transparent, and mappable datasets of study sites, linked to thesis metadata.

**Repository Structure & Workflow**
1. PDF to Text Extraction

text_extraction_1.ipynb
First iteration of the PDF-to-text pipeline. Converts PDFs to raw text for downstream processing.

text_extraction_final.ipynb
Improved and production-ready PDF-to-text extraction.

Includes page mapping, allowing every paragraph or sentence to be linked back to its page in the original PDF—increasing traceability and transparency of location extraction.

This notebook forms the basis for group workflows and will be pushed to the group repository.

2. LLM Location Extraction & Prompt Evaluation

LLM_zero_shot_vs_few_shot.ipynb

Compares zero-shot and few-shot prompting strategies for extracting locations from text using large language models (LLMs).

Evaluates prompt quality and extraction accuracy to inform best practices for the main pipeline.

LLM_location_extraction_final.ipynb

Extracts all explicit location mentions from text (in paragraph chunks), producing structured outputs suitable for automated geocoding and mapping.

The most robust version for general location extraction; will be pushed to the group repository.

3. Main Study Area Extraction

Main-study-area.ipynb

Identifies the main study area(s) for each thesis, links them to thesis title, author, and year, and geocodes the results.

Outputs are visualized on an interactive map for spatial summary of the dataset.

Also scheduled for group repository inclusion.

**Project Overview**

The notebooks in this repository are the foundation for the group’s full model pipeline, supporting transparent, reproducible, and high-quality geoscience data extraction from academic literature.

Key steps include:

PDF-to-text conversion with page traceability

Prompt evaluation and selection for LLM extraction

Paragraph-level location extraction using LLM

Identification and geocoding of main study areas
