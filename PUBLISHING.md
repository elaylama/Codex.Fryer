# Публикация CODEXFRYER на GitHub

## 1. Локальная проверка перед публикацией

```bash
cd "/Users/elaylama/Documents/Codex SKILLs/CODEXFRYER"
ls -la
```

Убедитесь, что есть:

- `README.md`
- `SKILL.md`
- `examples/dialogue-example.md`
- `LICENSE`
- `.gitignore`

## 2. Инициализация git (если ещё не сделано)

```bash
git init
git branch -M main
git add .
git commit -m "Initial public release: CODEXFRYER Codex skill"
```

## 3. Создание публичного репозитория

### Через GitHub UI

1. Создайте репозиторий `CODEXFRYER`.
2. Выберите `Public`.
3. Не добавляйте auto-generated README/License/.gitignore, чтобы избежать merge-конфликтов.

### Через GitHub CLI

```bash
gh repo create CODEXFRYER --public --source=. --remote=origin --push
```

## 4. Если репозиторий уже создан в UI

```bash
git remote add origin git@github.com:<ваш-github-логин>/CODEXFRYER.git
git push -u origin main
```

## 5. Проверка после публикации

- Откройте репозиторий и проверьте рендер `README.md`.
- Убедитесь, что `SKILL.md` доступен по прямой ссылке.
- Проверьте, что инструкцию установки можно выполнить на чистом окружении.

## 6. Рекомендованный следующий шаг

Добавьте `release` с тегом `v1.0.0` и кратким changelog:

- что делает CODEXFRYER
- чем отличается от vanilla `grill-me`
- как установить в Codex
