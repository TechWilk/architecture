# Readium Architecture

All Readium implementations (mobile, desktop or Web) are split in two main modules, which use the [Readium Web Publication Manifest](https://readium.org/webpub-manifest/) to communicate together.

On the Web, the [Publication Server](server) is responsible for serving a [Readium Web Publication Manifest](https://readium.org/webpub-manifest/) and the resources of a publication over HTTPS.

In native apps, the [Streamer](streamer) is responsible for parsing packaged publications and exposing them using an in-memory model.

On all platforms, the [Navigator](navigator) is meant to navigate in the resources of a publication and can adopt very different strategy based on the nature of the publication (ebooks, audiobooks and comics).

These modules are not necessarily meant to be deployed on the same device or written in the same language, which lets developers select the best implementation based on their requirements.

![Diagram of the Readium Architecture](images/architecture.svg)

## Components

### Models

* [Readium Web Publication Manifest](https://readium.org/webpub-manifest)
* [Locators](locators)
* [OPDS 2.0](https://drafts.opds.io/opds-2.0)

### Main Modules

* [Publication Server](server)
* [Navigator](navigator)
* [Readium CSS](https://readium.org/readium-css)
* [Streamer](streamer)


### Services

* [Location Resolver](locators/resolver.md)
* [Media Overlay](media-overlay)
* [Positions List](positions)
* [Search](search)

## Projects

[See all active Readium projects](projects.md) based on the Readium Architecture.

## Ecosystem

Take a look at our dedicated [awesome-readium repository](https://github.com/readium/awesome-readium) to explore the ecosystem built around Readium.
