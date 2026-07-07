project/
├── docker-compose.yml          # Оркестрация всех контейнеров
├── .env                        # Переменные окружения
├── .dockerignore               # Файлы, игнорируемые Docker
├── Makefile                    # Утилиты для управления проектом
├── backend/                    # ВСЕ файлы серверной части
│   ├── Dockerfile              # Инструкция сборки контейнера
│   ├── package.json            # Зависимости Node.js
│   ├── tsconfig.json           # Настройки TypeScript
│   ├── .env                    # Переменные окружения для бэка
│   └── src/                    # Исходный код приложения
│       ├── server.ts           # Точка входа (запуск сервера)
│       ├── config/             # Конфигурации
│       │   └── database.ts     # Подключение к MySQL
│       ├── entities/           # Модели данных (сущности)
│       │   └── User.ts         # Модель пользователя
│       ├── repositories/       # Слой работы с БД
│       │   ├── IRepository.ts  # Интерфейс репозитория
│       │   ├── BaseRepository.ts # Базовый класс репозитория
│       │   └── UserRepository.ts # Репозиторий пользователей
│       ├── services/           # Слой бизнес-логики
│       │   ├── IUserService.ts # Интерфейс сервиса
│       │   └── UserService.ts  # Сервис пользователей
│       ├── controllers/        # Слой обработки HTTP
│       │   └── UserController.ts # Контроллер пользователей
│       ├── routes/             # Маршруты API
│       │   └── userRoutes.ts   # Маршруты для пользователей
│       └── utils/              # Вспомогательные утилиты
│           └── errorHandler.ts # Обработка ошибок
└── mysql/                      # Настройки MySQL
    └── init/                   # Скрипты инициализации
        └── 01-init.sql         # Создание таблиц и тестовые данные