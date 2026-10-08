# Superhero Hunter

A front-end web application where users can search for superheroes, add them to a favorites list, and view detailed information about each hero. It is built with plain HTML, CSS, and JavaScript and gets its data from [SuperHero API](https://superheroapi.com/).

## Features and Functionality

### 1) Search for any superhero
Users can search for any superhero by typing the name into the search bar. Results update as you type and show each matching hero's name and image.

### 2) Add to favorites
Users can add the superheroes they like to their favorites list using the "Add to Favourites" button on a search result.

### 3) View favorites
Users can view all their favorite superheroes on the Favorites page, and delete any superhero from the list.

### 4) Get information
Users can click on a superhero card to view its details:
- Power stats: intelligence, strength, speed, durability, power, combat
- Name and real (full) name
- Alignment (good or bad)
- Appearance: gender, race, height, weight, eye color, hair color

## Tech Stack

- HTML, CSS, and vanilla JavaScript (no build step or dependencies)
- `XMLHttpRequest` calls to SuperHero API
- Browser `localStorage` to store favorites and the currently selected hero
- Font Awesome kit (loaded from a CDN on the Favorites page for the delete icon)

## Project Structure

```
Superhero Hunter/
├── index.html                 # Home page with the search bar and results
├── scriptIndex.js             # Search, add/remove favorites, open hero details
├── styleIndex.css
├── favouritesuperHeroes.html  # Favorites page
├── scriptFavourites.js        # Loads favorite heroes, delete from favorites
├── styleFavourites.css
├── heroInfo.html              # Hero details page
├── scriptHeroInfo.js          # Loads and displays the selected hero's details
├── styleHeroInfo.css
├── good.jpg                   # Alignment image for "good" heroes
└── bad.jpg                    # Alignment image for other heroes
```

## Getting Started

### Prerequisites
- A modern web browser
- An internet connection (all hero data is fetched from SuperHero API)

### Run locally

1. Clone the repository:
   ```bash
   git clone https://github.com/iSouvikKhan/Hero.git
   cd "Hero/Superhero Hunter"
   ```
2. Open `index.html` in your browser. You can double-click the file, or serve the folder with any static file server, for example:
   ```bash
   python -m http.server 8000
   ```
   and then visit `http://localhost:8000`.

## Usage

1. Type a superhero's name into the search bar on the home page.
2. Click "Add to Favourites" on a result to save it. The button changes to "Favourite" once saved.
3. Click "Favorites" in the header to see your saved heroes; use the trash button to remove one.
4. Click any hero card (in the search results or on the Favorites page) to open its details page.

Favorites are stored in your browser's `localStorage`, so they persist between visits in the same browser but are not shared across browsers or devices.

## Notes

- The SuperHero API access token is embedded in the request URLs in the JavaScript files. If requests fail, you may need to replace it with your own token from [superheroapi.com](https://superheroapi.com/).
- Removing a hero from favorites is most reliable from the Favorites page.
