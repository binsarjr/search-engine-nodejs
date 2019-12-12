# search-engine-nodejs
[![npm](https://nodei.co/npm/search-engine-nodejs.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/search-engine-nodejs)

[![npm-version](https://img.shields.io/npm/v/search-engine-nodejs)](https://github.com/binsarjr/search-engine-nodejs)
[![issues](https://img.shields.io/github/issues/binsarjr/search-engine-nodejs)](https://github.com/binsarjr/search-engine-nodejs/issues)
![lisense](https://img.shields.io/npm/l/search-engine-nodejs)
![download-weekly](https://img.shields.io/npm/dw/search-engine-nodejs)
![download-times](https://img.shields.io/npm/dt/search-engine-nodejs)


search-engine-nodejs is made from several search engines namely: Aol, Ask, Baidu, Bing, Google and Yahoo, this search engine is not perfect yet, but if anyone wants to develop it, just continue

# Includes
* fake-useragent
* request
* request-promise-native
* urlencode
* cheerio

# Before Installing
* Install [NodeJs](https://nodejs.org/en/download/)
* using [npm](https://www.npmjs.com)

# Instalation
Installation is done using the `npm install` command:
```properties
$ npm install search-engine-nodejs
```

# Features
search-engine-nodejs supports the following search engines:
* [Aol](https://www.aol.com/)
* [Ask](https://www.ask.com/)
* [Baidu](https://www.baidu.com/)
* [Bing](https://www.bing.com/)
* [Google](https://www.google.com/)
* [Yahoo](https://search.yahoo.com/)
* this module already supports [typescript](https://www.typescriptlang.org/)

# Usage
## javascript
create a file name `index.js` with the following contents
```js
const search_engine = require('search-engine-nodejs').default;

(async () => {
    const options = {
        qs: {
            q: 'Hello Search Engine'
        }
    }

    // you can use: Aol, Ask, Baidu, Bing, Google or Yahoo
    const results = await search_engine.Google(options)
    console.log(results)
})();
```
Start scraping by firing up the command `node index.js`

and more or less like this
```js
[
  {
    url: 'https://support.google.com/websearch/forum/AAAAgtjJeM4tswt4Orqfos/?hl=uk',
    title: 'How to switch to Google as my default search engine in MS EDGE ...',
    description: '15.01.16. Rotary Steve. Hello,. Perhaps this search can be helpful.... https://www. microsoft.com/en-us/search/result.aspx?q=default%20search%20engine.'
  },
  ...
  {
    url: 'http://www.proz.com/forum/sdl_trados_support/255884-an_easy_way_to_copy_paste_source_terms_from_trados_studio_into_a_search_engine_or_dictionary.html?text=An%20easy%20way%20to%20copy-paste%20source%20terms%20from%20Trados%20Studio%20into%20a%20search%20engine%20or%20dictionary%3F%20?text=An%20easy%20way%20to%20copy-paste%20source%20terms%20from%20Trados%20Studio%20into%20a%20search%20engine%20or%20dictionary%3F%20(SDL%20Trados%20support)&print=1',
    title: 'An easy way to copy-paste source terms from Trados Studio into a ...',
    description: '10 Sep 2013 - ... 20Trados%20Studio%20into%20a%20search%20engine%20or%20dictionary %3F%20?text=An ... Hello everyone, .... hi Paul, Sep 10, 2013 ...'
  }
]
```

add the `pageOfResult` option if you want to get results to 2 or more
```js
(async () => {
    const options = {
        pageOfResult: 2,
        qs: {
            q: 'Hello Search Engine'
        }
    }

    // you can use: Aol, Ask, Baidu, Bing, Google or Yahoo
    const results = await search_engine.Google(options)
    console.log(results)
    // This will display the second results page
})();
```
Start scraping by firing up the command `node index.js`

and more or less like this
```js
[
  {
    url: 'https://www.hijden.nl/homepages/digital-agency/',
    title: 'Digital Agency - Hijden - Ontwerp & Branding',
    description: '... 22%2C%22text%22%3A%22Our%20approach%20is%20to%20focus%20on %20growing%20visibility%20in%20organic%20search%20engine%20results.Tidak ada: Hello%'
  },
  ...
  {
    url: 'https://easynewsweb.com/amp/%F0%9F%98%8D-fall-in-love-with-your-search-engine-results-with-25-off-aioseop-pro-%F0%9F%98%8D/',
    title: 'Fall In Love With Your Search Engine Results With 25% Off ...',
    description: "Hey – As Valentine's Day is approaching, we'd like to take this opportunity to ... % 20Fall%20In%20Love%20With%20Your%20Search%20Engine%20Results% ..."
  }
]

```

## Typescript
You just need to change the require to import like this
```js
import SearchEngine from "search-engine-nodejs";
```
and this is the code
```js
import SearchEngine from "search-engine-nodejs";

(async () => {
    const options = {
        qs: {
            q: 'Hello Search Engine'
        }
    }

    // you can use: Aol, Ask, Baidu, Bing, Google or Yahoo
    const results = await SearchEngine.Google(options)
    console.log(results)
})();
```

# Thank You