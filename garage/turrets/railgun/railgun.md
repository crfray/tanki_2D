# Railgun

> Long range turret. Can pierce through tanks by hitting multiple targets in one line.
A big caliber turret with a lightning fast barrel speed. Incredibly powerful and overwhelmingly precise kinetic projectile can make a hole in any tank, hitting several targets standing in the same line. Don't forget that «Railgun» also takes a long time to reload and needs a short preparation before firing every shot.
If medium caliber turrets can no longer satisfy your thirst for creativity, then this toy is just perfect for you. It requires good skills not only in marksmanship, but also in tank positioning. Ready-to-fire barrel will burn brighter than a holiday tree, which can be detected and used as an advantage by experienced enemies.

## Оригинал (Tanki Online)

Референс, не значения игры. Числа в масштабе оригинала.

- damage:              1400
- cooldown time:       4.32
- turning speed:       80
- shot range:          170
- critical hit damage: 1 595

## В игре (`CONFIG.rail`)

Адаптация под свой геймплей. Здоровье считается не тысячами, а попаданиями:
два попадания до смерти (`CONFIG.hp = 2`), крита нет. Рельса двухтактная —
накопление, затем hitscan-выстрел.

| Параметр | Значение | Оригинал-аналог | Смысл |
|---|---|---|---|
| `charge` | 1.05 с | short preparation | держать огонь, пока копится заряд |
| `reload` | 4 с | cooldown 4.32 | пауза между выстрелами |
| `range` | 1400 px | shot range 170 | дальность луча (бьёт через всю арену) |
| `turretTurn` | 2.1 рад/с | turning speed 80 | опорное число баланса; башня проворнее корпуса |
| `beamTime` | 0.55 с | — | сколько след испаряется после выстрела |
| `boltStep` / `boltAmp` | 5 / 2 px | — | мелкие зубчики поверх луча (только рисунок) |
| `chargeSlowMove` | 0.45 | — | во сколько вязнет скорость при накоплении |
| `chargeSlowTurret` | 0.6 | — | во сколько вязнет башня при накоплении |
| `aimKick` | 0.55 рад | — | насколько сбивает прицел цели при попадании |
| урон | 1 попадание | damage 1400 | снимает одно из двух делений здоровья |
| `decal` (в `TURRETS`) | 7 px | — | размер следа на бетоне — самый крупный из трёх |

### Чем выстрел бьёт по цели

Попадание делает три вещи сразу: снимает деление здоровья, отбрасывает прицел
цели на `aimKick` в случайную сторону, срывает её накопленный заряд. Отсюда
дуэль — гонка зарядов: успел первым, и противник теряет и наводку, и энергию.

«Ready-to-fire barrel will burn brighter than a holiday tree» из оригинала
реализовано буквально: пока копится заряд, у дула растёт фиолетовый сгусток —
видимая метка, что танк сейчас медленный.

### Перерисовка по оригиналу

Казна — гранёная коробка из наклонных плит, 22 на 16: на фотографии она
заметно длиннее, чем шире. Ствол тонкий (1.8 у казны, 1.2 у среза) и
ребристый **по всей длине** — в оригинале он собран из секций, и это его
главная примета. Направляющие с бегущим зарядом оставлены: без них
накопление не видно, а оно половина смысла рельсы.

См. [hornet](../../hulls/hornet.md), [wasp](../../hulls/wasp.md).

## Color shots
- red
- violet
- black
- green
- blue
- white-blue
- white
- orange (gold)

