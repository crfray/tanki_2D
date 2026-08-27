# Гараж

Склад **спецификаций** для корпусов (`hulls/`), пушек (`turrets/`) и
карт (`maps/`). Здесь
Markdown, а не код: игра — один HTML-файл, и её игровые числа живут в `CONFIG`
внутри него. Гараж описывает сущности и их происхождение из оригинального
Tanki Online, чтобы было от чего отталкиваться при адаптации баланса.

В будущем это станет основой настоящего гаража, где можно будет менять
вооружение.

## Формат карточки

Каждая карточка держит два масштаба, чтобы не путать одно с другим:

- **Оригинал (Tanki Online)** — исходные характеристики. Референс, а не то,
  что стоит в игре. Числа там в своём масштабе (урон тысячами и т.п.).
- **В игре (`CONFIG`)** — фактические значения, которыми играешь сейчас.
  Источник истины — сам `tanki.html`; карточка обязана с ним совпадать.

## Что где

| Путь | Сущность | Соответствие в `CONFIG` |
|---|---|---|
| `hulls/hornet.md` | Корпус Хорнет (игрок) | `CONFIG.hulls.hornet` |
| `hulls/wasp.md` | Корпус Васп (бот) | `CONFIG.hulls.wasp` |
| `turrets/railgun/railgun.md` | Рельса | `CONFIG.rail` |
| `turrets/twins/twins.md` | Твинс | `CONFIG.twins` |
| `turrets/smoky/smoky.md` | Смоки | `CONFIG.smoky` |
| `turrets/flamethrower/flamethrower.md` | Огнемёт | `CONFIG.flame` |
| `turrets/isida/isida.md` | Изида | `CONFIG.isida` |
| `turrets/freeze/freeze.md` | Фриз | `CONFIG.freeze` |
| `maps/boombox.md` | Карта Boombox | `MAPS.boombox` |
| `maps/sandbox.md` | Карта Sandbox | `MAPS.sandbox` |
| `maps/format.md` | Из чего собраны карты и редактор | `PROPS`, `MAPS` |

Правишь число в `CONFIG` — правишь и карточку. Разошлись — карточка врёт.
