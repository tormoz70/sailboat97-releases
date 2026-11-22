# sailboat97-releases

Публичный репозиторий с APK-сборками игры **sailboat97** (SailBot, `com.ayrat.sailbot`).

Исходный код хранится в отдельном приватном репозитории [tormoz70/sailboat97](https://github.com/tormoz70/sailboat97). Здесь только готовые установочные файлы, чтобы их можно было скачивать без токена доступа.

## Последний релиз

Страница релизов: [Releases](https://github.com/tormoz70/sailboat97-releases/releases)

Последний релиз: [latest](https://github.com/tormoz70/sailboat97-releases/releases/latest)

Публичный API без авторизации:

`https://api.github.com/repos/tormoz70/sailboat97-releases/releases/latest`

## Схема версий

Чтобы номер сборки можно было надёжно прочитать из публичного API, каждый релиз следует одной схеме:

- **Тег:** `v{versionName}`, например `v0.1.8`.
- **Имя APK:** `sailboat97-{versionName}-vc{versionCode}.apk`, например `sailboat97-0.1.8-vc8.apk`.
- **Описание релиза** содержит машиночитаемые строки:

```
versionName: 0.1.8
versionCode: 8
```

Правило разбора (по приоритету):

1. `versionCode` из имени APK-ассета (`-vc` + целое число).
2. Если в имени нет — строка `versionCode: N` из тела релиза.
3. `versionName` — из тега без префикса `v`, либо из той же схемы в имени файла / теле релиза.

Не удаляйте старые релизы и ассеты: новые сборки публикуются рядом.

## Установка вручную

Скачайте APK со страницы [Releases](https://github.com/tormoz70/sailboat97-releases/releases) и установите его на устройство. Android может попросить разрешение на установку из неизвестных источников / из браузера.