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

## 📊 Key Experiments

- RMSE comparison between different algorithms
- Prediction accuracy evaluation
- Model performance on different dataset

## 🧠 What I'm Learning

- Collaborative filtering
- Matrix factorization
- Memory-based vs model-based approaches
- Evaluating 
- Scaling from 100k → 1m → real-world data

## 🔧 Tools Used

- Python
- Surprise library
- Pandas
- Matplotlib (for bar charts & visualizations)

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

## 🌲 Collaborative Filtering: Tree with Libraries & Algorithms

```text
Collaborative Filtering
│
├── Memory-based (Neighborhood)
│   │
│   ├── User-User
│   │   ├── Surprise: KNNBasic, KNNWithMeans, KNNBaseline
│   │   ├── scikit-learn: NearestNeighbors
│   │   └── implicit: NearestNeighbors (item-item only)
│   │
│   └── Item-Item
│       ├── Surprise: KNNBasic (user_based=False)
│       ├── implicit: NearestNeighbors (cosine, bm25)
│       └── scikit-learn: cosine_similarity
│
├── Model-based
│   │
│   ├── Matrix Factorization
│   │   ├── SVD
│   │   │   ├── Surprise: SVD
│   │   │   ├── implicit: use for explicit? no (ALS for implicit)
│   │   │   └── fancyimpute: SVD
│   │   │
│   │   ├── ALS (Alternating Least Squares)
│   │   │   ├── implicit: AlternatingLeastSquares
│   │   │   ├── Spark MLlib: ALS
│   │   │   └── lightfm: LightFM (uses WARP, not pure ALS)
│   │   │
│   │   ├── NMF (Non-negative MF)
│   │   │   ├── Surprise: NMF
│   │   │   ├── scikit-learn: NMF
│   │   │   └── implicit: NMF
│   │   │
│   │   └── SVD++
│   │       └── Surprise: SVDpp
│   │
│   ├── Deep Learning
│   │   │
│   │   ├── Neural Collaborative Filtering (NCF)
│   │   │   ├── TensorFlow Recommenders (TFRS)
│   │   │   ├── PyTorch: RecBole
│   │   │   └── cornac: NCF
│   │   │
│   │   ├── Two-Tower (Dual Encoder)
│   │   │   ├── TensorFlow Recommenders (TFRS)
│   │   │   ├── PyTorch: DLRM (Meta)
│   │   │   └── RecBole: DSSM
│   │   │
│   │   └── Graph Neural Networks (GNNs)
│   │       ├── PyTorch Geometric
│   │       ├── DGL (Deep Graph Library)
│   │       └── RecBole: LightGCN, NGCF
│   │
│   ├── Clustering
│   │   │
│   │   ├── K-Means
│   │   │   ├── scikit-learn: KMeans
│   │   │   └── cornac: KMeans
│   │   │
│   │   └── DBSCAN / Spectral
│   │       └── scikit-learn
│   │
│   └── Association Rules
│       ├── Apriori
│       │   ├── mlxtend: apriori
│       │   └── efficient-apriori
│       │
│       └── FP-Growth
│           ├── mlxtend: fpgrowth
│           └── pyspark: FPGrowth
│
└── Hybrid Methods
    │
    ├── LightFM
    │   └── lightfm: LightFM (MF + content features)
    │
    ├── Factorization Machines (FM)
    │   ├── fastFM (Python)
    │   ├── libFM (C++ with Python wrapper)
    │   ├── pytorch-fm
    │   └── TensorFlow Recommenders: FM
    │
    ├── Wide & Deep
    │   └── TensorFlow (tf.estimator)
    │
    └── Deep & Cross (DCN)
        └── TensorFlow: DCN, DCN-V2