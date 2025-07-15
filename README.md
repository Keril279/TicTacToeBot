# KirPlayer - Игровой бот для крестиков-ноликов / Tic-Tac-Toe Game Bot

## Описание / Description

**KirPlayer** - это игровой бот, реализующий стратегию для игры в крестики-нолики на поле произвольного размера с заданной выигрышной последовательностью. Бот оценивает опасность ходов противника и выбирает оптимальные ходы на основе анализа поля.

**KirPlayer** is a game bot implementing a strategy for playing Tic-Tac-Toe on a field of arbitrary size with a given winning sequence. The bot evaluates the danger of opponent's moves and selects optimal moves based on field analysis.

## Особенности / Features

- Поддержка полей произвольного размера / Supports fields of arbitrary size.
- Адаптивная стратегия, учитывающая ходы противника / Adaptive strategy that considers opponent's moves.
- Оценка "опасности" клеток для принятия решений / Evaluates cell "danger" levels for decision-making.
- Простая интеграция с игровой системой / Easy integration with the game system.

## Использование / Usage

1. **Инициализация бота** / **Initialize the bot**:
   ```cpp
   KirPlayer bot("PlayerName");
   ```
2. **Получение хода** / **Get a move**:
  ```cpp
  Point move = bot.play(gameView);
  ```
3. **Обработка событий** / **Handle events**:
   ```cpp
   bot.notify(gameView, event);
   ```
## Алгоритм / Algorithm

Бот использует следующий алгоритм:
    - Для каждой клетки в окрестности последних ходов вычисляется "уровень опасности".
    - Опасность определяется количеством потенциальных выигрышных последовательностей.
    - Бот выбирает ход с максимальной опасностью для противника или минимальной опасностью для себя.

The bot uses the following algorithm:
    - For each cell in the vicinity of the last moves, a "danger level" is calculated.
    - Danger is determined by the number of potential winning sequences.
    - The bot selects the move with the highest danger for the opponent or the lowest danger for itself.

## Пример / Example
  ```cpp
  KirPlayer player("Kir");
  Point move = player.play(game.get_view());
  ```

## Зависимости / Dependencies
    C++17 или новее / C++17 or newer.
    Заголовочные файлы из проекта / Header files from the project.
