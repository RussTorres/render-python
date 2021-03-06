# render-python

This is a python API client to interact with [render-webservices](https://github.com/saalfeldlab/render) and facilitate python scripting of [tilespec](https://github.com/saalfeldlab/render/blob/master/docs/src/site/markdown/data-model.md) creation

it presently interacts with render via a web-api, though the [client module](renderapi/client.py) aims to interface by calling java client scripts to avoid server-side processing.

Render connection objects created with `renderapi.connect()` can default to environment variables.  Below is an example of the variables which can be sourced and added to, e.g.,  ~/.bashrc or ~/.bash_profile.
```
    export RENDER_HOST="localhost"
    export RENDER_PORT="8080"
    export RENDER_PROJECT="YOURPROJECT"
    export RENDER_OWNER="YOURNAME"
    export RENDER_CLIENT_SCRIPTS=".../render/render-ws-java-client/src/main/scripts"
    export RENDER_CLIENT_SCRIPT="$RENDER_CLIENT_SCRIPTS/run_ws_client.sh"
    export RENDER_CLIENT_HEAP="1G"
```

[Usage examples for a development Array Tomography workflow](https://github.com/fcollman/render-python-apps) are available.
