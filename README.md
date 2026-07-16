<p align="center">
  <img src="https://catbridge.guildwar.win/images/catbridge-logo.png" width="96" alt="CatBridge logo">
</p>

# CatBridge

**Play Guild Wars 2 in your language.**

CatBridge translates story dialogue, Guild Wars 2 chat, screen OCR, Discord voice, TTS, voice chat input, custom cursors, and WvW combat reports in one companion app.

Official site: https://catbridge.guildwar.win

Community Discord: https://discord.gg/hndrDWN7zA

> CatBridge is closed-source software. This repository is used for public releases, issue tracking, and update notes.

## The App

Choose a language and translation engine, then start playing.

CatBridge runs while Guild Wars 2 is open. Menus and settings can use several UI languages. Even if a UI language is not available, chat and dialogue translation still work.

<img src="https://catbridge.guildwar.win/images/v11/ui-localization-language-list.png" alt="CatBridge language and engine settings">

CatBridge initial setup page. The UI changes to the language you choose when that UI locale is available. If the UI locale is not available, all features still work.

## Story, Chat, And Your Own Messages

NPC dialogue and Guild Wars 2 chat are translated directly from game data. Your own message can be translated before you send it.

<table>
  <tr>
    <td width="50%">
      <img src="images/readme/story-ko.jpg" alt="CatBridge story dialogue translated into Korean"><br>
      <strong>Story translation</strong> keeps NPC lines readable while the game stays open.
    </td>
    <td width="50%">
      <img src="https://catbridge.guildwar.win/images/v11/input-translate-output.png" alt="CatBridge translated outgoing chat input"><br>
      <strong>Outgoing chat</strong> can be sent instantly in the selected language, or copied first when you want to check it.
    </td>
  </tr>
</table>

## See It In Action

Multilingual translation examples from earlier CatBridge builds.

<table>
  <tr>
    <td width="50%">
      <img src="https://catbridge.guildwar.win/images/chat2-jpn.png" alt="Party chat translated into Japanese"><br>
      <strong>Party chat</strong><br>Japanese<br><em>Old UI screenshot.</em>
    </td>
    <td width="50%">
      <img src="https://catbridge.guildwar.win/images/chat5-port.png" alt="Party chat translated into Portuguese"><br>
      <strong>Party chat</strong><br>Portuguese<br><em>Old UI screenshot.</em>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <img src="https://catbridge.guildwar.win/images/story-turkey.png" alt="NPC story dialogue translated into Turkish"><br>
      <strong>NPC story</strong><br>Turkish<br><em>Old UI screenshot.</em>
    </td>
    <td width="50%">
      <img src="https://catbridge.guildwar.win/images/story-pol.png" alt="NPC story dialogue translated into Polish"><br>
      <strong>NPC story</strong><br>Polish<br><em>Old UI screenshot.</em>
    </td>
  </tr>
</table>

CatBridge supports dozens of languages through free translation engines and optional AI engines, including English, French, German, Spanish, Russian, Arabic, and Thai.

## More Than Chat Translation

CatBridge now covers native translation, OCR, Discord voice translation, cursor tools, and WvW reports.

<img src="images/readme/ocr-combined-ko.jpg" alt="CatBridge OCR translating Guild Wars 2 screen text">

**OCR** translates non-chat screen text such as objectives, skills, achievements, and dialogue choices by dragging over it.

<table>
  <tr>
    <td width="33%">
      <img src="https://catbridge.guildwar.win/images/v11/discord-caption-ko.png" alt="CatBridge Discord voice translation over Guild Wars 2"><br>
      <strong>Discord voice translation</strong> captures the Discord voice session and shows captions in the language you choose.
    </td>
    <td width="33%">
      <img src="https://catbridge.guildwar.win/images/v11/mobility-editor-ko.png" alt="CatBridge Mobility Tech cursor editor"><br>
      <strong>Mobility Tech</strong> replaces the GW2 cursor. You can customize it, share presets by code, and change colors between combat and non-combat states.
    </td>
    <td width="33%">
      <img src="images/readme/combat-report-wvw.jpg" alt="CatBridge WvW combat report overlay"><br>
      <strong>Combat Tech</strong> uses AxiBridge to share quick WvW combat reports in chat or view detailed results in an overlay window.
    </td>
  </tr>
</table>

## Translation First, Useful Tools Around It

Understand story, talk with players, translate screen text, and handle voice without leaving the game.

| Feature | What it does |
| --- | --- |
| NPC & Story Translation | NPC dialogue appears in real time on a dedicated overlay. AI engines can use CatBridge's 273-character persona dictionary to keep character tone more consistent. |
| Two-Way Chat Translation | Guild, Map, Team, Say, Whisper, Party, and Squad messages are translated from game data. Type in your language, choose a target language, then copy it or send it instantly. |
| OCR Screen Translation | Drag over objectives, skills, achievements, dialogue choices, and other non-chat screen text. OCR is fast and recognition is strong. |
| Discord Voice Translation | Capture the Discord voice session, translate speech, and show captions in the language you choose. Lock the caption window for click-through play. |
| Mobility Tech | Replace or overlay the GW2 cursor, customize shape and color, and share cursor presets with a code. |
| Combat Tech | With AxiBridge, WvW fights can produce quick chat reports and detailed combat windows inside the game. |
| API & Engine Setup | Start free with M, B, C, P, or Google. Add the AI engine you prefer when you want stronger translation. |

## How It Works

CatBridge is a standalone app that receives game data through ArcDPS.

```text
Guild Wars 2 -> ArcDPS -> CatBridge
```

- **ArcDPS** loads the CatBridge plugin with the game client.
- **arcdps_catbridge.dll** reads the game data CatBridge needs and passes it to the app.
- **CatBridge** handles translation, overlay rendering, and AI features.

## Installation

### 1. Install ArcDPS and download CatBridge

1. Fully close Guild Wars 2.
2. If you do not use an addon manager, download ArcDPS's [`d3d11.dll`](https://www.deltaconnected.com/arcdps/x64/) and place it next to `Gw2-64.exe` in the main Guild Wars 2 folder.
3. If you use Nexus or another addon manager, install ArcDPS through that manager instead. In this setup, ArcDPS is commonly loaded as `arcdps.dll` from a folder under `Guild Wars 2\addons`.
4. Download the latest [CatBridge release](https://github.com/motionsilse/CatBridge/releases).
5. Extract the CatBridge ZIP and keep the app files together.

### 2. Put the files in the right places

| File | Purpose | Location |
| --- | --- | --- |
| `CatBridge.exe` | Main application | Keep it with `CatBridgeAudio.dll`, `WebRtcVad.dll`, and `catbridge_mouse.dll`, usually in the Guild Wars 2 folder. |
| `arcdps_catbridge.dll` | Reads game data and passes it to CatBridge | The folder where ArcDPS is actually running. |

With a standard manual ArcDPS installation, put `arcdps_catbridge.dll` next to `Gw2-64.exe` and `d3d11.dll`.

If you use Nexus or another addon manager, ArcDPS may be in a subfolder instead of next to `Gw2-64.exe`. Do not guess from the visible game folder:

1. Start Guild Wars 2 and open ArcDPS with **Alt + Shift + T**.
2. Open the last **About / Info** tab.
3. Use the folder path shown at the top of that tab as the install location for `arcdps_catbridge.dll`.

### 3. Restart and verify

1. Fully close Guild Wars 2, then start it again.
2. Open the ArcDPS **About / Info** tab and confirm ArcDPS is current and `arcdps_catbridge.dll` is loaded.
3. Run `CatBridge.exe`.

### Runtime requirements

- Use **Windowed Fullscreen** or **Windowed** display mode. Exclusive Fullscreen hides the overlay.
- ArcDPS must be running normally.

### If the overlay opens but nothing is translated

`arcdps_catbridge.dll` is usually in the wrong folder. Check the ArcDPS **About / Info** tab again and move the DLL to the folder shown there.

Party or squad chat is designed to resume after reconnecting, but in some cases you may still need to leave and rejoin the group.

For screenshots, detailed file placement, and more troubleshooting, see the [full installation guide](https://catbridge.guildwar.win/install/).

## Notes

CatBridge is not affiliated with, endorsed by, or approved by ArcDPS or AxiBridge.

CatBridge is an unofficial fan-made tool and is not affiliated with, endorsed by, or approved by ArenaNet or NCSOFT.
