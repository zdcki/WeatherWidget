# Weather Widget

Always-on-top weather widget for Windows, distributed as a standalone `.exe`.
Погодный виджет для Windows поверх всех окон, готовый к запуску через `.exe`.

<img width="337" height="569" alt="image" src="https://github.com/user-attachments/assets/ac891ec9-c957-4d8f-be08-3be3584488a6" />


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
1. Download or copy `WeatherWidget.exe` to a folder of your choice.
2. Double-click `WeatherWidget.exe` to launch it.
3. On first run, enter your city (or coordinates like `55.08, 38.78`). Autostart is enabled automatically and can be switched off in the menu.

No separate AutoHotkey installation is required. Requires Windows 10/11 with PowerShell (built in).

### Usage
Right-click the widget or the tray icon for the menu: refresh, city, view and size, units, notifications, hotkeys, autostart, language.
Drag the widget with the left mouse button.

In click-through mode the widget's own menu is unavailable, so use the tray icon or the `F8` hotkey.

### Customizing the file
The application is distributed as an executable, so the AutoHotkey source settings below can only be changed by editing the source and rebuilding the `.exe`:
- `menuOrder` (top of the source file): reorder or remove menu items
- `windAlert`: wind speed (m/s) that triggers the wind warning
- `notifyLead`: minutes before rain/snow when the notice appears
- `tNote` line: size and position of the rain/snow notice
- In `BuildMenu`, the block between `ТЕСТЫ УВЕДОМЛЕНИЙ` comments adds notification test items; comment it out to hide them

### Data and files
- Settings and cache: `%AppData%\WeatherWidget\` (`settings.txt`, `cache.txt`)
- Forecast sources: [Open-Meteo](https://open-meteo.com/), [MET Norway](https://api.met.no/), [wttr.in](https://wttr.in/)
- City search: Open-Meteo geocoding, falling back to OpenStreetMap Nominatim; a small built-in city list works offline
- Rain/snow timing is approximate: 15-minute steps with Open-Meteo, hourly with MET Norway, 3-hour with wttr.in

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
1. Скачайте или скопируйте `WeatherWidget.exe` в любую удобную папку.
2. Запустите `WeatherWidget.exe` двойным щелчком.
3. При первом запуске введите город (или координаты, например `55.08, 38.78`). Автозапуск включается автоматически; отключить его можно в меню.

Отдельно устанавливать AutoHotkey не нужно. Требуются Windows 10/11 и PowerShell (уже встроен в Windows).

### Использование
Нажмите ПКМ по виджету или его значку в системном трее, чтобы открыть меню: обновление погоды, выбор города, вида и размера, единиц измерения, уведомлений, горячих клавиш, автозапуска и языка.
Виджет перетаскивается левой кнопкой мыши.

В сквозном режиме меню самого виджета недоступно: используйте значок в системном трее или клавишу `F8`.

### Настройка
В готовом `.exe` нельзя напрямую менять параметры исходного скрипта. Чтобы изменить перечисленные настройки, нужно отредактировать исходный код и заново собрать приложение:
- `menuOrder` (в начале исходного файла): порядок и состав пунктов меню
- `windAlert`: скорость ветра (м/с), при которой появляется предупреждение
- `notifyLead`: за сколько минут до дождя или снега появляется уведомление
- строка `tNote`: размер и положение уведомления о дожде/снеге
- В `BuildMenu` блок между комментариями `ТЕСТЫ УВЕДОМЛЕНИЙ` добавляет пункты тестирования уведомлений; закомментируйте его в исходном коде, чтобы скрыть эти пункты

### Данные и файлы
- Настройки и кэш: `%AppData%\WeatherWidget\` (`settings.txt`, `cache.txt`)
- Источники прогноза: [Open-Meteo](https://open-meteo.com/), [MET Norway](https://api.met.no/), [wttr.in](https://wttr.in/)
- Поиск города: геокодер Open-Meteo, запасной вариант OpenStreetMap Nominatim; небольшой встроенный список городов работает без интернета
- Время начала дождя/снега приблизительное: шаг 15 минут у Open-Meteo, час у MET Norway, 3 часа у wttr.in


