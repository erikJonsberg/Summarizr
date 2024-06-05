# Summarizr

## Overview

This is an app that takes the URL of a blog post or article and sends back a summary of it. The user can specify the length and language of the summary and save summaries to local storage.

This project was built with [Vite](https://vitejs.dev/) and uses [Redux Toolkit](https://redux-toolkit.js.org/) for state management. The API, [Article Extractor and Summarizer](https://rapidapi.com/restyler/api/article-extractor-and-summarizer), comes from [RapidAPI](https://rapidapi.com/hub).

## Install

Clone this repository

```bash
git clone git@github.com:erikJonsberg/summarizr.git]
```

Install dependencies

```bash
npm install
```

Start the development server

```bash
npm run dev
```

## Set up the project

- Go to the [API at RapidAPI](https://rapidapi.com/restyler/api/article-extractor-and-summarizer/playground/apiendpoint_99e4b95c-3adc-4532-8b4e-20795c3c996a) and click on the `subscribe` button. You'll be asked to sign up. Choose the **free** tier.
- Copy the `X-RapidAPI-Key`
- Create a `.env` file and paste in the key exactly as below.

```javascript
VITE_RAPID_API_ARTICLE_KEY = '<YOUR_KEY_GOES_HERE>';
```

## Resources

[Vite documentation](https://vitejs.dev/guide/)
[Redux Toolkit documentation](https://redux-toolkit.js.org/introduction/getting-started)
[RapidAPI documentation](https://docs.rapidapi.com/)

## Update

The API in this project is unstable, and I would not recommend using it. For some reason, it returns a 429 error -`too many requests`. The limit, set by the author, is 50 requests per day on the free tier. So, he either changed it, or there's a bug somewhere. Also, he hasn't updated it in a year and he has [another project](https://scrapeninja.net/) that seems to be his priority.

Given the release of GPT-4o, I think OpenAI has come far enough that an API like this is unnecessary. This might be a good use case for [CrewAI](https://crewai.com/) as well.
