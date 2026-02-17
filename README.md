# Конфигурация баннеров
## Структура

- `banner-config.json` - основной конфигурационный файл
- `banners/` - папка с изображениями баннеров

## Формат конфигурации

```json
{
  "enabled": true,
  "banners": [
    {
      "bannerImageUrl": "https://raw.githubusercontent.com/USERNAME/REPO/main/banners/banner1.png",
      "clickUrl": "https://example.com/promo1",
      "durationSeconds": 60
    },
    {
      "bannerImageUrl": "https://raw.githubusercontent.com/USERNAME/REPO/main/banners/828e543d.png",
      "clickUrl": "https://example.com/promo2",
      "durationSeconds": 60
    },
  ],
    "compactBanners": [
    {
      "bannerImageUrl": "https://..../banner_90px.png",
      "clickUrl": "https://...",
      "durationSeconds": 60
    }
  ],
  "version": "1.0.0"
    "appVersion": "8.0.0",
  "downloadUrl": "https://github.com/USERNAME/REPO/releases/latest"
}
```

### Поля:

- **enabled** (boolean) - включить/выключить показ баннера
  - `true` - баннеры активны, автоматически меняются по таймеру
  - `false` - баннеры отключены

- **banners** (array) - массив объектов баннеров
  - Каждый баннер имеет свое время показа
  - Каждый объект содержит:
    - **bannerImageUrl** (string) - прямая ссылка на изображение баннера
    - **clickUrl** (string) - URL для перехода при клике
    - **durationSeconds** (integer) - сколько секунд показывать этот баннер

- **version** (string) - версия конфигурации
  - Увеличивайте при обновлении для сброса кэша

- **appVersion** (string, опционально) - последняя версия приложения
  - Если указана, приложение проверит свою версию
  - При наличии новой версии покажет уведомление

- **downloadUrl** (string, опционально) - ссылка для скачивания новой версии
  - Используется вместе с `appVersion`
  - Открывается при клике на уведомление об обновлении

- **updateNotificationDurationSeconds** (integer, опционально) - сколько секунд показывать уведомление об обновлении

## Как обновить баннеры через командную строку

```cmd
cd путь/к/репозиторию
```
```cmd
git add 
```
```cmd
git commit -m "Обновил баннеры v1.1.0"
```
```cmd
git push
```