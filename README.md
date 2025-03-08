```markdown
# Telegram Channel Reposter Bot 🤖

Бот для автоматической пересылки и рерайта сообщений между Telegram-каналами с использованием AI (OpenRouter).

## 📌 Основные возможности
- 🔄 Автоматическая пересылка сообщений между каналами
- ✍️ Авто-рерайт текста с сохранением смысла через ИИ
- 🛠 Простое управление каналами через чат-команды
- 💾 Автосохранение настроек между перезапусками

## ⚙️ Требования
- Python 3.10 или новее
- [OpenRouter.ai](https://openrouter.ai/) API ключ
- Telegram API ключи ([инструкция](#-получение-api-ключей))

## 🚀 Быстрый старт

### 1. Установка зависимостей
```bash
git clone https://github.com/nikiarohK/tg_bot.git
cd ваш-репозиторий
pip install -r requirements.txt
```

### 2. Настройка конфигурации
Создайте файл `config.py` в корне проекта:
```python
# Telegram API
api_id = "123456"          # Ваш Telegram API ID
api_hash = "abcdef123456"  # Ваш Telegram API Hash
bot_token = "123:ABCdef"   # Токен бота от @BotFather

# OpenRouter API
api_ai = "sk-or-123456"    # Ключ с openrouter.ai
```

### 3. Получение API-ключей
#### Telegram API:
1. Перейдите на [my.telegram.org](https://my.telegram.org/)
2. Создайте приложение в разделе **API Development Tools**
3. Скопируйте `api_id` и `api_hash`

#### OpenRouter:
1. Зарегистрируйтесь на [OpenRouter.ai](https://openrouter.ai/)
2. В настройках профиля создайте API-ключ
3. Выберите модель `deepseek-r1-zero:free` в настройках ключа

### 4. Запуск бота
```bash
python main.py
```

## 🕹 Команды управления
| Команда | Описание | Пример |
|---------|-----------|--------|
| `/start` | Основное меню помощи | `/start` |
| `/main_channel [ссылка]` | Установить целевой канал | `/main_channel https://t.me/my_channel` |
| `/add_channel [ссылка]` | Добавить отслеживаемый канал | `/add_channel https://t.me/source_channel` |
| `/remove [ссылка]` | Удалить канал из списка | `/remove https://t.me/source_channel` |
| `/list` | Показать все отслеживаемые каналы | `/list` |
| `/status` | Текущее состояние бота | `/status` |

## 🛠 Решение проблем
- **"Канал не найден"**: 
  - Убедитесь, что бот добавлен в канал как администратор
  - Проверьте правильность ссылки на канал
- **"Нет прав доступа"**:
  - Проверьте API-ключи в config.py
  - Убедитесь, что бот имеет права на отправку сообщений
- **Ошибки OpenRouter**:
  - Проверьте баланс на [OpenRouter Dashboard](https://openrouter.ai/keys)
  - Убедитесь, что модель активна в настройках ключа

## 📄 Лицензия
Проект распространяется под лицензией MIT. Подробности в файле [LICENSE](LICENSE).

---

💡 После запуска отправьте боту команду `/start` для получения полного списка возможностей!

[![Telegram Bot API](https://img.shields.io/badge/Telegram-Bot%20API-blue)](https://core.telegram.org/bots)
[![OpenRouter.ai](https://img.shields.io/badge/Powered%20by-OpenRouter.ai-orange)](https://openrouter.ai/)