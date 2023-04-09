A demo repo based on [OpenAI GPT-3.5 And GPT 4 Turbo API.](https://platform.openai.com/docs/guides/chat)

**🍿 Live preview**: https://satriaopenai.vercel.app/

> ⚠️ Notice: Our API Key limit has been exhausted. So the demo site is not available now.


## Running Locally

### Pre environment
1. **Node**: Check that both your development environment and deployment environment are using `Node v18` or later. You can use [nvm](https://github.com/nvm-sh/nvm) to manage multiple `node` versions locally。
   ```bash
    node -v
   ```
2. **PNPM**: We recommend using [pnpm](https://pnpm.io/) to manage dependencies. If you have never installed pnpm, you can install it with the following command:
   ```bash
    npm i -g pnpm
   ```
3. **OPENAI_API_KEY**: Before running this application, you need to obtain the API key from OpenAI. You can register the API key at [https://beta.openai.com/signup](https://beta.openai.com/signup).

### Getting Started

1. Install dependencies
   ```bash
    pnpm install
   ```
2. Copy the `.env.example` file, then rename it to `.env`, and add your [OpenAI API key](https://platform.openai.com/account/api-keys) to the `.env` file.
   ```bash
    OPENAI_API_KEY=sk-xxx...
   ```
3. Run the application, the local project runs on `http://localhost:3000/`
   ```bash
    pnpm run dev
   ```

## Deploy

### Deploy With Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/tahaluindo/kawainimeaibang&env=OPENAI_API_KEY&envDescription=OpenAI%20API%20Key&eLink=https%3A%2F%2Fplatform.openai.com%2Faccount%2Fapi-keys)



> #### 🔒 Need website password?
> 
> Deploy with the [`SITE_PASSWORD`](#environment-variables)
> 
> <a href="https://vercel.com/new/clone?repository-url=https://github.com/tahaluindo/kawainimeaibang&env=OPENAI_API_KEY&env=SITE_PASSWORD&envDescription=OpenAI%20API%20Key&envLink=https%3A%2F%2Fplatform.openai.com%2Faccount%2Fapi-keys" alt="Deploy with Vercel" target="_blank"><img src="https://vercel.com/button" alt="Deploy with Vercel" height=24 style="vertical-align: middle; margin-right: 4px;"></a>

![image](https://cdn.staticaly.com/gh/yzh990918/static@master/20230310/image.4wzfb79qt7k0.webp)


### Deploy With Netlify

[![Deploy with Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/tahaluindo/kawainimeaibang#OPENAI_API_KEY=&HTTPS_PROXY=&OPENAI_API_BASE_URL=&HEAD_SCRIPTS=&SECRET_KEY=&OPENAI_API_MODEL=&SITE_PASSWORD=)

**Step-by-step deployment tutorial:**

1. [Fork]( new Site, select the project you `forked` done, and connect it with your `GitHub` account.


2. Select the branch you want to deploy, then configure environment variables in the project settings.

![image](https://cdn.staticaly.com/gh/yzh990918/static@master/20230311/image.gfs9lx8c854.webp)

3. Select the default build command and output directory, Click the `Deploy Site` button to start deploying the site。

![image](https://cdn.staticaly.com/gh/yzh990918/static@master/20230311/image.4jky9e1wbojk.webp)


### Deploy with Docker
Before deploying the app, please make sure `.env` is configured normally.

```bash
# build
docker-compose build .
# run
docker-compose up -d
# stop
docker-compose down
```

### Deploy on more servers

Please refer to the official deployment documentation：https://docs.astro.build/en/guides/deploy

## Environment Variables

You can control the website through environment variables.

| Name | Description | Default |
| --- | --- | --- |
| `OPENAI_API_KEY` | Your API Key for OpenAI. | `null` |
| `HTTPS_PROXY` | Provide proxy for OpenAI API. e.g. `http://127.0.0.1:7890` | `null` |
| `OPENAI_API_BASE_URL` | Custom base url for OpenAI API. | `https://api.openai.com` |
| `HEAD_SCRIPTS` | Inject analytics or other scripts before `</head>` of the page | `null` |
| `SECRET_KEY` | Secret string for the project. Use for generating signatures for API calls | `null` |
| `SITE_PASSWORD` | Set password for site. If not set, site will be public | `null` |
| `OPENAI_API_MODEL` | ID of the model to use. [List models](https://platform.openai.com/docs/api-reference/models/list) | `gpt-3.5-turbo` |


## Frequently Asked Questions

Q: TypeError: fetch failed (can't connect to OpenAI Api)

A: Configure environment variables `HTTPS_PROXY`，reference: 

Q: throw new TypeError(${context} is not a ReadableStream.)

A: The Node version needs to be `v18` or later，reference: 

Q: Accelerate domestic access without the need for proxy deployment tutorial?

A: You can refer to this tutorial: 

Q: `PWA` is not working?

A: Current `PWA` does not support deployment on Netlify, you can choose vercel or node deployment.
## Contributing

This project exists thanks to all those who contributed.

Thank you to all our supporters!🙏



## License

MIT © [satriabot99](https://github.com/satriabot99/LICENSE)
