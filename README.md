Keri-feedback — локальный статический сайт "Кері байланыс"

Как запустить

- Откройте файл `index.html` в папке `keri-feedback` в браузере (двойной клик). Функционал использует localStorage и работает без сервера.
- Если хотите запустить через простой сервер (рекомендуется для корректного origin при генерации ссылок), запустите из PowerShell в этой папке:

  python -m http.server 8000

и откройте http://localhost:8000/

Что реализовано

- Интерфейс учителя/ученика из присланного HTML.
- Локальное хранилище через `_sdk/data_sdk.js` (localStorage).
- Простая конфигурационная stub в `_sdk/element_sdk.js`.
- QR-код генерируется библиотекой qrcodejs (CDN).

Примечания

- Данные хранятся в localStorage под ключом `keri_feedback_data_v1`.
- Для очистки данных откройте devtools -> Application -> Local Storage или вызовите из консоли: `window.dataSdk._clearForTesting()`.
