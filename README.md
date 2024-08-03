# Movie Recommendation System

This project is a movie recommendation system that suggests movies based on a user's favorite movie. It uses cosine similarity to find movies with similar features such as genres, keywords, taglines, cast, and directors. The dataset is sourced from a CSV file containing movie information.

## Features

- **Content-Based Filtering**: The system recommends movies similar to the user's input movie by analyzing the content features of the movies.
- **TF-IDF Vectorization**: The text data from selected features are converted into feature vectors using the TF-IDF Vectorizer.
- **Cosine Similarity**: Similarity between movies is calculated using cosine similarity, helping identify movies with the closest content features.

## Dataset

The dataset consists of the following features:

- `genres`
- `keywords`
- `tagline`
- `cast`
- `director`
- `title`

## Installation

To run this project locally, you'll need to have Python installed. You can install the required libraries using the following command:

```sh
pip install numpy pandas scikit-learn

```
## Usage

1. **Load the dataset**: The data is loaded from a CSV file (`movies.csv`) into a pandas DataFrame.

2. **Data Preprocessing**:
   - Missing values in selected features are replaced with empty strings.
   - The selected features are combined into a single feature.

3. **Feature Vectorization**:
   - The combined features are converted into feature vectors using the TF-IDF Vectorizer.

4. **Calculate Similarity**:
   - The cosine similarity scores are calculated based on the feature vectors.

5. **Get Recommendations**:
   - The user inputs their favorite movie's name.
   - The system finds the closest match for the input movie in the dataset.
   - It retrieves the index of the movie and finds similar movies based on similarity scores.
   - The top similar movies are recommended to the user.
  

## Example

To run the recommendation system, execute the script and input your favorite movie name when prompted. The system will then output a list of similar movies based on your input.

 ```sh
Enter your favourite movie name: Inception
Movies suggested for you:
1. Inception
2. The Dark Knight
3. Interstellar
...
```
## Contributing

Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

Special thanks to the open-source community for providing the tools and libraries used in this project.
