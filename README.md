# Locations — Countries, States & Cities Data

> **Fork of [botble/locations](https://github.com/botble/locations)**
>
> This is a personal fork maintained by **Ali Adnan Haider Darwish Al-Zaabi** for use with Botble-based projects. All original credit goes to the [Botble](https://botble.com) team.

---

## 📦 What Is This?

A comprehensive dataset of world countries, states/provinces, and cities in JSON format. Used by [Botble CMS](https://botble.com) and compatible scripts to power location pickers and address forms.

## 📋 Data Structure

Each country has its own directory (ISO 3166-1 alpha-2 code) containing three JSON files:

```
{countryCode}/
├── country.json   # Country metadata (name, iso2, iso3, phone code, etc.)
├── states.json    # List of states / provinces
└── cities.json    # List of cities (with state references)
```

**Example — Oman (`om/`):**
```json
// country.json
{ "id": 172, "name": "Oman", "iso3": "OMN", "iso2": "OM", ... }

// states.json
[{ "id": 3248, "name": "Ad Dakhiliyah", "state_code": "DA" }, ...]

// cities.json
[{ "id": 52693, "name": "Muscat", "state_id": 3252 }, ...]
```

## 🚀 Usage

### In PHP (Botble CMS)

```php
$countries = json_decode(file_get_contents('path/to/locations/xx/country.json'), true);
$states    = json_decode(file_get_contents('path/to/locations/xx/states.json'), true);
$cities    = json_decode(file_get_contents('path/to/locations/xx/cities.json'), true);
```

### In JavaScript

```js
const response = await fetch('/locations/om/cities.json');
const cities = await response.json();
```

## 🗂️ Coverage

Contains data for **240+ countries** following ISO 3166-1 standards.

## 🤝 Original Project

- **Repository:** [github.com/botble/locations](https://github.com/botble/locations)
- **Website:** [botble.com](https://botble.com)
- **Marketplace:** [codecanyon.net/user/botble](https://1.envato.market/r55vj)
- **Contact:** [contact@botble.com](mailto:contact@botble.com)

## 📄 Fork Maintainer

**Ali Adnan Haider Darwish Al-Zaabi** — [github.com/zaabi1995](https://github.com/zaabi1995)

This fork may contain additional location data or corrections not yet in the upstream repo.
