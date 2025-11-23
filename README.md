# spotify-cli

`spotify-cli` is a Python script for downloading Spotify tracks as MP3 files via YouTube.  
Currently, only individual track downloads are supported (no playlists or albums yet).  

It performs the following steps:  
1. Parses a Spotify track link to extract information: track title, artist, album, release year.  
2. Uses [`ytmusicapi`](https://github.com/sigma67/ytmusicapi) to search for the track on YouTube Music.  
3. Downloads the track with [`yt-dlp`](https://github.com/yt-dlp/yt-dlp) and converts it to MP3.  
4. Uses `ffmpeg` for conversion, which must be placed in a folder named `ffmpeg` next to the script.

---

## Requirements

- Python 3.8+  
- Windows OS
- Python modules (can be installed via pip):
```bash
pip install colorama requests beautifulsoup4 ytmusicapi yt-dlp
