<!-- Please do not edit this file. Edit the `blah` field in the `package.json` instead. If in doubt, open an issue. -->


[![github-stats](http://i.imgur.com/1cEkaOy.png)](#)

# `$ github-stats`

 [![Support me on Patreon][badge_patreon]][patreon] [![Buy me a book][badge_amazon]][amazon] [![PayPal][badge_paypal_donate]][paypal-donations] [![Ask me anything](https://img.shields.io/badge/ask%20me-anything-1abc9c.svg)](https://github.com/IonicaBizau/ama) [![Version](https://img.shields.io/npm/v/github-stats.svg)](https://www.npmjs.com/package/github-stats) [![Downloads](https://img.shields.io/npm/dt/github-stats.svg)](https://www.npmjs.com/package/github-stats) [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/johnnyb?utm_source=github&utm_medium=button&utm_term=johnnyb&utm_campaign=github)

<a href="https://www.buymeacoffee.com/H96WwChMy" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/yellow_img.png" alt="Buy Me A Coffee"></a>

> Visualize stats about GitHub users and projects in your terminal.


This project is under the [`git-stats`](https://github.com/IonicaBizau/git-stats) umbrella. `git-stats` tracks your local commits and the visualization is similar. :sparkle:

[`github-profile-languages`](https://github.com/IonicaBizau/github-profile-languages) provides the same pie chart visualization, but in browser (for users and repositories).


[![github-stats](http://i.imgur.com/JFNQxbv.png)](#)

## :cloud: Installation

You can install the package globally and use it as command line tool:


```sh
# Using npm
npm install --global github-stats

# Using yarn
yarn global add github-stats
```


Then, run `github-stats --help` and see what the CLI tool can do.


```
$ github-stats --help
Usage: github-stats [options]

Options:
  -u, --user <user>        The GitHub user to get stats about.
  -r, --repo <repository>  The full repository name.
  -n, --no-ansi            Disable ansi styles.
  -l, --light              Use the light theme.
  -c, --calendar           Show the calendar.
  --user-stats, --us       Display user stats.
  --repo-stats, --rs       Display repository stats.
  --alt-host, --ah <host>  Alternate Github host.
  -t, --token <token>      GitHub access token to access private resources or
                           to increase the rate limit.
  -h, --help               Displays this help.
  -v, --version            Displays version information.

Examples:
  gh-stats -u IonicaBizau -r gh-stats --us --rs -c # Show everything
  gh-stats -u IonicaBizau # Show the calendar
  gh-stats -r IonicaBizau/git-stats --alt-host https://github.myhost.com/api/v3/ # Repository stats from hosted Github

Documentation can be found at https://github.com/IonicaBizau/gh-stats
```

## :clipboard: Example


Here is an example how to use this package as library. To install it locally, as library, you can do that using `npm` (or `yarn`):

```sh
# Using npm
npm install --save github-stats

# Using yarn
yarn add github-stats
```



```js
// Dependencies
var GitHubStats = require("github-stats");

// Create the GitHubStats instance
var stats = new GitHubStats({

    // Enable light theme for calendar
    theme: "LIGHT"

    // Provide the repository and the username
  , repo: "hubber-memory-game"
  , user: "alysonla"

    // Visualize repository, user and calendar stats
  , s_repo: true
  , s_user: true
  , cal: true

    // A token could help to visualize private stats
  , token: "an optional token"
});

// Stringify everything
stats.toString(function (err, output, warns) {
    console.log(err || output);
});
```



## :question: Get Help

There are few ways to get help:

 1. Please [post questions on Stack Overflow](https://stackoverflow.com/questions/ask). You can open issues with questions, as long you add a link to your Stack Overflow question.
 2. For bug reports and feature requests, open issues. :bug:

 3. For direct and quick help, you can [use Codementor](https://www.codementor.io/johnnyb). :rocket:



## :memo: Documentation

For full API reference, see the [DOCUMENTATION.md][docs] file.

## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :sparkling_heart: Support my projects

I open-source almost everything I can, and I try to reply to everyone needing help using these projects. Obviously,
this takes time. You can integrate and use these projects in your applications *for free*! You can even change the source code and redistribute (even resell it).

However, if you get some profit from this or just want to encourage me to continue creating stuff, there are few ways you can do it:


 - Starring and sharing the projects you like :rocket:
 - [![Buy me a book][badge_amazon]][amazon]—I love books! I will remember you after years if you buy me one. :grin: :book:
 - [![PayPal][badge_paypal]][paypal-donations]—You can make one-time donations via PayPal. I'll probably buy a ~~coffee~~ tea. :tea:
 - [![Support me on Patreon][badge_patreon]][patreon]—Set up a recurring monthly donation and you will get interesting news about what I'm doing (things that I don't share with everyone).
 - **Bitcoin**—You can send me bitcoins at this address (or scanning the code below): `1P9BRsmazNQcuyTxEqveUsnf5CERdq35V6`

    ![](https://i.imgur.com/z6OQI95.png)


Thanks! :heart:



## :scroll: License

[MIT][license] © [Ionică Bizău][website]


[badge_patreon]: https://ionicabizau.github.io/badges/patreon.svg
[badge_amazon]: https://ionicabizau.github.io/badges/amazon.svg
[badge_paypal]: https://ionicabizau.github.io/badges/paypal.svg
[badge_paypal_donate]: https://ionicabizau.github.io/badges/paypal_donate.svg

[patreon]: https://www.patreon.com/ionicabizau
[amazon]: http://amzn.eu/hRo9sIZ
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(https%3A%2F%2Fionicabizau.net)&year=2015#license-mit
[website]: https://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
