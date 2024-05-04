# Song Recommendendation Engine

## Overview
This repository contains a Python script designed to simulate a music recommender system. The script analyses user ratings of songs across various genres and utilises this data to predict user preferences and recommend new songs. The code leverages libraries such as `numpy`, `pandas`, and `sklearn` to manage data and compute similarities between user preferences.

## Data Structure
The dataset within the script includes:
- **Track ID:** A unique identifier for each song.
- **Song Title:** The name of the song.
- **Artist:** The artist who performed the song.
- **Genre:** The musical genre of the song.

This data is stored in a pandas DataFrame, which facilitates easy manipulation and analysis of the song information.

## User Ratings
User ratings are simulated in the script to demonstrate how the system would function with real user data. Each user rates a subset of songs, and these ratings are then used to determine user preferences across different genres. 

Example of User 1's Song Ratings:

| Song Title               | Rating | Genre   |
|--------------------------|--------|---------|
| Where You Are            | 3.0    | Dance   |
| Rhyme Dust               | 2.0    | Dance   |
| Padam Padam              | 3.0    | Dance   |
| Miracle                  | 5.0    | Dance   |
| ...                      | ...    | ...     |
| Die for You              | 2.0    | Pop     |
| Last Christmas           | 4.0    | Pop     |

## Recommendation Strategy
The recommender system calculates the cosine similarity between users based on their ratings and suggests songs from the genre most favoured by similar users. The system identifies the user's favourite genre based on the average rating given to each genre and selects songs from that genre which have not been rated by the user.

## Results for User 1
The recommender system determined that Pop was User 1's favourite genre based on the average ratings provided. Subsequently, the following songs were recommended:

| Track ID | Song Title    | Artist         | Genre |
|----------|---------------|----------------|-------|
| t68      | Boy's a Liar  | PinkPantheress | Pop   |
| t71      | Cruel Summer  | Taylor Swift   | Pop   |
| t70      | People        | Libianca       | Pop   |
| t66      | Calm Down     | Rema           | Pop   |
| t77      | Die for You   | The Weeknd     | Pop   |

## Conclusion
This script effectively demonstrates the basic functionality of a music recommender system. Enhancements can include more sophisticated user interaction simulations, integration with real user data, and advanced recommendation algorithms to further refine song suggestions.

## Dependencies
- Python 3.8+
- NumPy
- Pandas
- Scikit-Learn
