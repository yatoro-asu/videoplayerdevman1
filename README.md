# Видео-плеер

Кастомный видео-плеер с панелью управления: воспроизведение/пауза, регулировка громкости, полноэкранный режим и прогресс-бар.

## Как установить

**Требуется:** браузер и редактор кода.

1. Откройте `index.html` в браузере — плеер готов к работе.

## Как выглядит плеер

<img width="1047" height="782" alt="videoplayer" src="https://github.com/user-attachments/assets/95a689ca-efc3-4305-ba34-fa7b3a590874" />


**Для разработки с автообновлением:**

```bash
# Установите зависимости
pip install livereload

# Запустите сервер разработки
python server.py
```

Сервер запустится на порту `5501` с поддержкой LiveReload.

## Структура проекта

- `index.html` | Разметка плеера |
- `style.css` | Стили интерфейса |
- `player.js` | Логика управления (библиотека [Playable](https://github.com/liftoffio/playable)) |
- `server.py` | Dev-сервер с автообновлением |

## Как использовать

```html
<!-- Подключите скрипты в конце <body> -->
<script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
<script src="https://unpkg.com/playable@2.10.3/dist/statics/playable.bundle.min.js"></script>
<script src="player.js"></script>

<!-- Инициализация плеера -->
<script>
  createPlayer({ 
    elementId: 'player',
    src: 'ссылка_на_видео.mp4'  // опционально
  });
</script>
```

## Кастомизация

- **Видео**: измените `src` в `createPlayer()` или передайте при инициализации.
- **Стили**: отредактируйте `style.css` (цвета, размеры, отступы).
- **Кнопки**: в `player.js` можно добавить новые обработчики событий.

## Зависимости

- [Playable 2.10.3](https://unpkg.com/playable@2.10.3) | Воспроизведение видео |
- [jQuery 3.4.1](https://code.jquery.com/) | Работа с DOM |
- [Font Awesome 4.7](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css) | Иконки кнопок |

## Цель проекта

Образовательный пример создания кастомного UI для видео-плеера с использованием внешних библиотек.




