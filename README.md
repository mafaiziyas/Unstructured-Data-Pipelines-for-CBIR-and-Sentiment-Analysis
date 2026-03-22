# Unstructured Data Engineering Pipelines: CBIR & Sentiment Analysis

This repository contains a comprehensive data engineering project focused on building scalable pipelines for unstructured data. By utilizing MongoDB, the project demonstrates a flexible, NoSQL approach to managing complex data types like images, mathematical feature vectors, and social media text.

## Project Overview
The project is divided into two primary technical scenarios:

Secenario 1: Content-Based Image Retrieval (CBIR) System: Developing a system to search for pet species based on visual characteristics.

Secenario 2: Sentiment Analysis Database: Engineering a pipeline for short-form social media text (tweets).

## Secenario 1: Content-Based Image Retrieval (CBIR) System
The objective of this pipeline is to create an organized image library that allows users to search for pet species based on visual characteristics rather than just text labels.

### Data Ingestion & Preprocessing

Collection: Gathered 51 diverse pet images from various sources.

Standardization: Resized all images to a uniform 500x500 pixels.

Cleaning: Applied denoising filters to ensure high-quality feature extraction.

### Manual Annotation

Developed a custom script to label images with keywords and descriptions.

Generated structured metadata from raw image files for better queryability.

### Feature Extraction

Extracted complex visual features to be used as search parameters:

Color: Calculated average RGB values.

Texture: Analyzed contrast, homogeneity, and energy.

Shape: Measured contour area and perimeter.

### Database Integration

Merged metadata, numerical feature vectors, and raw image bytes into single MongoDB documents, creating a fully searchable content-based library.

## Secenario 2: Sentiment Analysis Database Pipeline
This scenario focuses on engineering a pipeline for short-form text data extracted from social media (tweets).

### Pipeline Stages

Raw Data Processing: Ingested 60 short-form text messages in CSV format.

Text Preprocessing (NLP): Utilized NLTK for:

Tokenization: Breaking text into individual words.

Stop-word Removal: Filtering out common words (e.g., "the", "is").

Punctuation Stripping: Cleaning raw text for cleaner analysis.

Vectorization & Labeling: Converted text into numerical representations and applied sentiment labels for machine learning readiness.

Testing & Verification: Used MongoDB aggregation queries to verify sentiment distributions and ensure data integrity.

## Tech Stack

Language:	Python

Database:	MongoDB (NoSQL)

Computer Vision:	OpenCV (cv2), matplotlib, scikit-image

Data Processing:	Pandas, NumPy, JSON, NLTK

## Why MongoDB?
The project utilizes MongoDB due to its schema-less nature, which allows for the seamless storage of unstructured data (images and text) alongside structured data (mathematical vectors and metadata).

Advantage: This flexibility is ideal for evolving projects where new data fields may be added without the need to rebuild the entire database schema.
