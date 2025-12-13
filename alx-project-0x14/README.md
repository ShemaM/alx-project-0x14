# MoviesDatabase API

## API Overview

The MoviesDatabase API provides developers with access to a vast collection of movie, series, and episode data. It covers over **9 million titles** and **11 million actors/crew members**, offering details such as:

- Title information (plots, genres, runtime, release dates)
- Ratings and votes
- Cast and crew details
- Awards and biographies
- YouTube trailer URLs
- Upcoming releases

Data is updated regularly: titles weekly, ratings and episodes daily.

## Version

Current API Version: **v1**

## Available Endpoints

- **/titles** – Retrieve multiple titles with filters (genre, year, type, etc.).
- **/titles/{id}** – Get detailed information for a specific title by IMDb ID.
- **/titles/{id}/ratings** – Fetch ratings and vote counts for a title.
- **/titles/series/{id}** – Get episodes for a series by ID.
- **/titles/seasons/{id}** – Retrieve the number of seasons for a series.
- **/titles/series/{id}/{season}** – Get episodes for a specific season.
- **/titles/episode/{id}** – Retrieve details for a specific episode.
- **/titles/x/upcoming** – List upcoming titles.
- **/titles/search/keyword/{keyword}** – Search titles by keyword.
- **/titles/search/title/{title}** – Search titles by exact or partial title.
- **/titles/search/akas/{aka}** – Search titles by alternative names.
- **/actors** – Retrieve a list of actors with filters.
- **/actors/{id}** – Get detailed information about a specific actor.
- **/title/utils/titleType** – List available title types.
- **/title/utils/genres** – List available genres.
- **/title/utils/lists** – Access predefined lists (e.g., top rated, most popular).

## Request and Response Format

### Request

Requests are made via **HTTP GET** with optional query parameters:

```http
GET /titles?limit=10&genre=Action&startYear=2020&endYear=2025
