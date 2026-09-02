# arcfpga-mister-db

[Custom database](https://github.com/MiSTer-devel/Downloader_MiSTer/blob/main/docs/custom-databases.md)
for the [MiSTer Downloader](https://github.com/MiSTer-devel/Downloader_MiSTer), distributing the
FPGA arcade cores built in **[arcfpga-cores](https://github.com/bmo00/arcfpga-cores)** — arcade
cores built on Jose Tejada's (jotego) [JTFRAME](https://github.com/jotego/jtframe) framework, with
an added **neptUNO+** target.

## Installation

There are two ways to integrate this database into your MiSTer.

The easiest option is to use the generated drop-in database. Download:

https://raw.githubusercontent.com/bmo00/arcfpga-mister-db/db/downloader_bmo00_arcfpga-mister-db.zip

Then extract `downloader_bmo00_arcfpga-mister-db.ini` from that ZIP file and place it either next
to `downloader.ini`, in the root of your MiSTer's SD card, or inside the `downloader` directory
also in the SD card's root — both locations are picked up automatically.

If you prefer to do it manually instead, add the following lines to the bottom of
`downloader.ini`:

```ini
[bmo00/arcfpga-mister-db]
db_url = https://raw.githubusercontent.com/bmo00/arcfpga-mister-db/db/db.json.zip
```

Either way, this only needs to be done once. After that, whenever you run *downloader* or
*update_all* you'll also be fetching and updating the cores distributed here.

## Source

Core source (HDL, config, per-core documentation) lives at
[bmo00/arcfpga-cores](https://github.com/bmo00/arcfpga-cores) — this repository only carries the
built binaries and the database manifest the MiSTer Downloader reads.

## Release table

| Core | Ported from | Release date | Notes |
| --- | --- | --- | --- |
| mystston | Original | 2026-08-26 | Bug: Flickering horizontal lines. |

## Credits

- [Jose Tejada (jotego)](https://github.com/jotego) — [JTFRAME](https://github.com/jotego/jtframe) and [jtcores](https://github.com/jotego/jtcores), the framework and core collection this project builds on (0 ported cores in this database).
- The MiSTer open-source FPGA arcade community.
