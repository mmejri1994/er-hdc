# Er-HDC
Error Resilient Hyperdimensional Computing Using Hypervector Encoding and Cross-Clustering

## Description
The paper provided two algorithms a checksum hypervector encoding (CHE) framework and cross-hypervector clustering (CHC) framework to make the hyperdimensional computing resilient against soft and timing errors that may occur in the associative memory.

## Installation and Setup

### Step 1: Install Requirements
First, install the necessary dependencies listed in `requirements.txt`. Run the following command:
pip install -r requirements.txt

### Step 2: Create Data Directory
Create a folder named `data` to store your datasets. Use the following command:

mkdir ./data

### Step 3: Download Data
Download the required data they are stored as .npy files. The folder includes ISOLET and UCIHAR datasets.

link: https://drive.google.com/drive/folders/1EoCzkYAKJrCbxAzH5aAgvYHVAjJeZBLF?usp=sharing


## Usage

Run the algorithm using the command below. You can adjust the parameters as needed for different configurations.
```rb
python3 main.py
--x_train_filepath "../data/isolet/X_train.npy"
--y_train_filepath "../data/isolet/y_train.npy"
--x_test_filepath "../data/isolet/X_test.npy"
--y_test_filepath "../data/isolet/y_test.npy"
--dim 10000
--epochs 200
--lr 0.035
--init_er 8
--final_er 1
--Thresh 10
--encoding_system "kernel"
--nbr_cluster 1500
--bootstrap 1.0
--eps 1e-5
--itr 2
--weight_cluster 1.1
```


### Custom Configurations
You can modify the parameters in the command to fit your specific needs. Here are the parameters you can adjust:
- `dim`: Dimension size (e.g., 10000)
- `epochs`: Number of training epochs (e.g., 200)
- `lr`: Learning rate (e.g., 0.035)
- `init_er`: Initial error rate (e.g., 8)
- `final_er`: Final error rate (e.g., 1)
- `Thresh`: Threshold value (e.g., 10)
- `encoding_system`: Encoding system used (e.g., "kernel")
- `nbr_cluster`: Number of clusters (e.g., 1500)
- `bootstrap`: Bootstrap value (e.g., 1.0)
- `eps`: Epsilon value for convergence (e.g., 1e-5)
- `itr`: Number of iterations (e.g., 2)
- `weight_cluster`: Weight for clustering (e.g., 1.1)

## Reproducing Paper Results
To reproduce the results of the paper, particularly for the Clustering method, use the following settings:

| Dataset | HDC Dimension | Number of Clusters | Threshold |
|---------|---------------|--------------------|-----------|
| Isolet  | 10000         | 1500               | 10        |
| Ucihar  | 10000         | 1500               | 10        |

For academic use, please cite this work as follows:

## <span id="citelink">Citation</span>
If you find this repository useful in your research, please consider citing the following papers:
```
@article{Er-HDC2024,
  title         = {Error Resilient Hyperdimensional Computing Using Hypervector Encoding and Cross-Clustering},
  conference    = {IEEE VLSI Test Symposium},
  year          = {2024},
}
```

