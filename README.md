# 📈 githubtrending – GitHub Trending API (JSON)

githubtrending is a simple, fast, and real-time API for fetching data from the GitHub Trending page in JSON format. It supports all official GitHub Trending filters and is perfect for developers who want to integrate trending repository data into their apps, dashboards, or research tools.

# 🚀 Features
- Real-time GitHub Trending data in JSON format
- Supports all GitHub Trending filters (since, spoken_language_code, language)
- Lightweight GET API – easy to use
- Returns repository details, contributors, stars, forks, and more
- 

# 📡 API Usage
- Example request (daily trends)
```bash
curl -s "https://githubtrending.lessx.xyz/trending?since=daily"
```
- Example request (weekly, filtered by language and spoken language)
```bash
curl -s "https://githubtrending.lessx.xyz/trending?since=weekly&language=python&spoken_language_code=en"
```
- Supported query parameters

| Parameter             | Type    | Description                                                   |
|-----------------------|---------|---------------------------------------------------------------|
| `since`               | string  | Time window: `daily`, `weekly`, `monthly`                     |
| `language`            | string  | Programming language (e.g., `javascript`, `go`, `python`)     |
| `spoken_language_code`| string  | Spoken language code (e.g., `en`, `zh`, `ja`)                 |

# 📦 Example JSON Response
```json
[
  {
    "builders": [
      {
        "profile": "https://github.com/sridharavinash",
        "avatar": "https://avatars.githubusercontent.com/u/868958?s=40&v=4"
      },
      {
        "profile": "https://github.com/domdomegg",
        "avatar": "https://avatars.githubusercontent.com/u/4953590?s=40&v=4"
      }
    ],
    "repository": "https://github.com/modelcontextprotocol/registry",
    "name": "modelcontextprotocol/registry",
    "description": "A community driven registry service for Model Context Protocol (MCP) servers.",
    "language": "Go",
    "stars": "3220",
    "forks": "264",
    "increased": "361 stars today"
  }
  ...
]

```
# ⚠️ Usage Guidelines
- The API is real-time – please cache responses instead of making repeated requests to avoid unnecessary load.
- Respect GitHub’s terms of service when using the data.

# ⭐ Support the Project
If you find githubtrending useful:
- Star this repository on GitHub
- Share it with other developers
- Contribute by submitting issues or pull requests

# 📜 License
- MIT License – free to use, modify, and distribute.
