# Track Retriever

Built to make it easier for people to work with the tracks in their Spotify playlists 

### Prerequisites

I assume that you have already made a Spotify project, if not you can do that [here](https://developer.spotify.com/dashboard/)

```
You'll need your: username, client_id, client_secret, redirect_uri and userId 
```

### Installing

```
pip install trackRetriever
``` 

## Functions 

I made getPlaylistIds and get_playlist_tracks as helpers for getTracks but you are more than welcome to use them

```
getTracks(username, client_id, client_secret,redirect_uri,getNames = False)

All the parameters should be input as string except getNames
When getNames is set to True getTracks will return a list of the names of the tracks in your playlists
When getNames is set to False getTracks will return a list of the track id's of the tracks in your playlists 
```

```
getPlaylistIds(playlists)

This will get the playlist id's of your playlists 
playlists = sp.user_playlists(userId) *userId is not your username* 
```

```
get_playlist_tracks(userId, playlist_id,sp)

sp is the spotify object created by spotipy.Spotify(auth=token)
playlist_id is the id of the playlist you want to retrieve the tracks for 
```