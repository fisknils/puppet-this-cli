# Puppet This
Puppet This is a very simple command-line tool designed to automate extracting stuff from webpages, where everyone's favorite (curl + sed) might be a bit cumbersome.

That's where puppeteer comes in handy.

While there's many good (better) libraries for scraping data with puppeteer already, this tool is designed to let you quickly hack together small scripts without having to set up a full project to do so.

Maybe you're just obsessive about writing scripts in the command line, or maybe you want a quick way of finding out when a product is back in stock on your favorite webshop. 
How should I know? I've never even met you.

## Options
```javascript
('puppet-this')
    .description('Evaluate a .js script on a webpage using Puppeteer')
    .option('-sp, --scriptedPage <path to script>', 'This custom script will be evaluated outside of the browser sandbox, given a handle of the Page object.')
    .option('-s, --scripts <path to scripts>', 'Comma separated list of .js script files to evaluate')
    .option('-o, --screenshot <screenshotPath>', 'Grab a screenshot of the page')
    .option('-i, --interactive', 'Open an interactive non-headless Puppeteer window')
    .option('-c, --cleanup', 'Delete the user data directory after the script finishes')
    .option('-q, --quiet', 'Suppress spinner output')
    .arguments('<url>', 'URL to target (required)')
```

```bash
puppet-this https://github.com/fisknils/puppet-this-cli \
    -s ./example-scripts/get-github-stars.js
```

### Evaluating multiple scripts
```bash
puppet-this https://github.com/fisknils/puppet-this-cli \
    -s ./example-scripts/get-github-stars.js,./example-scripts/last-modified.js
```

### Grabbing a screenshot
```bash
puppet-this https://github.com/fisknils/puppet-this-cli \
    -o ./screenshot.png
```

### Open a browser window for manual inspection (or clicking away those nasty cookie popups for consequent runs)
```bash
    puppet-this https://github.com/fisknils/puppet-this-cli -i
```

## Installation
```npm -g i puppet-this```

## License
do whatever you want with it!

## Links
- [GitHub Repository](https://github.com/fisknils/puppet-this-cli)
- [NPM Package](https://npmjs.com/package/puppet-this)

## Footnote
In all honesty, I can't imagine this will be of much use to anyone.
I'm just trying to fall in love with coding again.
