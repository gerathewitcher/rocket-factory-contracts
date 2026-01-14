# rocket-factory-contracts (Python)

Python-пакет со сгенерированными protobuf/gRPC stubs.

## Генерация и сборка
```bash
python -m pip install --upgrade pip
python -m pip install build setuptools-scm
task gen-python
python -m build
```

## Установка из GitHub Packages
```bash
pip install --extra-index-url https://pypi.pkg.github.com/<owner> rocket-factory-contracts
```
`<owner>` — организация/пользователь GitHub, владелец репозитория.

## Версионирование
Версия вычисляется `setuptools_scm` по git-тегам (например, `v1.2.3`). Без тега используется `0.0.0`.
