# Spotify Playlist Word Cloud Generator

This project is a prototype for generating a Word Cloud based on the lyrics of songs from a user's Spotify playlist. It demonstrates how to integrate data from multiple APIs (Spotify and Genius) and utilize text processing techniques to create a visual representation of the most common words in the lyrics.

## Table of Contents

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [APIs Used](#apis-used)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project retrieves tracks from a user's Spotify playlist and fetches the corresponding song lyrics from the Genius API. It processes the lyrics by removing stopwords and creates a word cloud based on the frequency of the words. The final word cloud is displayed and saved as an image, which can be used as a playlist cover.

### Key Components:

1. **Spotify API**: Fetches playlist and track data from a Spotify account.
2. **Genius API**: Retrieves song lyrics for the tracks in the playlist.
3. **Word Cloud Generator**: Uses Matplotlib's `WordCloud` library to create a visual representation of word frequencies in the song lyrics.

## Installation

### Prerequisites

- Python 3.x
- Jupyter Notebook or Google Colab
- Spotify Developer Account
- Genius API Key

### Install Required Libraries

The necessary libraries can be installed with the following command:

```bash
pip install lyricsgenius nltk wordcloud matplotlib requests
```

If running in **Google Colab**, install the required libraries inside the notebook:

```python
!pip install lyricsgenius
```

## Usage

1. **Set Up API Credentials**:
   - **Spotify API**: Set up your Spotify API credentials (Client ID, Client Secret, and Redirect URI) through the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/login). These credentials should be securely stored in environment variables or in the notebook’s SECRETS tab.
   - **Genius API**: Obtain your Genius API access token from [Genius API](https://genius.com/developers) and store it securely.

2. **Run the Notebook**:
   - Open the `data_feature_1.ipynb` notebook in Jupyter or Colab and execute the cells.
   - Authorize access to your Spotify account using the provided URL and paste the authorization code into the notebook.

3. **Word Cloud Generation**:
   - The notebook will retrieve the tracks from your Spotify playlist, fetch the corresponding lyrics from the Genius API, and generate a word cloud based on the lyrics. 
   - The word cloud will be displayed in the notebook and saved as a PNG image in your working directory.

## APIs Used

- **Spotify API**: Retrieves the user's playlists and track information.
- **Genius API**: Fetches the song lyrics for tracks in the user's playlist.

## Features

- Retrieve a list of Spotify playlists and their tracks.
- Fetch lyrics for each track from the Genius API.
- Perform text processing using the `nltk` library to remove stopwords and clean the lyrics.
- Generate and display a word cloud based on the most common words in the lyrics.
- Save the word cloud as an image for use as a playlist cover.

## Contributing

If you would like to contribute to this project, feel free to submit a pull request or open an issue to discuss potential changes.

## License

This project is licensed under the MIT License.
