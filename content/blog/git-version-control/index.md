---
title: "Управление версиями. Git"
date: 2026-03-22
authors: ["admin"]
tags: ["Git", "Программирование"]
---

## Что такое Git

Система контроля версий. Позволяет отслеживать изменения в коде, работать в команде и хранить историю проекта.

---

## Команды

### Настройка
```bash
git config --global user.name "Имя"
git config --global user.email "email"
```

### Клонирование
```bash
git clone <url>
```

### Статус и история
```bash
git status                    # что изменилось
git log --oneline             # последние коммиты
```

### Работа с изменениями
```bash
git add .                     # добавить всё
git commit -m "что сделал"    # сохранить
git push                      # отправить на GitHub
```

### Работа с ветками
```bash
git checkout -b новая-ветка   # создать и переключиться
git checkout main             # вернуться на основную
git merge новая-ветка         # слить ветку
```

### Работа с удалённым репозиторием
```bash
git remote add origin <url>   # привязать удалённый репозиторий
git pull origin main          # получить изменения перед работой
```


## Как это работает

**1. Отдельная ветка под задачу**
```bash
git checkout -b новая-фича
```

**2. Пишем код**
(работаем с файлами)

**3. Коммит с пояснением**
```bash
git add .
git commit -m "добавил новую фичу"
```


**4. Отправляем на GitHub**
```bash
git push origin новая-фича
```


**5. Просим посмотреть код**
(создаём Pull Request на GitHub)

**6. Вливаем, если всё ок**
```bash
git checkout main
git pull
git merge новая-фича
git push
```
