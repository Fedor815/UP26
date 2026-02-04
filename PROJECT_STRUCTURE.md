echo # 🏗️ Структура проекта praktika26 > PROJECT_STRUCTURE.md
echo. >> PROJECT_STRUCTURE.md
echo ## 📁 Корневая директория проекта >> PROJECT_STRUCTURE.md
echo. >> PROJECT_STRUCTURE.md
echo \`\`\` >> PROJECT_STRUCTURE.md
echo praktika26/ >> PROJECT_STRUCTURE.md
echo ├── 📄 .env.example                    # Шаблон переменных окружения >> PROJECT_STRUCTURE.md
echo ├── 📄 .gitignore                     # Игнорируемые Git файлы >> PROJECT_STRUCTURE.md
echo ├── 📄 docker-compose.yml             # Docker конфигурация >> PROJECT_STRUCTURE.md
echo ├── 📄 README.md                      # Описание проекта >> PROJECT_STRUCTURE.md
echo ├── 📄 BUSINESS_REQUIREMENTS.md       # Бизнес-требования >> PROJECT_STRUCTURE.md
echo ├── 📄 USER_STORIES.md                # User Stories >> PROJECT_STRUCTURE.md
echo ├── 📄 PROJECT_STRUCTURE.md           # Этот файл >> PROJECT_STRUCTURE.md
echo ├── 📁 backend/                       # FastAPI бэкенд >> PROJECT_STRUCTURE.md
echo ├── 📁 frontend/                      # React фронтенд >> PROJECT_STRUCTURE.md
echo ├── 📁 telegram_bot/                  # Telegram бот >> PROJECT_STRUCTURE.md
echo ├── 📁 docs/                          # Документация >> PROJECT_STRUCTURE.md
echo ├── 📁 tests/                         # Тесты >> PROJECT_STRUCTURE.md
echo └── 📁 docker/                        # Docker файлы >> PROJECT_STRUCTURE.md
echo \`\`\` >> PROJECT_STRUCTURE.md 
## 🐍 Backend (FastAPI)
backend/
├── 📁 app/ # Основное приложение
│ ├── 📄 init.py
│ ├── 📄 main.py # Точка входа FastAPI
│ ├── 📁 api/ # Роутеры API
│ │ ├── 📄 init.py
│ │ ├── 📄 auth.py # Аутентификация
│ │ ├── 📄 competitors.py # Конкуренты
│ │ ├── 📄 products.py # Товары
│ │ └── 📄 parsing.py # Управление парсингом
│ ├── 📁 core/ # Ядро приложения
│ │ ├── 📄 init.py
│ │ ├── 📄 config.py # Конфигурация
│ │ ├── 📄 security.py # Безопасность
│ │ └── 📄 dependencies.py # Зависимости
│ ├── 📁 db/ # Работа с БД
│ │ ├── 📄 init.py
│ │ ├── 📄 base.py # Базовый класс моделей
│ │ ├── 📄 session.py # Сессии БД
│ │ └── 📄 init_db.py # Инициализация БД
│ ├── 📁 models/ # SQLAlchemy модели
│ │ ├── 📄 init.py
│ │ ├── 📄 user.py # Пользователи
│ │ ├── 📄 competitor.py # Конкуренты
│ │ ├── 📄 product.py # Товары
│ │ └── 📄 price_history.py # История цен
│ ├── 📁 schemas/ # Pydantic схемы
│ │ ├── 📄 init.py
│ │ ├── 📄 user.py
│ │ ├── 📄 competitor.py
│ │ └── 📄 product.py
│ └── 📁 services/ # Бизнес-логика
│ ├── 📄 init.py
│ ├── 📄 parser_service.py # Сервис парсинга
│ ├── 📄 competitor_service.py # Сервис конкурентов
│ ├── 📄 notification_service.py # Сервис уведомлений
│ └── 📄 analytics_service.py # Сервис аналитики
├── 📁 migrations/ # Миграции Alembic
│ ├── 📄 versions/
│ ├── 📄 env.py
│ └── 📄 script.py.mako
├── 📄 alembic.ini # Конфиг Alembic
├── 📄 requirements.txt # Зависимости Python
├── 📄 Dockerfile # Docker образ бэкенда
└── 📄 .env.example # Переменные окружения

## ⚛️ Frontend (React)
frontend/
├── 📁 public/ # Статические файлы
│ ├── 📄 index.html
│ ├── 📄 favicon.ico
│ └── 📄 robots.txt
├── 📁 src/ # Исходный код
│ ├── 📁 api/ # API клиенты
│ │ ├── 📄 axiosConfig.js
│ │ ├── 📄 authAPI.js
│ │ ├── 📄 competitorAPI.js
│ │ └── 📄 productAPI.js
│ ├── 📁 components/ # React компоненты
│ │ ├── 📁 common/ # Общие компоненты
│ │ │ ├── 📄 Header.jsx
│ │ │ ├── 📄 Sidebar.jsx
│ │ │ └── 📄 LoadingSpinner.jsx
│ │ ├── 📁 dashboard/ # Дашборд
│ │ │ ├── 📄 PriceChart.jsx
│ │ │ ├── 📄 CompetitorTable.jsx
│ │ │ └── 📄 AnalyticsCard.jsx
│ │ └── 📁 admin/ # Админ компоненты
│ │ ├── 📄 UserManagement.jsx
│ │ └── 📄 SystemSettings.jsx
│ ├── 📁 pages/ # Страницы
│ │ ├── 📄 Login.jsx
│ │ ├── 📄 Dashboard.jsx
│ │ ├── 📄 Competitors.jsx
│ │ ├── 📄 Products.jsx
│ │ └── 📄 Settings.jsx
│ ├── 📁 store/ # State management
│ │ ├── 📄 authSlice.js
│ │ └── 📄 competitorSlice.js
│ ├── 📁 styles/ # Стили
│ │ ├── 📄 main.css
│ │ └── 📄 variables.css
│ ├── 📄 App.jsx # Главный компонент
│ ├── 📄 index.jsx # Точка входа
│ └── 📄 routes.jsx # Маршрутизация
├── 📄 package.json # Зависимости Node.js
├── 📄 Dockerfile # Docker образ фронтенда
└── 📄 .env.example # Переменные окружения

## 🤖 Telegram Bot
telegram_bot/
├── 📁 handlers/ # Обработчики команд
│ ├── 📄 init.py
│ ├── 📄 start.py # /start
│ ├── 📄 help.py # /help
│ ├── 📄 price_check.py # /price
│ ├── 📄 alerts.py # Управление алертами
│ └── 📄 admin.py # Админ команды
├── 📁 services/ # Сервисы
│ ├── 📄 init.py
│ ├── 📄 database.py # Работа с БД
│ ├── 📄 api_client.py # Клиент к основному API
│ └── 📄 notification.py # Отправка уведомлений
├── 📁 utils/ # Утилиты
│ ├── 📄 init.py
│ ├── 📄 keyboards.py Клавиатуры бота
│ ├── 📄 validators.py # Валидация
│ └── 📄 logger.py # Логирование
├── 📄 bot.py # Главный файл бота
├── 📄 config.py # Конфигурация
├── 📄 requirements.txt # Зависимости Python
├── 📄 Dockerfile # Docker образ бота
└── 📄 .env.example # Переменные окружения

## 📚 Документация
docs/
├── 📁 api/ # API документация
│ ├── 📄 endpoints.md
│ └── 📄 examples.md
├── 📁 deployment/ # Развертывание
│ ├── 📄 local_setup.md
│ ├── 📄 production.md
│ └── 📄 docker.md
├── 📁 user_guides/ # Руководства пользователя
│ ├── 📄 admin_guide.md
│ ├── 📄 user_guide.md
│ └── 📄 api_usage.md
├── 📄 architecture.md # Архитектура системы
└── 📄 contributing.md # Как внести вклад

## 🐳 Docker
docker/
├── 📄 backend.Dockerfile # Dockerfile для бэкенда
├── 📄 frontend.Dockerfile # Dockerfile для фронтенда
├── 📄 bot.Dockerfile # Dockerfile для бота
└── 📄 nginx.conf # Конфиг Nginx

## 🧪 Тесты
tests/
├── 📁 backend/ # Тесты бэкенда
│ ├── 📄 test_auth.py
│ ├── 📄 test_parsing.py
│ └── 📄 test_api.py
├── 📁 frontend/ # Тесты фронтенда
│ └── 📄 App.test.jsx
└── 📁 integration/ # Интеграционные тесты
└── 📄 test_e2e.py

## 🚀 Как начать работу

### 1. Установка зависимостей
```bash
# Бэкенд
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt

# Фронтенд
cd frontend
npm install

# Telegram бот
cd telegram_bot
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt