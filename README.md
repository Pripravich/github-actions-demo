# Tennis Match Outcome Predictor

**Нейросеть** для предсказания результата теннисных матчей на основе:
- **Rank_1**, **Rank_2**, **Rank_diff** — рейтинги игроков  
- **WinRate_1**, **WinRate_2** — доля выигранных сетов  
- **Surface** — покрытие (Clay, Grass, Hard, Indoor)  
- **Series** — категория турнира (ATP250, ATP500, ATP1000 и т.д.)

---

## Структура проекта

C:.
├── data/ # Сырые (.csv) и предобработанные данные
├── logs/ # Логи обучения (TensorBoard, CSV, JSON)
├── models/ # Итоговая модель и препроцессор
├── src/ # Исходный код
│ ├── init.py # пакет
│ ├── app.py # Flask API для предсказаний
│ ├── config.py # Параметры и пути
│ ├── data_loader.py # Загрузка и предобработка данных
│ ├── cross_validation.py# K-Fold валидация
│ ├── main.py # Запуск полного пайплайна
│ ├── model.py # Определение нейросети
│ ├── preprocessor.py # Класс DataPreprocessor
│ └── trainer.py # Класс Trainer (обучение модели)
├── test_preprocessing.py # Тесты для preprocess_data
├── test_trainer.py # Smoke-тест для Trainer
├── test_api.py # Тест API (пропускается, если сервер не запущен)
├── requirements.txt # Зависимости проекта
└── README.md # Документация (этот файл)

---

## Установка

1. **Клонировать репозиторий** (замените `<repo_url>` на ваш URL):
   ```bash
   git clone <repo_url>
   cd C:\neeron
