# gtsrb

Traffic sign classification on the [German Traffic Sign Recognition Benchmark (GTSRB)](https://benchmark.ini.rub.de/gtsrb_news.html) with PyTorch and torchvision.

## Setup

This project uses [Pixi](https://pixi.sh) to manage the environment. Install Pixi, then run:

```bash
pixi install
```

This creates a CPU environment with PyTorch, torchvision, and the development tools.

### GPU (Linux, CUDA 12)

On a Linux machine with an NVIDIA GPU and a CUDA 12 driver, run:

```bash
pixi install -e cuda
```

Prefix commands with `-e cuda` to use it, e.g. `pixi run -e cuda test`.

## Development

Set up the git pre-commit hooks (ruff and mypy run on every commit):

```bash
pixi run pre-commit-install
```

| Command                 | Description                              |
| ----------------------- | ---------------------------------------- |
| `pixi run check`        | Run all checks (format, lint, types, tests) |
| `pixi run format`       | Format code with ruff                    |
| `pixi run lint`         | Lint with ruff                           |
| `pixi run lint-fix`     | Lint and auto-fix with ruff              |
| `pixi run typecheck`    | Type check with mypy (strict)            |
| `pixi run test`         | Run tests with coverage                  |

Run `pixi task list` to see all available tasks, or `pixi shell` to open a shell inside the environment.
