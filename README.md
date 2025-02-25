# Word-Clustering
Project Overview
This project implements an automated classification system for venue categories using machine learning techniques. It processes a comprehensive dataset of venue types (1001-10033) and classifies them into 9 distinct high-level categories:

Arts & Entertainment
College & University
Food
Nightlife Spot
Professional & Other Places
Recreation & Outdoors
Residence
Shop & Service
Travel & Transport

## Dataset
The input dataset (catname.txt) contains 446 venue types organized by ID ranges:

1001-1036: Entertainment venues (Amphitheater, Museum, Zoo, etc.)
2001-2023: Educational institutions (Universities, Libraries, etc.)
4001-4090: Food establishments (Restaurants, Cafes, etc.)
5001-5008: Nightlife venues (Bars, Nightclubs, etc.)
6001-6057: Outdoor locations (Parks, Mountains, etc.)
7001-7037: Professional venues (Offices, Government buildings, etc.)
8001-8005: Residential places (Homes, Apartments, etc.)
9001-9138: Shops and services (Stores, Salons, etc.)
10001-10033: Transportation hubs (Airports, Train stations, etc.)

## Methodology
The project employs unsupervised learning techniques to identify patterns and similarities between different venue types. Rather than relying on the numeric ID prefixes alone, the algorithm analyzes the semantic relationships between venue descriptions to create more nuanced categorizations.
Key techniques utilized:

Text preprocessing and feature extraction
Unsupervised learning algorithms for clustering
Semantic analysis of venue descriptions
Category prediction for unlabeled venues

## Results
The algorithm successfully categorized 446 venue types into 9 distinct clusters with some interesting insights:

Some venues were classified differently than their ID ranges might suggest (e.g., "Art Gallery" classified as "Residence" rather than "Arts & Entertainment")
The model identified cross-category relationships between seemingly different venues
A small set of venues (marked as "Category unknown") required additional analysis

## Applications
This classification system can be applied to:

Location-based recommendation systems
Urban planning and zoning analysis
Business intelligence for retail and hospitality industries
Social network platforms with location features

## Future Work
Potential improvements and extensions include:

Implementing a supervised learning approach with human-verified labels
Expanding the dataset with international venue types
Adding hierarchical subcategories for more granular classification
Incorporating geographical context to improve accuracy

## Technologies Used

Python
Scikit-learn
Pandas
Natural Language Processing libraries
Data visualization tools

Installation and Usage
Copy# Clone the repository
git clone https://github.com/yourusername/venue-category-clustering.git

# Install dependencies
pip install -r requirements.txt

# Run the clustering algorithm
python cluster.py --input catname.txt --output results.csv
