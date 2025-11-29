# wayfind

[a robot guidance counsellor](https://wayfind.abdl.sh)

Uses Cloudflare Pages/Workers for hosting, Workers AI for vector embeddings, Xata for storing vectors, and Langchain for coordination and state.

### Packages
- [app](https://github.com/futurGH/wayfind/tree/main/app) — frontend<br/>
  Required environment variables (in `.env`):
	- `VITE_API_URL` — the URL of the backend<br/>
  
  To run locally: `pnpm dev` 
- [server](https://github.com/futurGH/wayfind/tree/main/server) — backend; to run on Cloudflare Workers<br/>
  Required environment variables (in `.dev.vars`):
  - `OPENAI_API_KEY` — OpenAI API key for generating responses
  - `XATA_API_KEY` — API key for Xata vector database
  - `XATA_DB_URL` — URL to Xata vector database<br/>
  
  To run locally: `wrangler dev`
- [lib](https://github.com/futurGH/wayfind/tree/main/lib) — shared functions
- [scripts](https://github.com/futurGH/wayfind/tree/main/scripts) — scripts for scraping, formatting, and storing course data; see the [dedicated README](https://github.com/futurGH/wayfind/tree/main/scripts/README.md)!
