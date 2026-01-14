# Rocket Factory Contracts

Хранилище protobuf контрактов для сервисов Rocket Factory. Репозиторий предназначен для:
- хранения исходных `.proto`;
- генерации артефактов для разных языков;
- публикации артефактов в приватные/публичные реестры (начинаем с Python через GitHub Packages).

## Структура
- `proto/` — исходные контракты.
- `Taskfile.yml` — задачи lint/generate/build.
- `python/` — пакетная обвязка и сборка Python-артефактов (stubs).
- `.github/workflows/` — CI для генерации и публикации.

## Быстрый старт (локально)
```bash
python -m pip install --upgrade pip
python -m pip install build setuptools-scm
task proto:gen:
python -m build python
```

## Публикация
GitHub Actions собирает и публикует Python-пакет при пуше тега (`v*` или `python-v*`). Для публикации нужен `GITHUB_TOKEN` (предоставляется GitHub Actions) с правами `packages:write`. См. `.github/workflows/python-publish.yml`.
