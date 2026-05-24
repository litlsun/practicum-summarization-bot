# practicum-summarization-bot

Telegram-бот для автоматической транскрибации, суммаризации аудиолекций и генерации учебных заданий.

**Учебный проект, реализуемый совместно с Яндекс.Практикум**

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![Telegram](https://img.shields.io/badge/Telegram-Bot-blue.svg)](https://core.telegram.org/bots/api)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-development-yellow)]()

---

## О проекте

Бот помогает конвертировать синхронные лекции (аудио) в асинхронный формат:
- Распознаёт речь и превращает аудио в текст (Whisper)
- Составляет краткое саммари с ключевыми выводами (Yandex Cloud LLM)
- Генерирует учебные задания для проверки усвоения материала
- Поддерживает лекции до 2 часов

**Цель:** Автоматизация обработки учебных материалов для студентов и преподавателей.

---

## Структура проекта

| Файл | Назначение |
|------|-----------|
| `bot.py` | Главный файл бота |
| `asr.py` | Транскрибация (Whisper) |
| `summarizer.py` | Суммаризация (Yandex Cloud) |
| `questions.py` | Генерация заданий |
| `database.py` | Работа с БД |
| `config.py` | Переменные окружения |
| `utils.py` | Вспомогательные функции |
| `requirements.txt` | Зависимости Python |
| `.env.example` | Пример .env |
| `.gitignore` | Исключения Git |
| `README.md` | Общая информация |
| `docs/` | Папка с документацией |

**Содержимое `docs/`:**
- `user-guide.md` — руководство пользователя
- `architecture.md` — архитектура
- `development-guide.md` — гайд разработчика
- `deployment.md` — развёртывание
- `api-reference.md` — API функций
    
## Пайплайн

- Загрузка аудио (MP3, WAV, M4A, OGG) и видео (MP4 — конвертация в аудио)
- Транскрибация через Whisper
- Суммаризация через Yandex Cloud API
- Генерация учебных заданий (от 1 до 5, типы: выбор ответа, открытый вопрос, практическое)
- Сохранение истории в БД (SQLite / PostgreSQL)

## Команда

| Имя | Роль | GitHub |
|-----|------|--------|
| Милана Майорова | Team Leader | @svyatoslavna |
| Виктория Жиляева | ... | @zhilyaevaviktorija |
| Стефания Чернова | ... | @steffiprog |
| Маргарита Баева  | ... | @ritaveab |
| Екатерина Иванова | ... | @litlsun |
