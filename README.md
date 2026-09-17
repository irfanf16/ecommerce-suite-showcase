# eCommerce Implementations — Multi-Stack Collection

**Collection · Laravel · React · Node**

The same commerce domain implemented across five stacks — server-rendered, SPA and stateless API architectures.

> **Source code is private.** This repository documents the architecture and engineering work.

## What's in the collection

| Project | Stack | Notable work |
|---|---|---|
| Laravel 8 storefront | Laravel, Blade, MySQL | Multi-locale catalogue, PDF invoicing, Twilio order alerts |
| KwikeMart | Laravel, Stripe, Telescope | Unlimited-depth category tree, Stripe checkout |
| React storefront | React 18, Redux Toolkit | Client-side cart/state, tested with React Testing Library |
| Node commerce API | Express, MongoDB, JWT | Stateless REST API, Mongoose modelling |
| Laravel store | Laravel, Blade | Product listings, cart, order management |

## Engineering highlights

**Arbitrary-depth categories.** KwikeMart uses `kalnoy/nestedset` — a nested-set model — so category trees of any depth resolve in a single query, instead of the recursive lookups an adjacency list forces. The right data structure choice for read-heavy category navigation.

**Tested React state.** The React storefront uses Redux Toolkit for cart and catalogue state, with React Testing Library and jest-dom covering user-facing behaviour rather than implementation detail.

**Stateless Node API.** Express + Mongoose with JWT auth and bcrypt password hashing — a deliberately minimal, horizontally scalable API surface.

**Production observability.** Laravel Telescope wired into KwikeMart for request, query and queue inspection.

**Commerce fundamentals across stacks.** Multi-locale catalogues, PDF invoice generation (dompdf + wkhtmltopdf), image transformation, Excel import/export, and Stripe and Twilio integration — implemented in both server-rendered and SPA architectures.


## Screenshots

<!-- ![Laravel Storefront](docs/laravel-storefront.png) -->
<!-- ![React Storefront](docs/react-storefront.png) -->

_Screenshots pending — see `docs/README.md`._

## Stack

`Laravel 8` · `React 18` · `Redux Toolkit` · `Express` · `MongoDB` · `MySQL` · `Stripe` · `JWT` · `Blade`
