# arcfpga-mister-db

[Custom database](https://github.com/MiSTer-devel/Downloader_MiSTer/blob/main/docs/custom-databases.md)
for the [MiSTer Downloader](https://github.com/MiSTer-devel/Downloader_MiSTer), distributing the
FPGA arcade cores built in **[arcfpga-cores](https://github.com/bmo00/arcfpga-cores)** — arcade
cores built on Jose Tejada's (jotego) [JTFRAME](https://github.com/jotego/jtframe) framework, with
an added **neptUNO+** target.

## Installation

Add the following to the bottom of `downloader.ini`, on the root of your MiSTer's SD card:

```ini
[bmo00/arcfpga-mister-db]
db_url = https://raw.githubusercontent.com/bmo00/arcfpga-mister-db/db/db.json.zip
```

Then run *downloader* or *update_all* as usual — this only needs to be done once. Every later run
will also fetch and update the cores distributed here.

## Other platforms

The same cores are also available for **neptUNO+**, built from the same source at
[bmo00/arcfpga-cores](https://github.com/bmo00/arcfpga-cores).

## Source

Core source (HDL, config, per-core documentation) lives at
[bmo00/arcfpga-cores](https://github.com/bmo00/arcfpga-cores) — this repository only carries the
built binaries and the database manifest the MiSTer Downloader reads.

## Credits

- [Jose Tejada (jotego)](https://github.com/jotego) — [JTFRAME](https://github.com/jotego/jtframe)
  and [jtcores](https://github.com/jotego/jtcores), the framework and core collection
  [arcfpga-cores](https://github.com/bmo00/arcfpga-cores) builds on.
