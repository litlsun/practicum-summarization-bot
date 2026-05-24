# practicum-summarization-bot
A chatbot for automatic transcription, summarization of audio lectures, and subsequent generation of study tasks to convert synchronous learning into asynchronous learning.

# Lecture Assistant Bot

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

lecture-assistant-bot/
├── bot.py                 # Главный файл бота
├── asr.py                 # Транскрибация (Whisper)
├── summarizer.py          # Суммаризация (Yandex Cloud LLM)
├── questions.py           # Генерация заданий
├── database.py            # Работа с БД
├── config.py              # Загрузка переменных окружения
├── utils.py               # Вспомогательные функции
├── requirements.txt       # Зависимости
├── .env.example           # Пример переменных окружения
├── .gitignore
├── README.md              # Этот файл
└── docs/                  # Полная документация
    ├── user-guide.md
    ├── architecture.md
    ├── development-guide.md
    └── deployment.md
    
## Функциональность

- Загрузка аудио (MP3, WAV, M4A, OGG) и видео (MP4 — конвертация в аудио)
- Транскрибация через Whisper
- Суммаризация через Yandex Cloud API
- Генерация учебных заданий (от 1 до 5, типы: выбор ответа, открытый вопрос, практическое)
- Сохранение истории в БД (SQLite / PostgreSQL)

## Команда

| Имя | Роль | GitHub |
|-----|------|--------|
| ... | ... | @... |
