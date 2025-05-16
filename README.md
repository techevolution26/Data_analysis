# Data_analysis
Using python libraries to perform an extensive analysis
## Libraries & Methods

### 1. Data Loading & Inspection  
- **pandas**  
  - `pd.read_csv()`  
  - `pd.to_datetime()`  
  - `df.columns.tolist()`  
  - `df.head()` / `df.tail()`  
  - `df.shape`  
  - `df["column"].nunique()`  
  - `df.isnull().sum()`  

### 2. Data Cleaning & Transformation  
- **pandas.DataFrame**  
  - `.dropna(subset=[…])`  
  - `.sort_values([…])`  
  - `.groupby("column")["col"].transform(lambda x: …)`  
  - `.fillna()` / `.ffill()`  
  - `.merge()`  
  - `.to_csv()` (optional saving of cleaned data)  

### 3. Exploratory Data Analysis (EDA) & Plots  
- **matplotlib.pyplot**  
  - `plt.figure()`  
  - `plt.plot(x, y, label=…)`  
  - `plt.title()` / `plt.xlabel()` / `plt.ylabel()`  
  - `plt.legend()`  
  - `plt.tight_layout()`  
  - `plt.show()`  
  - `plt.pie()`  

- **seaborn**  
  - `sns.barplot(data=…, x=…, y=…)`  
  - `sns.heatmap(corr_df, annot=True, fmt=".2f", cmap="viridis")`  

### 4. Interactive Mapping (Optional)  
- **plotly.express**  
  - `px.choropleth(data_frame, locations="iso_code", color="…", hover_name="…")`  

- **geopandas** (advanced)  
  - `gpd.read_file()`  
  - `.merge()` with your COVID DataFrame  

### 5. Statistical & Summary Metrics  
- Computing new columns:  
  - `df["death_rate"] = df.total_deaths / df.total_cases`  
  - `df["pct_vaccinated"] = df.total_vaccinations / df.population * 100`  
  - `.rolling(window=7).mean()` (7-day moving average)  
- Correlation:  
  - `df.corr()`  

### 6. Notebook Export  
- **Jupyter nbconvert**  
  ```bash
  jupyter nbconvert notebooks/06_report.ipynb --to pdf
