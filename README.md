# Customer-Segmentation-Project-
# Customer Segmentation with K-Means and Power BI Dashboard

![Dashboard Preview](<img width="1309" height="734" alt="image" src="https://github.com/user-attachments/assets/ab29f8ca-83d7-4ac2-881e-650bdd1489df" />
)

## 📖 Project Overview

This project performs a complete customer segmentation analysis on a dataset of mall customers. It uses unsupervised machine learning (K-Means clustering) in a Python Jupyter Notebook to group customers into distinct segments based on their demographic and spending data.

The final output is an interactive Power BI dashboard that visualizes these segments, provides detailed profiles for each group, and offers actionable business recommendations.

---

## 📋 Table of Contents

- [Key Features](#-key-features)
- [Tech Stack & Tools](#-tech-stack--tools)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Results: Cluster Personas](#-results-cluster-personas)
- [Dashboard Visualization](#-dashboard-visualization)
- [How to Use This Project](#-how-to-use-this-project)
- [File Structure](#-file-structure)
- [License](#-license)

---

## ✨ Key Features

- **Exploratory Data Analysis (EDA):** Visual inspection of data distributions and relationships.
- **K-Means Clustering:** Application of the K-Means algorithm to segment customers.
- **Optimal Cluster Determination:** Use of the **Elbow Method** and **Silhouette Score** to find the ideal number of clusters (k=10).
- **Cluster Profiling:** Detailed analysis of each segment's average age, income, and spending score.
- **PCA Visualization:** 2D projection of the clusters using Principal Component Analysis (PCA) for visual inspection.
- **Interactive Dashboard:** A comprehensive Power BI dashboard for dynamic data exploration and business insights.

---

## 🛠️ Tech Stack & Tools

- **Python:** For data analysis and machine learning.
- **Libraries:**
  - `pandas` & `numpy` for data manipulation.
  - `scikit-learn` for K-Means clustering, scaling, and PCA.
  - `matplotlib` & `seaborn` for static data visualization in the notebook.
- **Jupyter Notebook / Google Colab:** For the development environment.
- **Microsoft Power BI:** For creating the interactive dashboard.

---

## 💾 Dataset

The project uses the **Mall Customers** dataset, which contains the following key features for 200 customers:
- `CustomerID`: Unique identifier for each customer.
- `Gender`: Male or Female.
- `Age`: Age of the customer.
- `Annual Income (k$)`: Annual income in thousands of dollars.
- `Spending Score (1-100)`: A score assigned by the mall based on spending behavior.

---

## ⚙️ Project Workflow

1.  **Data Loading & EDA:** The `Mall_Customers.csv` dataset is loaded, and initial exploratory analysis is performed to understand distributions and identify any missing values.

2.  **Data Preprocessing:**
    - The `Gender` feature is converted into a numerical format using `LabelEncoder`.
    - Key features (`Age`, `Annual Income`, `Spending Score`, and `Gender`) are selected for clustering.
    - All features are standardized using `StandardScaler` to ensure the K-Means algorithm (which is distance-based) performs accurately.

3.  **Finding the Optimal Number of Clusters (K):** The Silhouette Score and Elbow Method were used to evaluate a range of `k` values (from 2 to 10). The **Silhouette Score peaked at k=10**, indicating it as the optimal number of clusters for this dataset.

4.  **Clustering and Labeling:** The K-Means algorithm was fitted on the scaled data with `k=10`. The resulting cluster labels were then added back to the original DataFrame.

5.  **Cluster Profiling & Export:** The data was grouped by the new cluster labels to create average profiles for each segment. Two CSV files were exported:
    - `Mall_Customers_with_clusters.csv`: The original data with the assigned cluster for each customer.
    - `cluster_profiles.csv`: A summary table of the average characteristics for each of the 10 clusters.

6.  **Dashboard Creation:** The `Mall_Customers_with_clusters.csv` file was imported into Power BI to create the final interactive dashboard.

---

## 🎯 Results: Cluster Personas

The analysis revealed 10 distinct customer segments, each with unique characteristics. These personas are crucial for targeted marketing strategies.

| Cluster | Persona Name | Short Summary |
| :--- | :--- | :--- |
| **3 & 7** | **High-Value Targets** | Young, high-income professionals who spend a lot; the mall's most valuable customers. |
| **8** | **Young Enthusiasts** | Very young customers with low income but a very high willingness to spend on trends. |
| **1** | **Young Spenders** | Young adults with moderate income who enjoy shopping and have a high spending score. |
| **6** | **Standard Customers (Young)** | A large group of younger customers with average income and spending habits. |
| **4** | **Standard Customers (Older)** | A significant segment of older customers with stable, average income and spending. |
| **5 & 9** | **Cautious Earners** | High-income, middle-aged customers who earn a lot but spend very little. |
| **0** | **Cautious Seniors** | Older customers with moderate income who are careful with their spending. |
| **2** | **Budget-Conscious Adults**| Middle-aged adults with low income who are the most frugal and have very low spending scores. |

---

## 📊 Dashboard Visualization

The Power BI dashboard provides an at-a-glance view of the customer segments. It includes:
- KPIs for key metrics (Total Customers, Average Age, etc.).
- A scatter plot visualizing the income vs. spending score for each segment.
- Charts detailing the size and profile of each segment.
- Slicers to filter the data by Gender and Customer Segment for deeper analysis.

---

## 🚀 How to Use This Project

To replicate this analysis, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Naveen75cmd/Customer-Segmentation-Project-
    ```

2.  **Install dependencies:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```

3.  **Run the Jupyter Notebook:**
    - Open and run the `Customer Segmentation Project.ipynb` notebook. This will perform the analysis and generate the `Mall_Customers_with_clusters.csv` file.

4.  **Use the Power BI Dashboard:**
    - Open the `.pbix` file with Power BI Desktop.
    - If prompted, update the data source to point to the `Mall_Customers_with_clusters.csv` file on your local machine.

File Structure : 

├── Customer Segmentation Project.ipynb # The main Jupyter Notebook for the analysis.
├── Mall_Customers.csv # The original, raw dataset.
├── Mall_Customers_with_clusters.csv # The dataset with added cluster labels.
├── cluster_profiles.csv # A summary of the average profile for each cluster.
├── Customer Segmentation Dashboard.pbix # The interactive Power BI dashboard file.
├── dashboard_preview.png # A screenshot of the dashboard.
└── README.md # This file.

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 👨‍💻 Author

Naveen M.S - www.linkedin.com/in/naveen-ms

