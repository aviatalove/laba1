OS Info Collector — Лабораторная работа 1

Скрипт определяет текущую ОС (Linux / macOS / Windows), собирает
базовые параметры и сохраняет их в `os_report.json`.

Запуск
    python my_script.py

Собираемые параметры
- os: family (Linux/macOS/Windows), release, arch, версия Python
- hardware: количество логических CPU
- environment: hostname, username, home_dir, cwd
- filesystem: свободное место на диске (ГБ)
- locale: кодировка ФС, переменная LANG/LC_ALL
- generated_at: время формирования отчёта

Модули
Использованы только стандартные модули: `os`, `sys`, `json`, `platform`,
`socket`, `getpass`, `shutil`, `datetime`. 

Ограничение
Внешние утилиты ОС (`uname`, `wmic`, `systeminfo` и др.) не вызываются:
всё собирается средствами Python.
