> # Archival Notice
>
> Hello! 👋 I've been working on **magnetico** since 2017 (less so in the recent years) and seeing so many people interested in it and using it has been a great source of joy and pride for me. However, I have decided that it is for the best to acknowledge and admit openly that I no longer have as much time as I did in high school, nor any willingness to spend the little time I now have by working on **magnetico** or any other [free software](https://en.wikipedia.org/wiki/Free_software) in general, except what I think is [the most important problem in the world](http://www.aaronsw.com/weblog/productivity#:~:text=not%20working%20on-,the%20most%20important%20problem%20in%20the%20world,-\)%20but%20each%20little) that I can work on at that moment.
>
> Fork it, improve it, ship it; keep up the good fight against scarcity. ☀️
>
> Bora <bora at [boramalper.org](https://boramalper.org/)>

# magnetico
*Autonomous (self-hosted) BitTorrent DHT search engine suite.*

[![chat on gitter](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/magnetico-dev/magnetico-dev)&emsp;[![Go](https://github.com/boramalper/magnetico/workflows/Go/badge.svg)](https://github.com/boramalper/magnetico/actions)&emsp;[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/1029/badge)](https://bestpractices.coreinfrastructure.org/projects/1029)

magnetico is the first autonomous (self-hosted) BitTorrent DHT search engine suite that is *designed
for end-users*. The suite consists of two packages:

- **magneticod:** Autonomous BitTorrent DHT crawler and metadata fetcher.
- **magneticow:** Lightweight web interface for magnetico.

Both programs, combined together, allows anyone with a decent Internet connection to access the vast
amount of torrents waiting to be discovered within the BitTorrent DHT space, *without relying on any
central entity*.

**magnetico** liberates BitTorrent from the yoke of centralised trackers & web-sites and makes it
*truly decentralised*. Finally!

## Features
- Easy installation & minimal requirements:
  - [Pre-compiled static binaries](https://github.com/boramalper/magnetico/releases) and [Docker images](https://hub.docker.com/u/boramalper) are provided.
  - Root access is *not* required to install or to use.
- Near-zero configuration:
  - Both programs work out of the box, and **magneticow** can be used without a web-server too.
  - Detailed, step-by-step manual to guide you through the installation.
- No reliance on any centralised entity:
  - **magneticod** trawls the BitTorrent DHT by "going" from one node to another, and fetches the
    metadata using the nodes without using trackers.
- Resilience:
  - Unlike client-server model that web applications use, P2P networks are *chaotic* and
    **magneticod** is designed to handle all the operational errors accordingly.
    - Currently on paper, wait for the v1.0!
- High performance implementation in Go:
  - **magneticod** utilizes every bit of your resources to discover as many infohashes & metadata as
    possible.
- Built-in lightweight web interface:
  - **magneticow** features a lightweight web interface to help you access the database without
    getting on your way.

### Screenshots
*Click on the images to view full-screen.*

<!-- Use https://www.tablesgenerator.com/markdown_tables -->
| ![The Homepage](https://i.imgur.com/RuMctMh.png) | ![Searching for torrents](https://i.imgur.com/ZmLfc12.png) | ![Torrent page](https://i.imgur.com/k4Quwt7.png) |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------------------------:|
|                                                                     __The Homepage__                                                                    |                                                                     __Searching for torrents__                                                                    |                                                     __Viewing the metadata of a torrent__                                                     |

## Why?
BitTorrent, being a distributed P2P file sharing protocol, has long suffered because of the
centralised entities that people depended on for searching torrents (websites) and for discovering
other peers (trackers). Introduction of DHT (distributed hash table) eliminated the need for
trackers, allowing peers to discover each other through other peers and to fetch metadata from the
leechers & seeders in the network. **magnetico** is the finishing move that allows users to search
for torrents in the network, hence removing the need for centralised torrent websites.

## Installation Instructions
> **WARNING:**
>
> **magnetico** is still under active construction, and is considered *alpha* software. Please
> use **magnetico** suite with care and follow the installation instructions carefully to install
> it & secure the installation. Feel perfectly free to send bug reports, suggestions, or whatever
> comes to your mind to send to us through GitHub or personal e-mail.

> **WARNING:**
>
> Do NOT clone the [repository](https://github.com/boramalper/magnetico) to install **magnetico**,
> as it is never meant to be stable (except
> [releases](https://github.com/boramalper/magnetico/releases) of course).

1. Install **magneticod** first by following its [installation instructions](cmd/magneticod/README.md).
2. Install **magneticow** afterwards by following its
   [installation instructions](cmd/magneticow/README.md).

### Docker

Run **magneticod** and **magneticow** with:

``` bash
make docker
```

It will run magnetico from already built image on [Docker Hub](https://hub.docker.com/u/boramalper)!

You should access magneticow at <http://localhost:8080>.

To build fresh images from source, first run:

``` bash
make image
```

Then run `make docker`. It ensures you run updated images of magnetico.

## License

All the code is licensed under AGPLv3, unless stated otherwise specifically. See `COPYING` for
details.

## Donations
### Patreon
https://www.patreon.com/boramalper

### PayPal
https://paypal.me/boramalper

### Cryptocurrencies (Coinbase)
- **BTC:** `3BLWjamWug3QQzcDDGwYLwuCqJyjcfYJB8`
- **LTC:** `MRWX5SGCF7EvN15gpzT5b3KQD3Z91gH8qi`
- **BCH:** `qqn07a58hax9l8pckq9j8ys6dsh2cnu4rsyztw2kj9`
- **ETH:** `0xe5A8e80bAA6129DF7eBB1B5302F9e2Ef4C6f6E62`
- **ETC:** `0x8964EcC86eaf043Bff2CdfE875E73D8095c26a58`

----

Dedicated to Cemile Binay, in whose hands I thrived.

Bora M. ALPER <bora@boramalper.org>
