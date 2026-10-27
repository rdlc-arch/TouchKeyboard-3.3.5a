Claude (Anthropic) generated

# TouchKeyboard

An on-screen touch keyboard for **World of Warcraft 3.3.5a (WotLK)**.

It is made for playing on a **touchscreen or with a controller**: Android emulators (GameHub, Winlator and similar), handhelds like the Lenovo Legion Go or Steam Deck, or any setup without a physical keyboard. The keyboard pops up when you click into chat or any other text box, and you type by tapping the keys.

## Features

- Pops up automatically when any text box gets focus: chat, mail, Auction House search, macros, addon search boxes
- Hides by itself after you send a message or close the text box
- A movable **Chat** button opens chat and the keyboard in one tap
- Big 44 px keys made for fingers
- Move the keyboard by dragging its title bar, and resize it with the **– / +** buttons
- Position, size and settings are saved between sessions
- **Shift**: tap once for one capital letter, double-tap for caps lock
- **?123** switches to a page of numbers and symbols
- Hold **Del** to keep deleting
- No libraries or other addons needed

## Installation

1. Download the latest release and extract it.
2. Put the `TouchKeyboard` folder into `World of Warcraft/Interface/AddOns/`.
   The result should be `Interface/AddOns/TouchKeyboard/TouchKeyboard.toc`, **not** `AddOns/TouchKeyboard/TouchKeyboard/...`.
3. On the character select screen, click **AddOns** and make sure TouchKeyboard is enabled. If it shows as "out of date", tick **Load out of date AddOns**.

On Android emulators the `Interface/AddOns` folder is inside the game folder you set up in the emulator, the same place as on PC.

## How to use

- Tap the **Chat** button, or tap into any text box, and the keyboard appears.
- Type, then tap **Enter** to send. Tap **Hide** or **X** to close the keyboard without sending.
- Drag the **Chat** button to wherever suits your thumbs.
- **Esc** is on the **?123** page.

### Slash commands

| Command | What it does |
|---|---|
| `/tkb` | Show or hide the keyboard. Opened this way, it stays open until you close it. |
| `/tkb reset` | Reset the keyboard's size and position, and the Chat button's position |
| `/tkb autoshow` | Turn automatic pop-up on or off |
| `/tkb autohide` | Turn automatic hiding on or off |
| `/tkb launcher` | Show or hide the Chat button |

## What to know

- **It only types inside WoW.** It's a WoW addon, not a system keyboard, so it can't type into your emulator, Windows or Android.
- **It's only for typing text.** It can't press keybinds, cast spells or move your character. The game doesn't let addons press keys. That's by design, and it's why the addon is safe to use.
- **It doesn't automate anything.** It doesn't send messages for you or read game data. It just inserts the characters you tap into the text box you're using.
- **On a touchscreen, a tap must count as a left mouse click.** In most emulators that's the default touch or mouse mode. If keys don't respond, check your emulator's touch settings.
- Settings are saved per account in `WTF/Account/<name>/SavedVariables/TouchKeyboard.lua`. Delete that file to reset everything.

## Known limitations

- **English QWERTY only.** There are no accented letters (ă, é, ß, …) and no other layouts yet.
- **No clipboard paste.** WoW 3.3.5a doesn't give addons access to the clipboard.
- **No arrow keys or cursor movement.** Text is inserted where the cursor is. To edit the middle of a line, tap into the text box at that spot, if your input method allows it.
- **One key at a time.** There's no multi-touch, so tapping two keys at once only registers one.
- **Item, spell and quest links:** deleting text next to or inside a link with **Del** may break the link. If that happens, clear the line and link the item again.
- Only **Del** repeats when held. Other keys type once per tap.
- **Enter** does whatever that text box normally does on Enter. Some addon text boxes ignore Enter, so it does nothing there.
- The pop-up triggers on **every** text box, including addon search fields. If that's annoying, turn it off with `/tkb autoshow` and use the Chat button or `/tkb`.
- The keyboard sits above most windows (DIALOG layer), so it can cover parts of the Auction House, mail or bank. Drag it out of the way; it remembers where you put it.
- It's only built and tested for **3.3.5a** (interface 30300). It won't work on retail or Classic without changes.
- Other UI or chat replacement addons (ElvUI, Prat and similar) should work, since it types into whichever box has focus, but that hasn't been widely tested.

## Bug reports

Please include:
- What you were doing, for example typing in guild chat or searching in the AH
- The full Lua error text, if any. Turn errors on with `/console scriptErrors 1`, or use BugGrabber/BugSack.
- Your setup: PC, Android plus which emulator, Legion Go, Steam Deck…
- Other UI addons you use

## Credits

Created by **[YOUR NAME]**.
Written with help from Claude (Anthropic's AI assistant). It doesn't include code from other addons; it only uses the game's standard interface functions.

## License

MIT. See [LICENSE](LICENSE). You're free to use, modify and share it; please keep the copyright notice.
