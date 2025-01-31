# <img src="./phi.svg" width="32" height="32"> Phi (/faɪ/)

The ultimate vertical experience theme for Vivaldi, made with attention to details.

| ![](./screenshot1.webp) | ![](./screenshot2.webp) |
| ----------------------- | ----------------------- |
| ![](./screenshot3.webp) | ![](./screenshot4.webp) |
| ![](./screenshot5.webp) | ![](./screenshot6.webp) |

## :gear: Installation

1. Create a folder to download the theme into ;
2. Download the theme by right-clicking [here](https://git.kaki87.net/KaKi87/phi-for-vivaldi/raw/branch/master/phi.css) then "Save Link As..." to the folder created in step 1 ;
3. Go to `vivaldi:experiments` and check "Allow CSS modifications" ;
4. Open Vivaldi settings ;
   - Under "General" ➔ "Startup" ➔ "Default Browser", uncheck "Check on Startup" ;
   - Under "Appearance" ➔ "Window Appearance", check "Use Native Window" ;
   - Under "Appearance" ➔ "Window Appearance" ➔ "Status Bar", select "Hide Status Bar" ;
   - Under "Appearance" ➔ "Custom UI Modifications", open the folder created in step 1 ;
   - Under "Tabs" ➔ "Tabs" ➔ "Tab Bar Position", select "Left" or "Right" ;
   - Under "Tabs" ➔ "Tab Display" ➔ "Tab Options", uncheck "Show Popup Thumbnails" ;
   - Under "Tabs" ➔ "Tab Features" ➔ "Tab Stacking", select "Compact" ;
   - Under "Panel" ➔ "Panels" ➔ "Panel Options", check "Floating Panel" ;
5. Quit and relaunch Vivaldi ;
6. Start tweaking the UI ;
   - Right-click in the blank above the URL bar then "Customize Toolbar..." ;
   - Right-click the space items then "Remove from Toolbar" : left to the "Back" button, below the URL bar, below the panel buttons at the bottom ;
   - Then add, move and remove whatever you want, before clicking "Done" ;
7. Subscribe to Theo.

##  :hammer_and_wrench: Customization

While the theme aims to be compatible with as many native customization features as possible (especially sidebar position, side panel position & width, official themes, etc.), some had to be moved (e.g. sidebar width), but more were also added, these are located in the file you downloaded, above the source code :

| Name                                     | Description                                                  | Value(s)                                  | Default |
| ---------------------------------------- | ------------------------------------------------------------ | ----------------------------------------- | ------- |
| `sidebar-width`                          | Amount of horizontal space for the area containing the whole UI.<sup>(1)</sup> | Any number (in pixels)                    | `210`   |
| `is-phi-menu-icon`                       | Whether to show Phi's logo in place of Vivaldi's as menu button. | `1` = enable<br />`0` = disable           | `1`     |
| `toolbar-column-count`                   | Number of toolbar buttons per row above the URL bar.         | Any quantity                              | `5`     |
| `address-bar-focused-width-increase`     | Enlarge the URL bar over the page content when focused.      | Any number (in pixels)<br />`0` = disable | `200`   |
| `is-address-bar-focused-height-increase` | Whether to enlarge the URL bar over the extensions row below it when focused. | `1` = enable<br />`2` = disable           | `1`     |
| `address-bar-font-size-decrease`         | Lower the character size of the URL to see more of it.       | Any number (in pixels)<br />`0` = disable | `1`     |
| `is-address-bar-unfocused-hide-icons`    | Whether to hide icons<sup>(2)</sup> in the URL bar when not focused to see more of the URL. | `1` = enable<br />`0` = disable           | `1`     |
| `is-address-bar-focused-hide-icons`      | Whether to hide icons<sup>(2)</sup> in the URL bar when focused to see more of the URL. | `1` = enable<br />`0` = disable           | `0`     |
| `pinned-column-count`                    | Number of pinned tabs per row.                               | Any quantity                              | `4`     |

<sup>(1)</sup> Unfortunately, the sidebar cannot be resized by drag-and-drop.<br>
<sup>(2)</sup> With the exception of (in)valid HTTP(S), obfuscated domain name, and loading indicators.

Applying modifications require restarting Vivaldi.

##  :handshake: Support

- [Issues](https://git.kaki87.net/KaKi87/phi-for-vivaldi/issues)
- [Discord](https://discord.gg/pdgQE6juqM)
- [Reddit](https://old.reddit.com/r/vivaldibrowser/comments/1ieyt5a/)

## 🛜 Why "Phi" ?

Phi (φ) is a greek letter, used (among other things) to designate angles, like (for example) [sextant](https://en.wikipedia.org/wiki/Sextant) (<a href="https://en.wikipedia.org/wiki/Arc_(web_browser)" target="_blank"><img src="./arc.svg" width="32" height="32"></a>) & [compass](https://en.wikipedia.org/wiki/Compass) (<a href="https://en.wikipedia.org/wiki/Safari_(web_browser)" target="_blank"><img src="./safari.svg" width="32" height="32"></a>) measurements for *navigation*.

## :link: Related projects

- [ImMainTheme/ArchyVivaldi](https://github.com/ImMainTheme/ArchyVivaldi)
- [tovifun/VivalArc](https://github.com/tovifun/VivalArc)
- [(Address Bar + Title Bar + Status Bar) = Docked to side | Vivaldi Forum](https://forum.vivaldi.net/topic/80588/address-bar-title-bar-status-bar-docked-to-side)

## :technologist: Development notes

Guide : [Customizing Vivaldi’s UI with CSS mods - gabevilela.vivaldi.net](https://gabevilela.vivaldi.net/2020/12/26/guide-customizing-vivaldis-ui-with-css-mods/)

DevTools URL : `vivaldi://inspect/#apps`

DOM structure :

```
#browser.linux.win.mac.minimal-ui.fullscreen.tabs-left.tabs-right
├─ [aria-label="Address"]
│  ├─ .vivaldi
│  ├─ .button-toolbar
│  ├─ .UrlBar-AddressField
│  └─ .toolbar-extensions
├─ [aria-label="Panels"]
│  └─ .button-toolbar.button-toolbar-webpanel
├─ .panel-group
├─ [name="WorkspaceButton"]
├─ #tabs-container
│  └─ .tab-strip
│     ├─ .tab-position.is-pinned
│     │  └─ .tab-wrapper.active.group
│     │     ├─ .tab.pinned.active.tab-group
│     │     │  └─ .tab-header
│     │     │     ├─ .favicon
│     │     │     ├─ .title
│     │     │     └─ .close
│     │     └─ .tab-group-indicator
│     │        └── .tab-indicator.active
│     ├─ .separator
│     └─ .newtab
└─ #webview-container
```

---

© 2025 — KaKi87<br>
Released under the [MIT license](https://opensource.org/license/mit).