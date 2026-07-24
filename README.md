# Ulises Pérez Espinosa Project Portfolio

This repository is a central index of my main technical projects — each one lives in its own repo, linked below with a summary, tech stack, and key highlights so you can jump straight to whichever interests you most.

## 📑 Table of Contents

- [NLP Topic Extraction](#-nlp-topic-extraction)
- [Beehive Anomaly Detection System (LSTM)](#-beehive-anomaly-detection-system-lstm)
- [Motorcycle Multi-Dealership Management System](#-motorcycle-multi-dealership-management-system)

---

## [🔎 NLP Topic Extraction](https://github.com/UlisesPe22/NLP_Topic_Extraction) Data Science Project

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-FFD21E?logo=huggingface&logoColor=black)
![Sentence Transformers](https://img.shields.io/badge/Sentence--Transformers-SBERT-4B8BBE)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![UMAP](https://img.shields.io/badge/UMAP-Dimensionality%20Reduction-6A5ACD)
![HDBSCAN](https://img.shields.io/badge/HDBSCAN-Clustering-556B2F)
![NLTK](https://img.shields.io/badge/NLTK-NLP-9C27B0)

An unsupervised NLP pipeline that extracts and clusters topics from unstructured text without any labeled training data. Text is embedded using SBERT (Sentence-Transformers), reduced to a lower-dimensional space with UMAP, and grouped into topics with HDBSCAN density-based clustering. KeyBERT is used to surface representative keywords per cluster, turning raw text into interpretable topic groups — useful for document summarization, customer feedback analysis, or content categorization at scale.

**Highlights:**
- End-to-end embedding → dimensionality reduction → clustering pipeline
- Fully unsupervised — no manual labeling required
- CPU-only PyTorch backend for lightweight deployment

---

## [🐝 Beehive Anomaly Detection System (LSTM)](https://github.com/UlisesPe22/Anomaly_Detection_System_LSTM_Model) Data Science Project

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?logo=keras&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)

An IoT-connected anomaly detection system for beehive health monitoring. A BME280 sensor streams live temperature, humidity, and pressure readings from inside a hive, and a trained LSTM model analyzes the sequential pattern of those readings to flag whether the colony is healthy ("queen producing") or at risk ("queen not producing"). Results are served through a Flask backend to a live web dashboard, giving beekeepers real-time hive health visibility without needing to physically inspect the hive.

**Highlights:**
- PCA-driven feature selection (temperature, humidity) backed by exploratory data analysis
- Engineered distance features to capture short/mid/long-term sensor drift
- Sliding-window LSTM trained on labeled sequential sensor data
- Real-time Flask + SQLite dashboard with a simulator to replay live sensor streams

---

## [🏍️ Motorcycle Multi-Dealership Management System](https://github.com/UlisesPe22/Motorcycle_Multi_Dealership_Mangement_System) AI-powered full-stack business platform

![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-B73BFE?logo=vite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Gemini](https://img.shields.io/badge/Google%20Gemini-AI-8E75B2?logo=googlegemini&logoColor=white)

An AI-driven dealership management platform built as my thesis project for a real multi-location motorcycle dealership group. The system automates document-heavy dealership workflows — from purchase to sale — using an event-driven architecture and a Google Gemini-powered AI pipeline that reads and validates official ID documents (INE) and dealership paperwork automatically. It manages the full motorcycle lifecycle (purchased → in stock → reserved → sold) with role-based access for owners, managers, and vendors, and a React/Vite frontend backed by a FastAPI + PostgreSQL system.

**Highlights:**
- Full motorcycle lifecycle state machine with sale/payment event tracking
- Gemini-powered document pipeline: ID corner detection, perspective correction, field extraction, and MRZ cross-validation
- JWT authentication with role-based access control (master/owner/manager/vendor)
- Dockerized FastAPI + PostgreSQL backend with async performance load-tested via Locust
- React/Vite frontend with a live owner dashboard
