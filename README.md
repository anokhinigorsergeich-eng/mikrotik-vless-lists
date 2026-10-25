# mikrotik-vless-lists

Списки сервисов для набора MikroTik VLESS Kit: домены и сети, которые роутер направляет через VPN-шлюз.

* `lists/services.json` — единственный файл. Это только данные (JSON, схема 1), никаких команд и скриптов.
  Роутер клиента скачивает его раз в сутки, проверяет формат и при любой ошибке оставляет прежние списки.
* Формат: `{"schema": 1, "updated": "ГГГГ-ММ-ДД", "services": {"имя": {"title", "default", "domains": [], "cidrs": []}}}`.
  Домены — строчные латинские буквы, цифры, точки и дефисы; сети — `a.b.c.d/N`, N от 8 до 32, не частные.
* Адрес для роутеров: `https://raw.githubusercontent.com/anokhinigorsergeich-eng/mikrotik-vless-lists/main/lists/services.json`
