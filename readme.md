# issue

cannot fetch remote context as copy of files fails

```cmd
D:\Dev\HomeSmartMesh\website_light>docker compose build runner
2024/05/05 15:45:55 http2: server: error reading preface from client //./pipe/docker_engine: file has already been closed
[+] Building 2.4s (7/7) FINISHED                                                                                                            docker:default
 => [runner internal] load git source https://github.com/MicroWebStacks/copper.git#main:runner                                                        1.1s
 => [runner internal] load metadata for docker.io/library/python:3.9-slim                                                                             1.1s
 => [runner 1/5] FROM docker.io/library/python:3.9-slim@sha256:44122e46edb1c3ae2a144778db3e01c78b6de3af20ddcc38d43032decffb00cf                       0.0s
 => CACHED [runner 2/5] WORKDIR /app                                                                                                                  0.0s
 => CACHED [runner 3/5] RUN pip install PyYAML==5.3.1 aiomqtt                                                                                         0.0s
 => [runner 4/5] COPY *.py /app/                                                                                                                      0.1s
 => ERROR [runner 5/5] COPY utils/*.py /app/utils/                                                                                                    0.1s
------
 > [runner 5/5] COPY utils/*.py /app/utils/:
------
failed to solve: lstat /var/lib/docker/tmp/buildkit-mount3718892074/utils: no such file or directory
```
