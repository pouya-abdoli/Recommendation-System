# Recommendation System

> Learning, building, and comparing recommendation systems — one step at a time.

## 🎯 Goal

My ultimate goal is to develop a **production-ready recommendation system** for an e-commerce website.

This repository is my learning journey. I explore different models, architectures, and evaluation techniques — then compare them side by side.

## 📚 What's Inside Up to Now

| Dataset | Status | Library | Models Used |
|---------|--------|---------|-------------|
| MovieLens-100k | ✅ Done | Surprise | SVD, KNN, BaselineOnly, SlopeOne |
| MovieLens-1m | ✅ Done | Surprise | SVD, KNN, BaselineOnly, SlopeOne |

## CF vs MF: The Difference

| | **Collaborative Filtering (CF)** | **Matrix Factorization (MF)** |
|---|-----------------------------------|-------------------------------|
| **What it is** | A recommendation **strategy** | A mathematical **technique** |
| **How it works** | "Users who liked X also liked Y" | Factorizes user-item matrix into latent vectors |
| **Analogy** | "Ask similar people for advice" | "Discover hidden taste dimensions" |
| **Examples** | User-User, Item-Item, MF | SVD, ALS, NMF, SVD++ |

### One-Line Summary

> **CF is the *what* (recommend based on crowd behavior). MF is one *how* (learn latent factors to do it).**

### Key Takeaway

**All MF is CF, but not all CF is MF.** MF is just the most popular way to implement CF today.


## 🗂️ Recommendation Systems: Approaches & Architectures

```text
Recommendation Systems
│
├── Non-Personalized
│   ├── Most Popular
│   ├── Trending
│   └── Top Rated
│
├── Content-Based Filtering
│   ├── TF-IDF Based
│   ├── Keyword-Based
│   ├── Metadata-Based
│   ├── Embedding-Based
│   └── Deep Content Models
│
├── Collaborative Filtering
│   │
│   ├── Memory-Based CF
│   │   ├── User-Based CF
│   │   └── Item-Based CF
│   │
│   ├── Model-Based CF
│   │   │
│   │   ├── Matrix Factorization
│   │   │   ├── SVD
│   │   │   ├── SVD++
│   │   │   ├── ALS
│   │   │   ├── PMF (Probabilistic MF)
│   │   │   ├── NMF
│   │   │   ├── BPR-MF
│   │   │   └── Logistic MF
│   │   │
│   │   ├── Factorization Machines
│   │   │   ├── FM
│   │   │   ├── FFM
│   │   │   └── Field-aware FM
│   │   │
│   │   └── Graph-Based Methods
│   │       ├── Random Walk
│   │       ├── Personalized PageRank
│   │       └── Graph Neural Networks
│   │
│   └── Neural Collaborative Filtering
│       ├── NCF
│       ├── MLP-based CF
│       ├── AutoRec
│       ├── Mult-VAE
│       ├── Wide & Deep
│       ├── DeepFM
│       ├── xDeepFM
│       └── DLRM
│
├── Sequential / Session-Based
│   ├── Markov Chains
│   ├── FPMC
│   ├── GRU4Rec
│   ├── SASRec
│   ├── BERT4Rec
│   ├── TiSASRec
│   └── Transformer-based Recommenders
│
├── Knowledge-Based
│   ├── Constraint-Based
│   ├── Case-Based
│   └── Rule-Based
│
├── Demographic-Based
│   ├── Age-Based
│   ├── Gender-Based
│   └── Location-Based
│
├── Context-Aware
│   ├── Time-Aware
│   ├── Location-Aware
│   ├── Device-Aware
│   └── Situation-Aware
│
└── Hybrid Systems
    ├── Content + Collaborative
    ├── Collaborative + Deep Learning
    ├── Multi-Stage Retrieval + Ranking
    ├── Two-Tower Models
    └── Large-Scale Industrial Systems
