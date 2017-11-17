## NSTREAM

live streaming with: <br>
[NGINX](https://nginx.org/)  <br>
[RTMP](https://github.com/tiangolo/nginx-rtmp-docker)

    docker run --detach --restart always \
        --name streaming-server \
        --hostname streaming-server \
        --publish 1935:1935 \
        --publish 8080:8080 \
        --publish 8443:8443 \
        puppycodes/nstream

    ```bash
    cd ./documents/examples
    docker-compose up -d
    ```

[Open Broadcaster Software](https://obsproject.com/)

    * Add media source, e.g. `Video Capture Device`
    * Configure streaming server (`Settings` > `Stream`)
        - Stream type: `Custom Streaming Server`
        - URL: `rtmp://localhost/live`
        - Stream key: `test`
    * Press `Start Streaming` button

`http://localhost:9999`
