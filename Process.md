# Process

Several custom scripts and utilities were used to automate the generation of markdown files in the Obsidian Beets Vault. To index and categorize a [Beets music library](https://beets.io/), the [MusicPlayerPlus](https://github.com/doctorfree/MusicPlayerPlus#readme) package can be used. MusicPlayerPlus provides command line utilities that can be used to query, list, and manage various aspects of a Beets library. The scripts used to produce the Beets markdown for this repository can be found in `Tools/Beets/`. Example Beets markdown can be viewed at:

- [Beets Albums by Artist](Beets_Albums_by_Artist.md)

## Overview

If your media libraries are cataloged in an online service such as [Discogs](https://discogs.com) or [Goodreads](https://goodreads.com) or in a media management system such as [CLZ Music](https://connect.collectorz.com) or [Invelos DVD Profiler](http://www.invelos.com/) then it is usually possible to export your online library to a file format that can be converted to markdown. Usually there is an option to export the data to CSV format and that is typically what I used although in some cases all that is available is XML format. Either will work although CSV format is much easier to parse using `csvkit`.

The first step is gathering data sources. That step, for this vault, was exporting data from my Beets library to files in a format that I could manipulate locally. In Beets this is easily accomplished with the `beet info ...` command and other Beets queries.

## See_also

- [README](README.md)
- [Media Queries](Media_Queries.md)

