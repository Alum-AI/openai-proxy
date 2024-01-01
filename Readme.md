# OpenAI/ChatGPT Proxy

## Deployment

### Deno

Click [here][1] tod deployment on the Deno Deploy。

then go to Settings, and setupt domains.

or visit https://deno.new, copy deno.ts to Playground， and click `Play`
button.

### CloudFlare

copy cloudflare.ts to CloudFlare Workers.

## Usage

use OpenAI/ChatGPT official npm package：

```diff
import { Configuration } from "openai";

const configuration = new Configuration({
  apiKey: OPENAI_API_KEY,
+ basePath: "https://xxxxx.deno.dev/v1",
});
```

use OpenAI/ChatGPT official Python package：

```diff
  import openai

  openai.api_key = os.getenv("OPENAI_API_KEY")
+ openai.api_base = "https://xxxxx.deno.dev/v1"
```

## Reference

- [ChatGPT From Beginning to Expert](https://github.com/justjavac/chatgpt)

## Local

```bash
deno run --allow-net --allow-read --allow-env --watch deno.ts
```

[1]: https://dash.deno.com/new?url=https://raw.githubusercontent.com/Alum-AI/openai-proxy/main/deno.ts
