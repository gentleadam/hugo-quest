# hugo-quest

## Features

## Installation

## Configuration

## Development
For local development run Hugo's built-in local server.

```
hugo server
```

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your browser.

## Localhost inside exampleSite

You can run this site without installing it as a hugo theme using the following command. I use this for theme development.

```
hugo server --source=exampleSite --theme=../..
```

## Github Codespace

```
hugo server --source=exampleSite --theme=../.. --baseURL=https://improved-pancake-7vgq497rpg72rw59-1313.app.github.dev/ --appendPort=false
```