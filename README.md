# Orvid search

Search engine repository for [Orvid](https://github.com/mankidev/orvid). It sends your search to DuckDuckGo and Yandex video search and lists the videos they find on any site. Videos from sites Orvid knows play through that source; other pages play through Orvid's generic player.

Search engines block Tor, so these sources work only when Tor is turned off. While Tor is off, the search engine sees your IP address and your search.

To add it, open Filters → Repositories → Add repository in Orvid and paste:

```
https://raw.githubusercontent.com/mankidev/orvid-search/main/
```

The source format is described in [orvid-sources](https://github.com/mankidev/orvid-sources#source-format). A source with `"portal": true` needs no `match` and keeps every link it finds. `"torless": true` turns a source off while Tor is on. `python3 tools/build.py` signs the index with the key in `ORVID_SEARCH_KEY`.

## License

GPL-3.0-or-later.
