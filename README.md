# Spotify API Documentation

This repository provides a collection of requests to interact with the Spotify Web API using OAuth 2.0 for authorization. The requests include retrieving user profiles, managing playlists, and searching for tracks. The requests are organized by type (GET, POST) and purpose.

## Authorization
All requests in this collection use OAuth 2.0 for authorization. Ensure you have a valid access token from Spotify's OAuth 2.0 authentication flow to use these requests.

## Requests

### GET User Profile
Retrieve information about the current authenticated user.

- **Endpoint:** `GET users/`
- **Authorization:** OAuth 2.0 (from collection Spotify)

### GET My Playlists
Retrieve a list of playlists owned or followed by the current Spotify user.

- **Endpoint:** `GET users/{user_id}/playlists`
- **Authorization:** OAuth 2.0 (from collection Spotify)

### GET Playlist Image
Retrieve the images for a specific playlist.

- **Endpoint:** `GET playlists/{playlist_id}/images`
- **Authorization:** OAuth 2.0 (from collection Spotify)
- **Request Headers:**
  - `Content-Type: application/json`

### GET Playlist Items
Retrieve the items (tracks) of a specific playlist.

- **Endpoint:** `GET playlists/4VHOpzgncQMU4RlEjUcgQJ/tracks`
- **Authorization:** OAuth 2.0 (from collection Spotify)

### POST Create Playlist
Create a new playlist for the current user.

- **Endpoint:** `POST users/{user_id}/playlists`
- **Authorization:** OAuth 2.0 (from collection Spotify)
- **Body:**
  ```json
  {
      "name": "Postman",
      "description": "Customize Playlist",
      "public": true
  }
  ```

### GET Search Artist Top-Tracks
Retrieve the top tracks of a specific artist.

- **Endpoint:** `GET artists/4gzpq5DPGxSnKTe4SA8HAU/top-tracks`
- **Authorization:** OAuth 2.0 (from collection Spotify)

### POST Add Items to Playlist
Add tracks to a specific playlist.

- **Endpoint:** `POST playlists/{playlist_id}/tracks`
- **Authorization:** OAuth 2.0 (from collection Spotify)
- **Body:**
  ```json
  {
      "uris": [],
      "position": 0
  }
  ```

## About Me
This collection is created to demonstrate and document various endpoints of the Spotify Web API, providing a comprehensive guide to performing common tasks such as retrieving user information, managing playlists, and searching for music tracks. Ensure you have the necessary authorization before making requests.

For more detailed information on Spotify's Web API, visit the official [Spotify Developer Documentation](https://developer.spotify.com/documentation/web-api/).
