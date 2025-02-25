# Word-Clustering
This project implements a word clustering algorithm using Word2Vec embeddings to categorize words into predefined categories. The algorithm uses cosine similarity to measure the semantic similarity between words and categories, allowing for efficient and accurate classification.

### Key Features:

1. **Word2Vec Integration**: Utilizes pre-trained Google News vectors for word embeddings.
2. **Compound Word Handling**: Custom function to process compound words by combining vectors of individual words.
3. **Cosine Similarity Calculation**: Implements cosine similarity to measure semantic closeness between words and categories.
4. **Flexible Input Processing**: Handles various input formats, including compound words and special characters.
5. **Predefined Categories**: Uses a set of predefined categories for classification.
6. **CSV Output**: Generates a CSV file with word IDs, original words, and assigned categories.

### Implementation Details:

- **Input**: Takes a text file ('catname.txt') containing word IDs and words.
- **Preprocessing**: Cleans and standardizes input data, handling compound words and special characters.
- **Model**: Uses gensim to load pre-trained Word2Vec embeddings.
- **Classification**: Computes similarity between each input word and predefined categories, assigning the most similar category.
- **Output**: Produces a CSV file ('Project_Output.csv') with classification results.
- 
## Dataset
The input dataset (catname.txt) contains 446 venue types organized by ID ranges:

- 1001-1036: Entertainment venues (Amphitheater, Museum, Zoo, etc.)
- 2001-2023: Educational institutions (Universities, Libraries, etc.)
- 4001-4090: Food establishments (Restaurants, Cafes, etc.)
- 5001-5008: Nightlife venues (Bars, Nightclubs, etc.)
- 6001-6057: Outdoor locations (Parks, Mountains, etc.)
- 7001-7037: Professional venues (Offices, Government buildings, etc.)
- 8001-8005: Residential places (Homes, Apartments, etc.)
- 9001-9138: Shops and services (Stores, Salons, etc.)
- 10001-10033: Transportation hubs (Airports, Train stations, etc.)


## Results
The algorithm successfully categorized 446 venue types into 9 distinct clusters with some interesting insights:

Some venues were classified differently than their ID ranges might suggest (e.g., "Art Gallery" classified as "Residence" rather than "Arts & Entertainment")
The model identified cross-category relationships between seemingly different venues
A small set of venues (marked as "Category unknown") required additional analysis

### Use Case:

This project is particularly useful for tasks such as:

- Automated content categorization
- Semantic analysis of large text datasets
- Improving search and recommendation systems


### Requirements:

- Python 3.x
- NumPy
- Pandas
- Gensim
- Pre-trained Google News vectors file


### Future Improvements:

- Implement dynamic category generation
- Explore other embedding models for comparison
- Add support for multi-language classification

# Run the clustering algorithm
python cluster.py --input catname.txt --output results.csv
