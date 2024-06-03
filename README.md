`docker compose` becomes stuck if it has to build image.
Image will be correctly built, however cli becomes stuck on:

```
 => exporting to docker image format                                                                              78.2s
 => => exporting layers                                                                                            0.0s
 => => exporting manifest sha256:1421688e715829c33991e565b18f6ce01a3dc7067a60c59b403ae5287b3fd16e                  0.0s
 => => exporting config sha256:ddd16cb6566e8bb08217a5eaadde76de441741c0a8e5e9579453213252b9f28f                    0.0s
 => => sending tarball                                                                                            75.1s
 ```
 
Repro steps:

```
cd src
docker compose up
```