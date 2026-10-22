# PathoMod 1.0 - Interactable Object Markers for Pathologic Classic HD

**PathoMod** is a lightweight mod for the Steam version of *Pathologic Classic HD* that displays markers above objects you can interact with. Hold **Tab** to reveal nearby objects, similar to the interaction highlighting found in Fallout and other CRPGs.

## Features

- **NPC markers:** cyan diamonds.
- **Door markers:** orange diamonds.
- **Object markers:** green diamonds.
- **Selected target marker:** yellow, indicating the object currently selected by the game's own targeting system.
- **Wall occlusion:** markers can be hidden behind walls and other geometry.
- **Configurable distance:** the default detection range is 40 metres.
- **Customizable controls:** change the keys used to show markers, toggle persistent display, and enable or disable depth testing.
- **Optional categories:** configure which types of markers are displayed.

The mod uses a local `d3d9.dll` proxy to load the original system Direct3D 9 library and draw markers during rendering. It reads object information from the game's memory and does not modify game data or save files. It does not connect to the internet.

## Requirements and compatibility

- Steam version of *Pathologic Classic HD*.
- Windows and DirectX 9.
- The specific game build listed in the documentation.

The mod has been verified against a particular executable and engine DLL build. If your files differ, the mod displays three red squares while the marker key is held instead of drawing object markers. The documented screen resolution is 1920×1080; other resolutions and aspect ratios have not been tested.

## Installation

1. Locate the game's `Game.exe`.
2. Copy `d3d9.dll` into the same directory as `Game.exe`.
3. Launch the game through Steam and hold **Tab**.

The first scan after starting the game or changing locations may take 1–2 seconds. An amber square indicates that scanning is in progress.

## Configuration

On first launch, the mod creates `pathomod.ini` beside `Game.exe`. You can change the marker keys, maximum distance, marker size, depth testing, and marker categories. Developer hotkeys and detailed logging are disabled by default; set `debug=1` to enable them.

## Known limitations

NPCs are marked even when they cannot be spoken to, because the game does not expose a suitable flag. Large objects may have markers offset from their visual centre. Newly spawned objects may take up to approximately 30 seconds to appear. The mod is incompatible with other Direct3D 9 wrappers using the same `d3d9.dll` filename, such as ReShade for DX9.

See the Russian documentation below for further installation details and troubleshooting.

---

# PathoMod 1.0 — Подсветка интерактивных объектов для Pathologic Classic HD

**PathoMod** — небольшой мод для Steam-версии *Pathologic Classic HD*, который отображает маркеры над объектами, с которыми можно взаимодействовать. Удерживайте **Tab**, чтобы увидеть ближайшие объекты, как в Fallout и других CRPG с подсветкой взаимодействия.

## Возможности

- **NPC:** голубые ромбы.
- **Двери:** оранжевые ромбы.
- **Предметы и объекты:** зелёные ромбы.
- **Текущая цель:** жёлтый маркер у объекта, выбранного самой игрой.
- **Скрытие за стенами:** маркеры могут исчезать за стенами и другими препятствиями.
- **Настраиваемая дальность:** по умолчанию 40 метров.
- **Настраиваемое управление:** можно менять клавиши показа маркеров, постоянного отображения и проверки глубины.
- **Настраиваемые категории:** можно отдельно включать и отключать разные типы маркеров.

Мод использует локальную прокладку `d3d9.dll`, загружает оригинальную системную библиотеку Direct3D 9 и рисует маркеры во время рендеринга. Информация об объектах считывается из памяти игры. Мод не изменяет игровые данные и сохранения и не подключается к интернету.

## Требования и совместимость

- Steam-версия *Pathologic Classic HD*.
- Windows и DirectX 9.
- Конкретная сборка игры, указанная в документации.

Совместимость проверена с определёнными версиями исполняемого файла и библиотеки движка. Если файлы отличаются, при удержании клавиши показа вместо маркеров отображаются три красных квадрата. Проверенное разрешение — 1920×1080; другие разрешения и соотношения сторон не тестировались.

## Установка

1. Найдите `Game.exe` в папке игры.
2. Скопируйте `d3d9.dll` в ту же папку.
3. Запустите игру через Steam и удерживайте **Tab**.

Первый поиск объектов после запуска или смены локации может занимать 1–2 секунды. Во время поиска отображается янтарный квадрат.

## Настройки

При первом запуске рядом с `Game.exe` создаётся `pathomod.ini`. В нём можно изменить клавиши, максимальную дальность, размер маркеров, проверку глубины и отображаемые категории. Служебные клавиши разработчика и подробное логирование отключены по умолчанию; для их включения установите `debug=1`.

## Известные ограничения

NPC отмечаются даже тогда, когда с ними нельзя поговорить: игра не предоставляет подходящего флага. У крупных объектов маркер может находиться не по центру. Новые объекты могут появляться с задержкой до 30 секунд. Мод несовместим с другими прокладками Direct3D 9, использующими то же имя `d3d9.dll`, например с ReShade для DX9.

Подробности установки и устранения неполадок приведены в документации на русском языке.
