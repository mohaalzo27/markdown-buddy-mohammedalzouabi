# Synthetic Retail Sales EDA

AI Assistance Declaration: I used Grok (xAI, Grok 4.7, October 26, 2026) for ideation of README structure, drafting Markdown content, refining section organization, and suggesting R Markdown formatting. Prompts used: "Explain what sections a good GitHub README for an R data analysis project should include."; "Here's a summary of my R project: [summary]. Generate a professional README.md file using Markdown."; "Add sections for Installation, Example Code, and License. Keep tone concise and professional."; "Review the Markdown for syntax errors and suggest 2 improvements for clarity."; "Here's my R script description. Suggest Markdown formatting and code block examples." I verified outputs by previewing Markdown rendering, comparing to tidyverse-style READMEs, and manually editing for accuracy, clarity, and originality. All final content decisions are my own. I am responsible for the accuracy and originality of this work.

## Overview

This project performs exploratory data analysis (EDA) on a synthetic retail sales dataset. It loads the data, cleans missing values and outliers, summarizes sales by region and product category, and creates visualizations to identify trends over time. The analysis supports basic business insights such as top-performing categories and seasonal patterns. All data is synthetic and contains no real customer or business information.

## Installation

Clone the repository and open the project in RStudio or Posit Cloud.

```r
# Install required packages (run once)
install.packages(c("tidyverse", "lubridate"))
```

Then load the packages in your script or R Markdown file:

```r
library(tidyverse)
library(lubridate)
```

## Project Structure

- `sales_eda.R` — Main analysis script
- `sales_eda_documentation.Rmd` — R Markdown documentation of the script
- `data/synthetic_sales.csv` — Synthetic input dataset (not included in this minimal repo; generate or download as needed)
- `README.md` — This file

## Example Usage

The main script follows a standard tidyverse workflow:

```r
# Load and clean data
sales <- read_csv("data/synthetic_sales.csv") %>%%
  mutate(date = ymd(date)) %>%%
  filter(!is.na(sales_amount)) %>%%
  mutate(month = floor_date(date, "month"))

# Summarize by category
category_summary <- sales %>%%
  group_by(category) %>%%
  summarise(
    total_sales = sum(sales_amount),
    avg_units = mean(units),
    .groups = "drop"
  )

# Create a simple bar chart
ggplot(category_summary, aes(x = reorder(category, total_sales), y = total_sales)) +
  geom_col(fill = "steelblue") +
  coord_flip() +
  labs(title = "Total Sales by Category", x = "Category", y = "Total Sales")
```

## Dependencies

- R (>= 4.2)
- tidyverse
- lubridate

## License

MIT License. See LICENSE file for details (optional for this assignment).

## AI Assistance Disclosure

This README was drafted with assistance from Grok (xAI, Grok 4.7, October 26, 2026). Main prompts included requests for standard README sections for an R project, generation of a full draft from a project summary, and refinements for Installation, Example Code, and License sections. After reviewing the output, I edited the tone for conciseness, verified Markdown syntax by previewing headers and code blocks, added the project structure section for clarity, and confirmed all content matched the synthetic data scope. No real data or personal information was shared with the AI tool.
