### This project is forked from [[excalidraw]](https://github.com/excalidraw/excalidraw)

<div align="center" style="display:flex;flex-direction:column;">
  <a href="https://excalidraw.com">
    <img width="540" src="./public/og-image-sm.png" alt="Excalidraw logo: Sketch handrawn like diagrams." />
  </a>
  <h4>Virtual whiteboard for sketching hand-drawn like diagrams.<br>Collaborative and end-to-end encrypted.</h4>
</div>

## Documentation

To view the Timeline and Todo for this project see [[MyReadme|MyReadme]]

### Shortcuts

You can almost do anything with shortcuts. Click on the help icon on the bottom right corner to see them all.

### Curved lines and arrows

Choose line or arrow and click click click instead of drag.

### Charts

You can easily create charts by copy pasting data from Excel or just plain comma separated text.

### Translating

To translate Excalidraw into other languages, please visit [our Crowdin page](https://crowdin.com/project/excalidraw). To add a new language, [open an issue](https://github.com/excalidraw/excalidraw/issues/new) so we can get things set up on our end first.

Translations will be available on the app if they exceed a certain threshold of completion (currently 85%).

### Create a collaboration session manually

In order to create a session manually, you just need to generate a link of this form:

```
https://excalidraw.com/#room=[0-9a-f]{20},[a-zA-Z0-9_-]{22}
```

#### Example

```
https://excalidraw.com/#room=91bd46ae3aa84dff9d20,pfLqgEoY1c2ioq8LmGwsFA
```

The first set of digits is the room. This is visible from the server that’s going to dispatch messages to everyone that knows this number.

The second set of digits is the encryption key. The Excalidraw server doesn’t know about it. This is what all the participants use to encrypt/decrypt the messages.

> Note: Please ensure that the encryption key is 22 characters long.

## Shape libraries

Find a growing list of libraries containing assets for your drawings at [libraries.excalidraw.com](https://libraries.excalidraw.com).

## Embedding Excalidraw in your App?

Try out [`@excalidraw/excalidraw`](https://www.npmjs.com/package/@excalidraw/excalidraw). This package allows you to easily embed Excalidraw as a React component into your apps.

## Development

### Code Sandbox

- Go to <https://codesandbox.io/p/github/excalidraw/excalidraw>
  - You may need to sign in with GitHub and reload the page
- You can start coding instantly, and even send PRs from there!

### Local Installation

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

#### Requirements

- [Node.js](https://nodejs.org/en/)
- [Yarn](https://yarnpkg.com/getting-started/install) (v1 or v2.4.2+)
- [Git](https://git-scm.com/downloads)

#### Clone the repo

```bash
git clone https://github.com/excalidraw/excalidraw.git
```

#### Install the dependencies

```bash
yarn
```

#### Start the server

```bash
yarn start
```

Now you can open [http://localhost:3000](http://localhost:3000) and start coding in your favorite code editor.

#### Collaboration

For collaboration, you will need to set up [collab server](https://github.com/excalidraw/excalidraw-room) in local.

#### Commands

##### Install the dependencies

```
yarn
```

##### Run the project

```
yarn start
```

##### Reformat all files with Prettier

```
yarn fix
```

##### Run tests

```
yarn test
```

##### Update test snapshots

```
yarn test:update
```

##### Test for formatting with Prettier

```
yarn test:code
```

#### Docker Compose

You can use docker-compose to work on Excalidraw locally if you don't want to setup a Node.js env.

```sh
docker-compose up --build -d
```

### Self-hosting

We publish a Docker image with the Excalidraw client at [excalidraw/excalidraw](https://hub.docker.com/r/excalidraw/excalidraw). You can use it to self-host your own client under your own domain, on Kubernetes, AWS ECS, etc.

```sh
docker build -t excalidraw/excalidraw .
docker run --rm -dit --name excalidraw -p 5000:80 excalidraw/excalidraw:latest
```

The Docker image is free of analytics and other tracking libraries.

**At the moment, self-hosting your own instance doesn't support sharing or collaboration features.**
