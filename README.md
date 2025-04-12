# fantasy-adventure-game
то приключенческая игра в жанре фэнтези, где игроки могут исследовать обширный мир, выполнять квесты и сражаться с различными врагами. Игра включает в себя систему уровней, уникальных персонажей и множество предметов для сбора. 


# Pure

Pure — это веб-приложение, представляющее собой многопользовательскую компьютерную игру, в которой игроки могут исследовать виртуальный мир, выполнять квесты и сражаться с противниками. Игра предлагает уникальный опыт взаимодействия с другими игроками и возможность развивать своего персонажа.

## Описание проекта

Pure — это многопользовательская игра, разработанная для браузеров. Игроки могут создавать своих персонажей, исследовать обширные локации, выполнять задания и участвовать в боях с другими игроками. Игра включает в себя элементы RPG и стратегии, что делает ее интересной для широкой аудитории.

**Технологии, использованные в проекте:**  
- Backend: **Node.js** + **Express**  
- Frontend: **React**  
- База данных: **MongoDB**  
- Система сборки: **Webpack**  
- Тестирование: **Jest**, **Supertest**  

## Требования

Для работы с проектом необходимо установить:
- **Node.js** версии 16+  
- **npm** версии 8+  
- **MongoDB** для работы с базой данных  

Дополнительно можно использовать **Docker** для упрощения настройки окружения.

## Установка и запуск

1. Склонируйте репозиторий:  
   ```bash
   git clone https://github.com/yourusername/pure.git
   ```

2. Перейдите в директорию проекта:  
   ```bash
   cd pure
   ```

3. Установите все зависимости:  
   ```bash
   npm install
   ```

4. Настройте переменные окружения (создайте файл `.env`):
   ```bash
   DATABASE_URL=mongodb://localhost:27017/game_database
   PORT=3000 
   ```

5. Запустите сервер:  
   ```bash
   npm start
   ```

6. Перейдите в браузер по адресу:  
   `http://localhost:3000`

7. Если хотите развернуть проект с помощью Docker, используйте следующий команду:
   ```bash
   docker-compose up
   ```

## Использование

После запуска приложения откройте браузер и перейдите по следующему адресу:
`http://localhost:3000`

### Основные функции:
1. **Создание персонажа**: Игроки могут настраивать внешний вид и характеристики своего персонажа, выбирая из различных опций, таких как раса, класс, навыки и внешний вид.
2. **Исследование мира**: Огромный открытый мир с различными локациями, которые можно исследовать. Игроки могут находить скрытые места, собирать ресурсы и взаимодействовать с окружающей средой.
3. **Выполнение квестов**: Игроки могут принимать участие в квестах, получая за это награды. Квесты могут быть как основными, так и побочными, предлагая разнообразные задачи и истории.
4. **Сражения с противниками**: Возможность сражаться как с NPC (неигровыми персонажами), так и с другими игроками. Бои могут включать в себя различные стратегии и тактики, а также использование уникальных навыков персонажа.

## Пример использования API

Если вы хотите использовать API для взаимодействия с игрой, вот несколько примеров запросов:

### Добавление новой задачи:
```bash
GET /api/character?username=player1

```
{
  "username": "player1",
  "level": 10,
  "experience": 1500,
  "health": 100,
  "mana": 50,
  "inventory": ["sword", "potion"]
}
### Получение списка квестов:
```bash
GET /api/quests?username=player1
```

### Выполнение атаки на противника:
```bash
POST /api/battles/attack
Content-Type: application/json

{
    "characterId": "12345",
    "enemyId": "54321"
}
```

### Получение информации о предмете в инвентаре:
```bash
GET /api/items/sword?username=player1 
```

### Обновление характеристик персонажа:
```bash
PUT /api/characters/12345
Content-Type: application/json

{
    "level": 2,
    "experience": 3000,
    "health": 120,
    "mana": 60
}
```

## Лицензия

Этот проект распространяется под лицензией MIT. Подробнее смотрите в файле [LICENSE](LICENSE).

