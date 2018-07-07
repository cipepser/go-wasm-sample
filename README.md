# go-wasm-sample

[Go 1.11: WebAssembly for the gophers](https://medium.zenika.com/go-1-11-webassembly-for-the-gophers-ae4bb8b1ee03)の写経です。

## コンテナの起動

`nlepage/golang_wasm:examples`コンテナを起動します。

```sh
❯ docker container run -dP nlepage/golang_wasm:examples
Unable to find image 'nlepage/golang_wasm:examples' locally
examples: Pulling from nlepage/golang_wasm
ff3a5c916c92: Already exists
b430473be128: Pull complete
7d4e05a01906: Pull complete
8aeac9a3205f: Pull complete
d29c098e021e: Pull complete
7ab573c03893: Pull complete
ba3e9e92ddfd: Pull complete
3d5cf98ca6fd: Pull complete
ea002c1a8d50: Pull complete
747a17426e87: Pull complete
441f2ef1d3f5: Pull complete
1d9d423a68e3: Pull complete
Digest: sha256:f60e5bde1837489463946275e12dc86eb5360e94b3f1bd14d6cce18a78e26b25
Status: Downloaded newer image for nlepage/golang_wasm:examples
658a1399ec5e8a07582e1c83617a7db2e8afd38193a5fc178a599e0ddf33cb62
```

## ブラウザアクセスの確認

マッピングされているポート番号を確認します。この例だと`32768`です。

```sh
❯ docker container ls | grep golang
658a1399ec5e        nlepage/golang_wasm:examples     "nginx -g 'daemon of…"   15 minutes ago      Up 15 minutes       0.0.0.0:32768->80/tcp   adoring_hypatia
```

`http://localhost:32768`にブラウザでアクセスします。

![01](https://github.com/cipepser/go-wasm-sample/blob/master/img/01.png)