# litestream-sidecar-example

Example container application configuring persistent storage that restores and replicates with [litestream](https://litestream.io/).

## Usage

Configure litestream.yaml to match your S3 storage.

```
$ docker compose up
```

At the first, this restore-container restore bbs.sqlite from your S3 storage. And application update bbs.sqlite, and it is backed-up as replication.

So you can completely delete containers from the host.

```
$ docker compose rm -v -f
```

## License

MIT

## Author

Yasuhiro Matsumoto (a.k.a. mattn)
