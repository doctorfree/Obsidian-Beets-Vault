---
banner: "assets/banners/Dataview-Banner.png"
banner_x: 0.8
banner_y: 0.2
---

# Beets Queries

The Obsidian Beets Vault markdown contains metadata with tags allowing a variety of queries using the [Dataview](https://blacksmithgu.github.io/obsidian-dataview/) plugin for [Obsidian](https://obsidian.md/).

For example, the markdown for "Fragile" by Yes has the following YAML prelude:

```yaml
---
catalog: Beets
album: Fragile
artist: Yes
format: Digital, Album
albumartist: Yes
genre: Progressive Rock
mb_albumartistid: c1d4f2ba-cf39-460c-9528-6b827d3417a1
mb_albumid: dc792622-a22b-3268-8d7f-8bc27b60b907
mb_releasegroupid: b1176e7b-fa2e-3b28-959a-d8f55b5b6ccf
year: 1977
---
```

## Dataview

The above album metadata can be used to perform Dataview queries to search, filter, and retrieve albums as if they are in a database. For example, to produce a table of all albums in this vault by Yes released prior to 1980 add the following to a markdown file in the vault:

````markdown
```dataview
TABLE
  album AS "Title",
  albumartist AS "Artist",
  year AS "Year"
FROM "Beets"
WHERE albumartist = "Yes" and year < 1980
SORT year ASC
```
````

The above Dataview code block produces the following output:

```dataview
TABLE
  album AS "Title",
  albumartist AS "Artist",
  year AS "Year"
FROM "Beets"
WHERE albumartist = "Yes" and year < 1980
SORT year ASC
```

### Beets albums filtered with Dataview queries

- [All Beets Albums](Dataviews/Beets_Albums.md)
- [Beets Albums released in 1977](Dataviews/Beets_Albums_1977.md)
- [Beets Albums released in the 70s](Dataviews/Beets_Albums_70s.md)
- [Beets Albums in a Progressive genre](Dataviews/Beets_Progressive.md)

## See also

- [Index of the Beets Vault](Beets_Albums_by_Artist.md)
- [README](README.md)
- [Process](Process.md)
