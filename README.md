# scRNAseq_PBMC_Pipeline
A complete scRNA-seq preprocessing and clustering pipeline for PBMC 3k dataset using Scanpy and Leiden algorithm.

## 🔬 Project 02: PBMC 單細胞 RNA 定序分析管線

### 🎯 專案目標 (Project Goal)
本專案展示了從原始單細胞計數矩陣到細胞分群與視覺化的完整生物資訊管線，旨在識別 PBMC 樣本中的不同細胞類型。

### 🛠️ 使用技術 (Technologies Used)
* Python (3.x)
* Scanpy (生物資訊核心函式庫)
* Leidenalg (高性能分群演算法)
* UMAP (非線性降維)

### 🔎 數據品質控制 (Quality Control)

為了確保分析基礎的可靠性，我們首先計算並視覺化了關鍵的 QC 指標，並根據圖表結果決定過濾閾值：

![單細胞 QC 診斷圖](images/violin_qc_metrics_pre_filter.png)

**分析結論：**
* 細胞基因數量主要分佈在 200 到 2500 之間。
* 粒線體基因比例主要集中在 5% 以下，證明大部分細胞狀態良好。

### 📈 成果總覽 (Results)

#### 1. 資料清洗與過濾結果
- 原始數據：2700 個細胞, 32738 個基因
- 過濾後：2638 個高品質細胞, 13656 個基因
- 高變異基因 (HVGs) 選擇：1826 個基因用於後續分析

#### 2. UMAP 細胞分群視覺化


![PBMC UMAP 分群圖](umap_pbmc_clustering_v2.png)

圖中清晰地將細胞分成了 14 個群集 (0-13)，展現了 PBMC 樣本的異質性。
