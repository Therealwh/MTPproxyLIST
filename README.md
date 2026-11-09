<div align="center">

# 🔥 MTPproxyLIST

### Автообновляемый список живых MTProto прокси для Telegram

**Проверка каждые 15 минут — реальным MTProto-подключением, а не просто пингом**

![Collector](https://img.shields.io/github/actions/workflow/status/Therealwh/MTPproxyLIST/collector.yml?branch=main&style=flat-square&label=collector&logo=github)
![Last Commit](https://img.shields.io/github/last-commit/Therealwh/MTPproxyLIST?style=flat-square&label=updated)
![Stars](https://img.shields.io/github/stars/Therealwh/MTPproxyLIST?style=flat-square&color=2AABEE)
![License](https://img.shields.io/github/license/Therealwh/MTPproxyLIST?style=flat-square)
![Servers](https://img.shields.io/badge/servers-200%2B_verified-3fb950?style=flat-square)
![Interval](https://img.shields.io/badge/check-every_15_min-FFC53D?style=flat-square)

**🆓 Бот с готовым прокси**
[![Free Bot](https://img.shields.io/badge/GET_FREE_PROXY-%40webproxy_tgrobot-2AABEE?style=for-the-badge&logo=telegram)](https://t.me/webproxy_tgrobot)

**💎 Премиум 24/7** — [![Premium](https://img.shields.io/badge/PREMIUM_24/7-%40webproxy_panel_bot-FFC53D?style=for-the-badge&logo=telegram)](https://t.me/webproxy_panel_bot)
**📢 Канал** — [![Channel](https://img.shields.io/badge/Telegram-%40wtfpoxy-24A0ED?style=for-the-badge&logo=telegram)](https://t.me/wtfpoxy)
**⚡ Web-версия** — [![Web](https://img.shields.io/badge/WEB_MTPROTO-Web--MTProto--Proxy-7C5CFF?style=for-the-badge&logo=github)](https://github.com/Therealwh/Web-MTProto-Proxy)

</div>

---

## 🇷🇺 Как это работает

Каждые **15 минут** GitHub Actions запускает коллектор, который:

1. **Собирает** кандидатов из открытых публичных списков MTProto-прокси
2. **Проверяет по-настоящему**: через Telethon устанавливает реальное MTProto-соединение (150 параллельных воркеров, таймаут 3 сек) — фейковые и мёртвые серверы отсеиваются
3. **Пишет** только живые серверы в папку `verified/` и коммитит при значимых изменениях

Режим TCP-ping включается автоматически, если Telethon недоступен (без API-ключей).

## 📋 Файлы со списками

| Файл | Формат | Что внутри |
|---|---|---|
| [proxy_all_verified.txt](verified/proxy_all_verified.txt) | `tg://proxy` | Все проверенные серверы (200+) |
| [proxy_eu_verified.txt](verified/proxy_eu_verified.txt) | `tg://proxy` | Только Европа |
| [proxy_ru_verified.txt](verified/proxy_ru_verified.txt) | `tg://proxy` | Только Россия |
| [proxy_all_tme_verified.txt](verified/proxy_all_tme_verified.txt) | `https://t.me/proxy` | Кликабельные ссылки |
| [proxy_all_verified.json](verified/proxy_all_verified.json) | JSON | Серверы + метаданные |
| [proxy_stats_verified.json](verified/proxy_stats_verified.json) | JSON | Статистика прогона |

## 🚀 Как использовать

**Просто нужен рабочий прокси:** откройте бота [@webproxy_tgrobot](https://t.me/webproxy_tgrobot) — он выдаёт проверенный сервер одной кнопкой. Нужна гарантированная стабильность 24/7 — [@webproxy_panel_bot](https://t.me/webproxy_panel_bot).

**Нужен именно список:** откройте нужный файл → кнопка **Raw** → скопируйте ссылки в Telegram или в своё приложение.

**Свой прокси-сервис:** этот список — готовый источник для вашего парсера (стандартный формат `tg://proxy?server=&port=&secret=`).

## 🛠 Запуск у себя

```bash
git clone https://github.com/Therealwh/MTPproxyLIST.git
cd MTPproxyLIST
pip install -r requirements.txt
python main.py --top 200 --workers 150 --timeout 3.0 --output-dir verified
```

Для полной проверки через Telethon задайте переменные окружения `TG_API_ID` и `TG_API_HASH` (получить: my.telegram.org) — без них включится режим TCP-ping.

---

<div align="center">

&nbsp;

# 🚀 Хочешь свой собственный прокси?

**Забудь о чужих списках — подними свой личный MTProto-сервер за 5 минут!**

&nbsp;

<table>
<tr>
<td width="50%" align="center" valign="top">

### 🌐 WEB MTProto Proxy

*Максимум скорости и скрытности*

✅ **FakeTLS** — маскировка под обычный HTTPS<br>
🛡 **Обход DPI** — работает даже при жёстких блокировках<br>
⚡ **Порт 443** — неотличим от обычного веб-трафика<br>
🖥 **Web-панель** — управление прямо из браузера<br>

[![Deploy](https://img.shields.io/badge/🚀_ОТКРЫТЬ_WEB_MTPROTO-Web--MTProto--Proxy-2AABEE?style=for-the-badge&logo=github)](https://github.com/Therealwh/Web-MTProto-Proxy)

</td>
<td width="50%" align="center" valign="top">

### 🤖 MTProto + Telegram Панель

*Максимум удобства и контроля*

👥 **Мульти-пользователь** — лимиты, квоты, QR-коды<br>
📊 **Статистика** — графики и мониторинг в реальном времени<br>
🤖 **TG-бот** — управление сервером из мессенджера<br>
🔄 **Авто-лечение** — перезапуск и ротация доменов<br>

[![Panel](https://img.shields.io/badge/%F0%9F%9A%80%20%D0%9E%D0%A2%D0%9A%D0%A0%D0%AB%D0%A2%D0%AC%20%D0%9F%D0%90%D0%9D%D0%95%D0%9B%D0%AC-TG%20BOT%20%26%20PANEL-FFC53D?style=for-the-badge&logo=github)](https://github.com/Therealwh/Web-Proxy-Telegram-Panel-TG-BOT)

</td>
</tr>
</table>

&nbsp;

### 💎 Один клик — и у тебя свой прокси, который никто не отберёт

[![Get Started](https://img.shields.io/badge/⭐_Собери_свой_прокси_сегодня-Web--Proxy--Telegram--Panel--TG--BOT-7C5CFF?style=for-the-badge&logo=telegram)](https://github.com/Therealwh/Web-Proxy-Telegram-Panel-TG-BOT)

&nbsp;

</div>

---

## 🇬🇧 English

**Auto-updated list of live MTProto proxies for Telegram.** A collector runs every 15 minutes via GitHub Actions: gathers candidates from public sources, verifies each with a real MTProto connection through Telethon (150 workers, 3s timeout), and commits only working servers to `verified/`.

- Free proxy bot: [@webproxy_tgrobot](https://t.me/webproxy_tgrobot) · Premium: [@webproxy_panel_bot](https://t.me/webproxy_panel_bot)
- Web MTProto version: [Web-MTProto-Proxy](https://github.com/Therealwh/Web-MTProto-Proxy)

> 🚀 **Want your own proxy?** Deploy your personal MTProto server in 5 minutes — with a web panel and Telegram bot:
> 👉 **[Web-Proxy-Telegram-Panel-TG-BOT](https://github.com/Therealwh/Web-Proxy-Telegram-Panel-TG-BOT)**

## ⚖️ Disclaimer

This repository aggregates and verifies publicly available proxy servers. Chats remain end-to-end encrypted by Telegram. Use in accordance with your local laws.
