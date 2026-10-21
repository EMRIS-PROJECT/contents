# contents

Ассеты публичного сервера [EMRIS-PROJECT/public-server](https://github.com/EMRIS-PROJECT/public-server): модели, звуки и спрайты. Структура повторяет папку `cstrike`, распаковывается поверх неё.

| Путь | Где используется |
|---|---|
| `models/pb_files/weapons/v_knife_*` | `pb_knife_menu` — скины ножей |
| `models/pb_files/v_climb.mdl` | `pb_parkour` — анимация залаза |
| `models/pb_files/v_zombie_hands.mdl`, `p_null.mdl` | `pb_virus_grenade` — руки зомби |
| `models/pb_files/mini_games/*`, `sound/pb_files/mini_games/*`, `sprites/pb_files/mini_games/*` | мини-игры `pb_mg_*` |
| `sprites/wall.spr` | `pb_walls` |

Чего здесь нет, но сборка подхватит, если положить:

- `models/player/zombie/zombie.mdl` — модель зомби (без неё зомби остаются в своей модели);
- `models/player/<имя>/<имя>.mdl` — модели из `configs/pb/models.ini` (по умолчанию `vip`).

## Версии

Каждое изменение набора ассетов — новый тег `vX.Y.Z`. Сборка сервера закрепляет конкретный тег в `amxbuild.yml`, так что обновление ассетов не ломает уже выпущенные релизы.
