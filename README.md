# excalidraw-storage-backend

This is a reimplementation of [excalidraw-json](https://github.com/excalidraw/excalidraw-json) suitable for self hosting you own instance of Excalidraw.

It can be used with [kiliandeca/excalidraw-fork](https://gitlab.com/kiliandeca/excalidraw-fork)

[DockerHub kiliandeca/excalidraw-storage-backend](https://hub.docker.com/r/kiliandeca/excalidraw-storage-backend)

## Environement Variables

| Name            | Description                                                  | Default value    |
| --------------- | ------------------------------------------------------------ | ---------------- |
| `PORT`          | Server listening port                                        | 8080             |
| `GLOBAL_PREFIX` | API global prefix for every routes                           | `/api/v2`        |
| `STORAGE_URI`   | [Keyv](https://github.com/jaredwray/keyv) connection string, example: `redis://user:pass@localhost:6379`. Availabe Keyv storage adapter: redis, mongo, postgres and mysql  | `""` (in memory **non-persistent**) |
| `LOG_LEVEL`     | Log level (`debug`, `verbose`, `log`, `warn`, `error`)       | `warn`           |
| `BODY_LIMIT`    | Payload size limit for scenes or images                      | `50mb`           |
