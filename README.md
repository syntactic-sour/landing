# Landing

## Local development with Docker

Create local environment variables (`.env.local`) based on `.env.local.sample`.

```
docker compose build
docker compose up
```


### Updating dependencies

After updating or installing new dependencies, copy `yarn.lock` from container to the host.

```
docker cp landing-web-1:/app/yarn.lock ./yarn.lock
```


### Remote containers in VS Code

Install [extension for Vs Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) to work with Docker while fully isolating `node_modules` inside Docker container.


### Running Unit-tests

```
docker exec landing-web-1 yarn test:unit --browser.headless
```

### Git hooks

If husky doesn't trigger precoomit, prepush and other hooks, run 

```
git config core.hooksPath .husky/_
```