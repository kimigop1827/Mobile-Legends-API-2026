# Mobile Legends User Info Lookup API

A powerful API for retrieving Mobile Legends: Bang Bang (MLBB) player information including rank, nickname, account details, collector stats, skins, login information, squad data, hero history, and more.

Perfect for developers building:

* MLBB websites
* Discord bots
* Gaming dashboards
* Player trackers
* Tournament systems
* MLBB checker tools
* Verification systems
* Community apps

## API Marketplace

[Mobile Legends User Info Lookup API](https://rapidapi.com/bienkim86/api/mobile-legends-user-info-lookup?utm_source=chatgpt.com)

---

# Features

* Fast MLBB account lookup
* Retrieve player profile data
* Current & highest rank
* Last login information
* Account country detection
* Collector level & points
* Skin count
* Squad information
* Hero history
* JSON response format
* RapidAPI integration
* Easy to use

---

# Base URL

```bash id="5de9of"
https://mobile-legends-user-info-lookup.p.rapidapi.com
```

---

# Authentication

All requests require RapidAPI headers.

```http id="6mkr8p"
X-RapidAPI-Key: YOUR_API_KEY
X-RapidAPI-Host: mobile-legends-user-info-lookup.p.rapidapi.com
```

---

# Endpoint

## Lookup MLBB Player

```http id="o9f5n7"
GET /lookup?id=PLAYER_ID&zone=ZONE_ID
```

---

# Parameters

| Parameter | Type   | Required | Description              |
| --------- | ------ | -------- | ------------------------ |
| id        | string | Yes      | Mobile Legends Player ID |
| zone      | string | No       | Mobile Legends Zone ID   |

---

# Example Request

## cURL

```bash id="u1l3b5"
curl --request GET \
  --url 'https://mobile-legends-user-info-lookup.p.rapidapi.com/lookup?id=569296372&zone=10012' \
  --header 'X-RapidAPI-Key: YOUR_API_KEY' \
  --header 'X-RapidAPI-Host: mobile-legends-user-info-lookup.p.rapidapi.com'
```

---

## JavaScript (Fetch)

```javascript id="mh2v0s"
const url = 'https://mobile-legends-user-info-lookup.p.rapidapi.com/lookup?id=569296372&zone=10012';

const options = {
  method: 'GET',
  headers: {
    'X-RapidAPI-Key': 'YOUR_API_KEY',
    'X-RapidAPI-Host': 'mobile-legends-user-info-lookup.p.rapidapi.com'
  }
};

fetch(url, options)
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

---

## Python

```python id="p7x2fe"
import requests

url = "https://mobile-legends-user-info-lookup.p.rapidapi.com/lookup"

querystring = {
    "id": "569296372",
    "zone": "10012"
}

headers = {
    "X-RapidAPI-Key": "YOUR_API_KEY",
    "X-RapidAPI-Host": "mobile-legends-user-info-lookup.p.rapidapi.com"
}

response = requests.get(url, headers=headers, params=querystring)

print(response.json())
```

---

# Example Response

```json id="72ah8n"
{
  "success": true,
  "status": 200,
  "data": {
    "player_data": {
      "achievement_points": 82140,
      "collector_point": 15815,
      "collector_rank": 0,
      "collector_tier": "Seasoned Collector III",
      "create_account_country": "ph",
      "current_rank": "Legend V",
      "hero_count": 0,
      "hero_history": [
        "Dyrroth",
        "Lesley",
        "Natalia",
        "Karina"
      ],
      "high_rank": "Mythic 1",
      "last_login": "2026-05-12 (0d 15h 50m ago) PHT",
      "last_login_country": "ph",
      "level": 80,
      "location": "Philippines, Metropolitan Manila, Taguig, Western Bicutan",
      "matches": 0,
      "nickname": "*Legend__gamer*",
      "player_id": 569296372,
      "server": 10012,
      "skin_breakdown": {},
      "skin_count": 95,
      "squad": "TCO Chøsen Ônes"
    },
    "request": {
      "role_id": 569296372,
      "zone_id": null
    },
    "status": "success"
  },
  "response_time_ms": 5162
}
```

---

# Response Fields

| Field           | Description                 |
| --------------- | --------------------------- |
| nickname        | Player nickname             |
| player_id       | MLBB player ID              |
| current_rank    | Current rank                |
| high_rank       | Highest achieved rank       |
| level           | Account level               |
| skin_count      | Total skins                 |
| squad           | Squad name                  |
| collector_tier  | Collector tier              |
| collector_point | Collector points            |
| hero_history    | Recently used heroes        |
| last_login      | Last login information      |
| location        | Approximate player location |

---

# Error Response

```json id="4m3c9s"
{
  "success": false,
  "status": 404,
  "message": "Player not found"
}
```

---

# Rate Limits

Rate limits depend on your RapidAPI subscription plan.

Check your RapidAPI dashboard for details.

---

# Best Practices

* Cache API responses when possible
* Handle errors properly
* Keep your API key private
* Respect rate limits
* Validate user input before requests

---

# Ideal For

* MLBB APIs
* Mobile Legends tools
* MLBB account checker
* Mobile Legends profile lookup
* Moonton-related integrations
* Gaming APIs
* Mobile Legends tracker systems

---

# Tags

```txt id="6d9xjw"
mlbb api
mobile legends api
mobilelegends api
mobile legends checker
mobilelegends checker
mlbb checker
mlbb account checker
mobile legends account lookup
mobile legends profile api
moonton api
mobile legends login
mlbb profile checker
mobile legends stats api
mlbb player info
mlbb player lookup
mobile legends tracker
gaming api
rapidapi mlbb
mobile legends user info
mobile legends account api
```

---

# Support

If you encounter issues or want to request new features, feel free to open an issue on GitHub.

---

# License

MIT License
