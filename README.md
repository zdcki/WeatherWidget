# Weather Widget

Always-on-top weather widget for Windows, written in AutoHotkey v2.
Погодный виджет для Windows поверх всех окон, написан на AutoHotkey v2.

> Add a screenshot here / Добавьте сюда скриншот: `![screenshot](screenshot.png)`

[English](#english) · [Русский](#русский)

---

## English

### Features
- Always on top, borderless, draggable, rounded corners, semi-transparent
- Current weather, next 6 hours, and a 5-day forecast (extended view)
- Three views (compact / normal / extended) and four sizes
- Units: °C / °F, m/s / km/h / mph, mmHg / hPa / inHg
- Heads-up in the widget when rain or snow is expected within 30 minutes
- Warnings for thunderstorms and strong wind next to the city name
- Works without a VPN: Open-Meteo, falling back to MET Norway, then wttr.in
- Last data is cached and shown if the network is down
- Global hotkeys: show/hide (default `F7`) and click-through mode (default `F8`), both configurable
- Click-through mode: the widget stays on screen, clicks go to the windows under it
- Autostart with Windows, Russian and English UI (follows Windows language)

### Install
1. Install [AutoHotkey v2](https://www.autohotkey.com/).
2. Download `weather.ahk` and double-click it.
3. On first run enter your city (or coordinates like `55.08, 38.78`). Autostart is enabled automatically and can be switched off in the menu.

Requires Windows 10/11 with PowerShell (built in). No other dependencies.

### Usage
Right-click the widget or the tray icon for the menu: refresh, city, view and size, units, notifications, hotkeys, autostart, language.
Drag the widget with the left mouse button.

In click-through mode the widget's own menu is unavailable, so use the tray icon or the `F8` hotkey.

### Customizing the file
- `menuOrder` (top of the file): reorder or remove menu items
- `windAlert`: wind speed (m/s) that triggers the wind warning
- `notifyLead`: minutes before rain/snow when the notice appears
- `tNote` line: size and position of the rain/snow notice
- In `BuildMenu`, the block between `ТЕСТЫ УВЕДОМЛЕНИЙ` comments adds notification test items; comment it out to hide them

### Data and files
- Settings and cache: `%AppData%\WeatherWidget\` (`settings.txt`, `cache.txt`)
- Forecast sources: [Open-Meteo](https://open-meteo.com/), [MET Norway](https://api.met.no/), [wttr.in](https://wttr.in/)
- City search: Open-Meteo geocoding, falling back to OpenStreetMap Nominatim; a small built-in city list works offline
- Rain/snow timing is approximate: 15-minute steps with Open-Meteo, hourly with MET Norway, 3-hour with wttr.in

### License
Add a license of your choice (for example MIT).

---

## Русский

### Возможности
- Поверх всех окон, без рамки, перетаскивается, скруглённые углы, полупрозрачный
- Погода сейчас, ближайшие 6 часов и прогноз на 5 дней (расширенный вид)
- Три вида (компактный / обычный / расширенный) и четыре размера
- Единицы: °C / °F, м/с / км/ч / mph, мм рт. ст. / гПа / inHg
- Уведомление в окне, если дождь или снег ожидаются в ближайшие 30 минут
- Предупреждения о грозе и сильном ветре рядом с названием города
- Работает без VPN: Open-Meteo, при недоступности MET Norway, затем wttr.in
- Последние данные кэшируются и показываются, если нет сети
- Глобальные горячие клавиши: показать/скрыть (по умолчанию `F7`) и сквозной режим (по умолчанию `F8`), настраиваются
- Сквозной режим: виджет остаётся на экране, а клики проходят к окнам под ним
- Автозапуск с Windows, интерфейс на русском и английском (по языку Windows)

### Установка
1. Установите [AutoHotkey v2](https://www.autohotkey.com/).
2. Скачайте `weather.ahk` и запустите двойным кликом.
3. При первом запуске введите город (или координаты, например `55.08, 38.78`). Автозапуск включается сам, отключить можно в меню.

Нужны Windows 10/11 и PowerShell (встроен). Других зависимостей нет.

### Использование
ПКМ по виджету или иконке в трее открывает меню: обновить, город, вид и размер, единицы, уведомления, горячие клавиши, автозапуск, язык.
Виджет перетаскивается левой кнопкой мыши.

В сквозном режиме меню виджета недоступно: пользуйтесь иконкой в трее или клавишей `F8`.

### Настройка через файл
- `menuOrder` (начало файла): порядок и состав пунктов меню
- `windAlert`: скорость ветра (м/с) для предупреждения
- `notifyLead`: за сколько минут до дождя/снега появляется уведомление
- строка `tNote`: размер и положение уведомления
- В `BuildMenu` блок между комментариями `ТЕСТЫ УВЕДОМЛЕНИЙ` добавляет пункты тестов; закомментируйте его, чтобы скрыть

### Данные и файлы
- Настройки и кэш: `%AppData%\WeatherWidget\` (`settings.txt`, `cache.txt`)
- Источники прогноза: [Open-Meteo](https://open-meteo.com/), [MET Norway](https://api.met.no/), [wttr.in](https://wttr.in/)
- Поиск города: геокодер Open-Meteo, запасной OpenStreetMap Nominatim; небольшой встроенный список городов работает офлайн
- Время начала дождя/снега приблизительное: шаг 15 минут у Open-Meteo, час у MET Norway, 3 часа у wttr.in

### Лицензия
Добавьте лицензию на ваш выбор (например, MIT).
