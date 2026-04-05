# market-discovery-agent
🧵 Market Trend Discovery Agent

An automated workflow for identifying and synthesizing emerging rug and home decor trends using real-time data from editorial sources, search behavior, and retail product signals.

✨ Overview
The Market Trend Discovery Agent is an AI-assisted pipeline built in n8n that:

Classifies user intent

Aggregates data from multiple sources

Extracts structured product and article signals

Synthesizes insights into a readable trend report

The system is designed to mimic how a human analyst would identify trends—by combining editorial direction, search demand, and retail availability.

🔍 Problem
Understanding market trends in home decor requires manually:

Monitoring multiple editorial sources

Tracking search behavior

Reviewing retail listings

Identifying patterns across all three

This process is time-consuming, inconsistent, and difficult to scale.

⚙️ Solution
This project automates that process using a multi-stage workflow:

1. Intent Classification
Determines whether a user query is trend-related using an LLM-based classifier.

2. Data Aggregation
Pulls recent data from:

RSS feeds (industry blogs & publications)

Google Custom Search

Amazon product and collection links

3. Data Extraction
Scrapes product details (title, price, features, patterns)

Extracts article content and metadata

Normalizes structured data across sources

4. Signal Processing
Filters recent content (last 7 days)

Groups and enriches product and article signals

Handles missing or failed sources gracefully

5. Trend Synthesis
Combines all signals into a structured trend report including:

Executive summary

Identified trends

Supporting evidence

Product attributes (color, material, style, etc.)

🧠 Key Features
Multi-source aggregation
Combines editorial, search, and retail data into a single analysis pipeline

Resilient architecture
Continues generating insights even when sources fail (e.g., Amazon scraping)

Structured outputs
Produces consistent, analyzable trend reports

Automated signal filtering
Focuses on recent and relevant data (last 7 days)

Extensible design
New data sources and classifiers can be added easily

📊 Example Output
The workflow generates structured trend reports like:
![trend summary](<assets/Screenshot 2026-04-05 at 3.57.15 PM.png>)


Executive Summary

Trend Signals (e.g., “Soft Neutral Foundations”, “Washable Vintage Revival”)

Key Attributes

Colors

Materials

Patterns

Styles

Features

Supporting Evidence

Articles

Search results

Product examples




⚠️ Limitations

Amazon scraping instability

Amazon frequently changes its structure, which can break scraping logic

Dependence on external sources

Availability and consistency of RSS/search data may vary

LLM variability

Output quality depends on prompt design and model behavior


🚀 Future Improvements

Replace Amazon scraping with more stable product APIs

Add historical trend comparison (week-over-week analysis)

Improve entity extraction and clustering

Build a lightweight frontend for report exploration

Add visualization (trend frequency, attribute distribution)


🛠️ Tech Stack

n8n – workflow orchestration

Google Custom Search API – search data

LLMs (Gemini / LangChain nodes) – classification and synthesis

JavaScript (n8n code nodes) – data transformation

Cheerio – HTML parsing for scraping


📌 Notes

This project focuses on data orchestration and insight generation, not UI.

A prototype frontend was explored but is not included as part of the final deliverable.


💡 Key Takeaway

This project demonstrates how AI + automation + multi-source data pipelines can be combined to generate structured, human-readable market insights—reducing manual research effort and improving consistency.
