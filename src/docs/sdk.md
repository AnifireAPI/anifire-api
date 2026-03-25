# Official `@Anifire/api` SDK

The official TypeScript SDK makes it easy to integrate Anifire API into your projects with full type safety.

## 🚀 Installation

```bash
npm install @Anifire/api
```

## 🛠️ Basic Usage

Initialize the client and start making requests.

```typescript
import { AnifireClient } from "@Anifire/api";

const client = new AnifireClient({
  baseUrl: "http://localhost:4000/api/v1" // Optional, defaults to localhost:4000
});

// Fetch trending anime
const home = await client.hianime.getHome();
console.log(home.data.trendingAnimes);

// Search for anime
const results = await client.hianime.search("Naruto");
```

## 📦 SDK Modules

### 1. HiAnime

- `getHome()`: Get spotlight, trending, and latest updates.
- `getInfo(id)`: Detailed metadata for a specific anime.
- `getEpisodes(id)`: Get episodes and their streaming sources.
- `search(query, page)`: Search for anime titles.

### 2. Utility

- `trace(imageUrl)`: Reverse image search via Trace.moe.
- `getRandomQuote(anime)`: Get inspiring quotes.
- `getFacts(anime)`: Fun facts about your favorite series.

## 🛡️ Configuration

| Parameter | Type     | Description                                     |
|-----------|----------|-------------------------------------------------|
| `baseUrl` | `string` | The root URL of your Anifire API instance.      |
| `apiKey`  | `string` | (Optional) Your API key if authentication is.   |
