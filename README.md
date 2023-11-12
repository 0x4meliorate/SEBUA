# SEBUA

<p align="center">
  <img src="https://github.com/0x4meliorate/SEBUA/raw/main/pictures/SEBUA.gif" alt="SEBUA custom image"/>
</p>

> **Created by [myself](https://github.com/0x4meliorate) and [MalwareMonster](https://github.com/malwaremonster).**
>
> :warning: **Warning**: Only use this software according to your current legislation. Misuse of this software can raise legal and ethical issues which I don't support nor can be held responsible for.

## Description

**SEBUA** is described as a '*Social Engineering Browser Update Attack*'. This attack requires user interaction and is highly deceiving.

### How it Works

- **Browser Detection**: SEBUA detects the browser type (Chrome, Firefox, or Edge).
- **Data Injection**: Uses `document.write` in JavaScript to inject data into the webpage.
- **UI Deception**: Displays an overlay mimicking the official browser download page.
- **Fake Update Prompt**: Demands an update to view content, triggering a download when the 'Update' button is clicked.
- **Post-Download Behavior**: Sets a key in the browser's localStorage to prevent overlay reappearance after the binary execution.
- **End Result**: Ideally leads to a beacon after the binary execution.

## Examples

| Chrome overlay | Firefox overlay | Edge overlay |
| :------------: | :-------------: | :----------: |
| ![Chrome](https://github.com/0x4meliorate/SEBUA/blob/main/pictures/Chrome.gif) | ![Firefox](https://github.com/0x4meliorate/SEBUA/blob/main/pictures/Firefox.gif) | ![Edge](https://github.com/0x4meliorate/SEBUA/blob/main/pictures/Edge.gif) |

## Additional Information

The primary component is the `payload.js` file. To create this payload:

1. Use `document.write` with obfuscated HTML in `payload.js`.
2. Employ [html-obfuscator](https://github.com/BinBashBanana/html-obfuscator) for obfuscation and de-obfuscation.

## Credits & Resources

- [BinBashBanana](https://github.com/BinBashBanana) for the **html-obfuscator** tool.
- [Browser Detection](https://stackoverflow.com/questions/9847580/how-to-detect-safari-chrome-ie-firefox-and-opera-browsers) - Useful for detecting browser types.
- [MalwareBytes](https://www.malwarebytes.com/blog/threat-intelligence/2023/07/socgholish-copycat-delivers-netsupport-rat) - Article on FakeSG and NetSupport RAT, the inspiration behind this project.
