# RequestBite API Catalog

## About

The RequestBite API Catalog is a community-built catalog of interesting REST
APIs from around the world. The catalog API allows you to search for, and list,
the OpenAPI spec of those APIs and thus returns data in a standards-based format
that can be used in [Slingshot](https://s.requestbite.com) or any other API
client that supports importing Swagger/OpenAPI specs.

The catalog itself is served through an open and publicly available API. You can
also browse the catalog online via Slingshots's [catalog
browser](https://s.requestbite.com/catalog).

<p align="center">
  <img alt="RequestBite Slingshot" src="https://github.com/user-attachments/assets/222fa175-09b3-4a7f-a302-9b6cd7a82198">
</p>

The OpenAPI spec for the API catalog itself can be found in the
[openapi.yaml](./openapi.yaml) and can be imported into Slingshot by [clicking
this link](https://s.requestbite.com?import=https://raw.githubusercontent.com/requestbite/api-catalog-data/refs/heads/main/openapi.yaml) (you can also find it in the API catalog itself).

## Using the API catalog

While the raw data of the API can be found in this repository, we encourage you
to use the provided API to search for, and list, any APIs of interest.

## Structure of this repo

This repository is roughly structured as the as the catalog API itself:

```
data/
└── providers/
    └── {provider}/
        └── {serviceName}/
            ├── {apiVersion}/
            │   ├── api.json           Mandatory metadata about API
            │   └── logo.webp          Optional logotype in .svg, .webp, .png or .jpg format
            └── region.json            Optional info about whether API is specific to a country
```

An example of an actual API from the catalog is as follows:

```
data/
└── providers/
    └── resrobot.se/
        └── resrobot-apis-v2.1/
            ├── 1.0.0/
            │   ├── api.json
            │   └── logo.webp
            └── region.json
```

## Contribute to the catalog

The easiest way to contribute a new API to the catalog is by using the API
catalog [submission form](https://s.requestbite.com/catalog/edit). It currently
requires you to have access to an publicly available OpenAPI spec online (which
you can link to).

There are two types of OpenAPI specs you can contribute:

* **Vendor-provided spec**  
  If you have a link to an authoritative OpenAPI spec provided by the API
  author, then select "API provider" as _source_ when submitting your spec.
* **Community-built spec**  
  If you have created or generated an OpenAPI spec yourself for an API to which
  there exists no authoritative OpenAPI spec by the API author, then select
  "Community" as _source_ when submitting your spec.

If you want to update or delete an entry (because it no longer exists or because
it contains incorrect details), you can do so by submitting a pull request to
this repository.

### To be documented

How to manually submit (and optionally host) an API spec through this repo.

## Notable mentions

A big thanks to the [APIs.guru](https://apis.guru) project that has been used to
power a large part of the initial version of the catalog.
