# Vision ∞ Shop: The Navigation App

Vision ∞ Shop is a navigation app designed to help users navigate a supermarket. It uses image recognition, speech recognition, and route planning to guide visually-impaired users to their desired products within the store.

## Features

- **Image Upload and OCR**: Users can upload images, which are processed using Optical Character Recognition (OCR) to detect text.
- **Speech Recognition**: The app uses speech recognition to understand the user's spoken requests for products.
- **Database Queries**: It connects to a database to retrieve information about product locations, discounts, and regions within the supermarket.
- **Route Planning**: The app calculates the optimal route from the user's current location to the desired product using A* search algorithm.
- **Audio Guidance**: The app provides audio instructions to guide the user along the planned route.

## Installation

1. Clone the repository

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Run the Streamlit app:
    ```bash
    streamlit run src/app.py
    ```

2. Open your web browser.

3. Upload an image of your current location in the supermarket.

4. If this is the first image, press the "Start Navigation" button to begin navigation.

5. For subsequent images, the app will automatically update your location and provide new directions.

## Database

SQL is used to query the database containing product, region and supermarket data. The database is stored in shop.db file while the specific data used is shown in the csv files. The data in the .db file can be modified using sqlite3 or other database engines for customized products and supermarket layouts.

The supermarket map is expressed in a coordinate graph, where A* algorithm is used to determine the shortest path between two grids in the map.

<div align="center">
  <img src="assets/readme/map.png" alt="map image" width="400"/>
</div>