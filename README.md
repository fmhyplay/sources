# AnantPlay sources

Title links and playlists that [AnantPlay](https://github.com/AnantPlay/android) offers through its [index](https://github.com/AnantPlay/index). They live in their own repository so the app carries no links, and so they can be updated without a new app release.

| File | What it is |
| --- | --- |
| `deeplinks.json` | Title-page address templates for streaming sites (`/movie/{tmdb}`, `/tv/{tmdb}`, episodes, anime with Sub / Dub) |
| `lists/*.m3u` | Playlists, one file per source, with names cleaned up and streams checked reachable on the day they were made |
| `sources.txt` | The list app versions 2.20.1 and older read; kept so they work until they update |

## `deeplinks.json`

    {"host.example": {"movie": "/movie/{tmdb}", "tv": "/tv/{tmdb}", "episode": "/tv/{tmdb}/{season}/{episode}"}}

`{tmdb}` and `{imdb}` are the title's ids; `{season}` and `{episode}` the episode; anime addresses can use `{anilist}`, `{mal}`, `{kitsu}`, `{anidb}` and `{audio}` (with an `audio` map for Sub / Dub).

`"@late": ["name", ...]` lists sites (host names without the ending) that check the browser's own `fetch` as they start; AnantPlay hooks those late so they still load.

## Contributing

Open an issue or a pull request with a playlist link or address pattern that works. Entries that stop working are removed. The playlists belong to their owners; this repository hosts links and a small amount of metadata, not video.
