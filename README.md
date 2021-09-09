# get-latest-version
Get latest docker image version from "hub.docker.com"  
Exclude prerelease version, like alpha, beta, rc, etc...

## Usage
```yaml
on:
  schedule:
    - cron: '0 0 * * 1'
  workflow_dispatch:

jobs:
  get-latest-version:
    runs-on: ubuntu-latest
    steps:
    - use: kyanagimoto/get-latest-version@main
      with:
        repo-name: 'elastic/filebeat'
```

## How to build
```shell
npm build
```
or
```shell
tsc src/main.ts --outDir lib/
node lib/main.js
```
