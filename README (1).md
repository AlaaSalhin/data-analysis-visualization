# Data Analysis & Visualization Portfolio

This notebook is a beginner-friendly **data analysis and visualization mini-portfolio** built in Jupyter/Colab. It demonstrates how to use Python tools such as **Pandas, Matplotlib, Seaborn, Plotly, and Altair** to explore data, understand patterns, and communicate insights clearly.

The notebook uses multiple datasets, including restaurant tipping data, Gapminder global development data, and car performance data. Each section focuses on a different visualization technique and explains why that technique is useful.

---

## Project Goals

The goal of this notebook is to show how different visualization tools can be used for different analytical purposes:

- Understand the structure and quality of a dataset.
- Create new useful features for analysis.
- Explore distributions, relationships, comparisons, and correlations.
- Build interactive visualizations for deeper exploration.
- Use advanced charts for portfolio-level storytelling.
- Create a simple interactive dashboard.

---

## Tools Used

### 1. Pandas

**Purpose:** Data loading, cleaning, profiling, and feature engineering.

Pandas is used before visualization to inspect the dataset and prepare it for analysis. Visualizations are only meaningful when the data is clean and well-structured.

**How it is used in the notebook:**

- Loading datasets into DataFrames.
- Displaying sample rows.
- Checking dataset shape.
- Checking missing values.
- Checking column data types.
- Creating new columns such as `tip_rate`, `is_weekend`, and `bill_bucket`.

**When to use it:**

Use Pandas before creating charts whenever you need to understand, clean, filter, group, or transform data.

---

### 2. Matplotlib

**Purpose:** Basic static plotting and full control over chart appearance.

Matplotlib is one of the core Python visualization libraries. It is useful when you want simple, static, customizable charts.

**How it is used in the notebook:**

- Setting a consistent visual style using `plt.rcParams`.
- Creating figures with custom size.
- Adding titles, labels, legends, and layout control.
- Displaying plots using `plt.show()`.

**When to use it:**

Use Matplotlib when you need static charts for reports, presentations, notebooks, or academic-style figures.

---

### 3. Seaborn

**Purpose:** Statistical visualization with cleaner and more attractive default styles.

Seaborn is built on top of Matplotlib. It is especially useful for exploratory data analysis because it makes statistical plots easier to create.

**How it is used in the notebook:**

- Histogram with KDE.
- Scatter plot with regression line.
- Box plot.
- Swarm plot.
- Bar plot with uncertainty.
- Correlation heatmap.

**When to use it:**

Use Seaborn when you want to quickly understand distributions, relationships, group comparisons, and correlations.

---

## Visualization Techniques Explained

### 1. Histogram + KDE

**Tool used:** Seaborn

**Purpose:** Show the distribution of one numeric variable.

In the notebook, a histogram with KDE is used to show the distribution of `total_bill`.

**Why use it:**

A histogram shows how often values appear in different ranges. KDE adds a smooth curve that helps reveal the general shape of the distribution.

**When to use it:**

Use it when you want to answer questions such as:

- Are the values normally distributed?
- Are most values small, medium, or large?
- Are there outliers?
- Is the data skewed?

**Example use case:**

Understanding whether most restaurant bills are low, moderate, or high.

---

### 2. Scatter Plot + Regression Line

**Tool used:** Seaborn

**Purpose:** Show the relationship between two numeric variables.

In the notebook, this chart is used to compare `total_bill` and `tip`.

**Why use it:**

A scatter plot shows whether two variables move together. The regression line helps summarize the direction of the relationship.

**When to use it:**

Use it when you want to check:

- Whether one variable increases when another increases.
- Whether there is a positive or negative relationship.
- Whether there are unusual points or outliers.

**Example use case:**

Checking whether higher restaurant bills usually lead to higher tips.

---

### 3. Box Plot + Swarm Plot

**Tool used:** Seaborn

**Purpose:** Compare a numeric variable across categories.

In the notebook, this combination is used to compare `tip_rate` across different days.

**Why use it:**

A box plot summarizes the median, spread, and outliers. A swarm plot shows the actual data points, making the visualization more transparent.

**When to use it:**

Use it when you want to compare groups and still see the real data distribution.

**Example use case:**

Comparing tipping behavior across Thursday, Friday, Saturday, and Sunday.

---

### 4. Bar Plot with Uncertainty

**Tool used:** Seaborn

**Purpose:** Compare average values across categories.

In the notebook, a bar plot is used to compare average `tip_rate` by day and time.

**Why use it:**

Bar plots make group comparisons easy. Seaborn can also show uncertainty, which helps communicate that averages may vary.

**When to use it:**

Use it when you want to compare category averages, such as:

- Average sales by region.
- Average score by group.
- Average tip rate by day and meal time.

**Example use case:**

Checking whether lunch or dinner has a higher average tip rate.

---

### 5. Correlation Heatmap

**Tool used:** Seaborn

**Purpose:** Show correlation between numeric variables.

In the notebook, a heatmap is used to compare correlations between `total_bill`, `tip`, `size`, and `tip_rate`.

**Why use it:**

A heatmap gives a quick overview of which numeric variables are strongly or weakly related.

**When to use it:**

Use it before modeling or deeper analysis to identify relationships between numeric features.

**Example use case:**

Checking whether bill size and tip amount are strongly correlated.

---

## Interactive Visualization Tools

### 6. Plotly

**Purpose:** Create modern interactive charts.

Plotly is used when the viewer needs to interact with the chart, hover over points, zoom, filter visually, or explore details.

**How it is used in the notebook:**

- Interactive scatter plot.
- Faceted histogram.
- Bubble chart.
- Choropleth map.
- Parallel coordinates plot.
- Sankey diagram using Plotly Graph Objects.

**When to use it:**

Use Plotly when your audience needs exploration rather than only a static image.

---

### 7. Interactive Scatter Plot with Hover

**Tool used:** Plotly Express

**Purpose:** Explore relationships while showing extra information on hover.

In the notebook, this plot shows `total_bill` vs `tip`, with colors for day and symbols for time.

**Why use it:**

Hover information allows the chart to contain more detail without becoming visually crowded.

**When to use it:**

Use it when each point has additional information that the user may want to inspect.

**Example use case:**

Exploring each restaurant bill while also seeing day, time, smoker status, party size, and tip rate.

---

### 8. Small Multiples / Faceted Histogram

**Tool used:** Plotly Express

**Purpose:** Compare the same chart across different groups.

In the notebook, faceting is used to compare tip rate distributions by day.

**Why use it:**

Small multiples avoid putting too many categories into one crowded chart. Each group gets its own mini-chart.

**When to use it:**

Use it when you want to compare patterns across categories.

**Example use case:**

Comparing tipping distributions separately for each day of the week.

---

### 9. Bubble Chart

**Tool used:** Plotly Express

**Purpose:** Show relationships between multiple variables at once.

In the notebook, the Gapminder bubble chart shows GDP per capita, life expectancy, population size, and continent.

**Why use it:**

A bubble chart can communicate four dimensions:

- X-axis variable.
- Y-axis variable.
- Bubble size.
- Bubble color.

**When to use it:**

Use it when you need to tell a multi-variable story in one chart.

**Example use case:**

Showing how GDP per capita and life expectancy differ across countries, while also representing population size.

---

### 10. Choropleth Map

**Tool used:** Plotly Express

**Purpose:** Show geographic patterns.

In the notebook, a choropleth map shows life expectancy by country.

**Why use it:**

Maps make geographic differences easy to understand quickly.

**When to use it:**

Use it when location is important to the analysis.

**Example use case:**

Comparing life expectancy across countries around the world.

---

## Advanced Portfolio Visualizations

### 11. Sankey Diagram

**Tool used:** Plotly Graph Objects

**Purpose:** Show flows between categories.

In the notebook, the Sankey diagram shows flow from `day` to `time` to `smoker` using counts.

**Why use it:**

Sankey diagrams are useful for showing movement, transitions, funnels, or allocation paths.

**When to use it:**

Use it when your data has a flow structure, such as:

- User journey steps.
- Source to destination movement.
- Budget allocation.
- Category transitions.

**Example use case:**

Showing how restaurant visits move from day to meal time to smoker/non-smoker categories.

---

### 12. Parallel Coordinates Plot

**Tool used:** Plotly Express

**Purpose:** Compare many numeric variables at the same time.

In the notebook, parallel coordinates are used to compare `total_bill`, `tip`, `size`, and `tip_rate`.

**Why use it:**

This chart helps reveal multivariate patterns, clusters, and outliers.

**When to use it:**

Use it when you want to compare several numeric features together instead of only two variables.

**Example use case:**

Finding patterns between bill amount, tip amount, group size, and tip rate.

---

## Dashboard Tool

### 13. Altair

**Purpose:** Build clean declarative and interactive visualizations.

Altair is used in the notebook to create a small cross-filter dashboard using the cars dataset.

**How it is used in the notebook:**

- Interactive scatter plot.
- Bar chart linked to the same selection.
- Histogram linked to the same selection.
- Legend-based filtering using `selection_point`.
- Combined layout using `vconcat` and `hconcat`.

**When to use it:**

Use Altair when you want elegant, interactive charts with clean syntax, especially for dashboards and linked visual analysis.

---

### 14. Altair Cross-Filtering Dashboard

**Tool used:** Altair

**Purpose:** Allow users to interactively filter multiple charts at once.

In the notebook, users can click a car origin group in the legend, and the scatter plot, bar chart, and histogram respond together.

**Why use it:**

Cross-filtering makes dashboards more exploratory. Instead of looking at one fixed chart, users can interact with the data and discover patterns.

**When to use it:**

Use it when you want to let users compare groups interactively.

**Example use case:**

Filtering cars by origin to compare horsepower, miles per gallon, and weight distribution.

---

## Feature Engineering in the Notebook

The notebook creates additional columns to make analysis more meaningful:

| Feature | Meaning | Why it is useful |
|---|---|---|
| `tip_rate` | Tip divided by total bill | Makes tipping comparisons fair across different bill sizes |
| `is_weekend` | Whether the day is Saturday or Sunday | Helps compare weekday vs weekend behavior |
| `bill_bucket` | Groups bill values into ranges | Makes bill-size comparisons easier |

---

## Recommended Use of Each Tool

| Tool | Best for | Use when |
|---|---|---|
| Pandas | Data preparation | You need to clean, inspect, filter, or transform data |
| Matplotlib | Static charts | You need simple figures with full control |
| Seaborn | Statistical EDA | You need distributions, comparisons, correlations, or regression plots |
| Plotly | Interactive visuals | You need hover, zoom, maps, bubbles, or modern exploration |
| Plotly Graph Objects | Advanced custom visuals | You need Sankey diagrams or more control than Plotly Express |
| Altair | Interactive dashboards | You need linked charts and cross-filtering |

---

## How to Run the Notebook

1. Open the notebook in Jupyter Notebook, JupyterLab, or Google Colab.
2. Run the installation cell if needed:

```python
!pip -q install --upgrade seaborn plotly altair vega_datasets kaleido
```

3. Run the notebook cells from top to bottom.
4. Interact with the Plotly and Altair visualizations directly inside the notebook.

---

## Main Learning Outcome

By completing this notebook, you learn that visualization is not only about creating attractive charts. Each chart type has a specific analytical purpose:

- Histograms reveal distributions.
- Scatter plots reveal relationships.
- Box plots compare groups.
- Bar plots summarize categories.
- Heatmaps reveal correlations.
- Bubble charts tell multi-variable stories.
- Maps reveal geographic patterns.
- Sankey diagrams show flows.
- Parallel coordinates show multivariate structure.
- Dashboards support interactive exploration.

This makes the notebook useful as both a learning exercise and a portfolio project.
