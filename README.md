<div align="center">
<pre>
██╗███████╗██████╗  ██████╗    ███████╗███████╗███████╗██████╗ ██████╗  █████╗  ██████╗██╗  ██╗    ██████╗  ██████╗ ████████╗
██║██╔════╝██╔══██╗██╔════╝    ██╔════╝██╔════╝██╔════╝██╔══██╗██╔══██╗██╔══██╗██╔════╝██║ ██╔╝    ██╔══██╗██╔═══██╗╚══██╔══╝
██║█████╗  ██████╔╝██║         █████╗  █████╗  █████╗  ██║  ██║██████╔╝███████║██║     █████╔╝     ██████╔╝██║   ██║   ██║   
██║██╔══╝  ██╔══██╗██║         ██╔══╝  ██╔══╝  ██╔══╝  ██║  ██║██╔══██╗██╔══██║██║     ██╔═██╗     ██╔══██╗██║   ██║   ██║   
██║██║     ██║  ██║╚██████╗    ██║     ███████╗███████╗██████╔╝██████╔╝██║  ██║╚██████╗██║  ██╗    ██████╔╝╚██████╔╝   ██║   
╚═╝╚═╝     ╚═╝  ╚═╝ ╚═════╝    ╚═╝     ╚══════╝╚══════╝╚═════╝ ╚═════╝ ╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝    ╚═════╝  ╚═════╝    ╚═╝   
                                                                                                                             
     IFRC Feedback Form Auto‑Filler (No Autre, 5s Delay)
</pre>
[![Version: 6.7](https://img.shields.io/badge/version-6.7-blue.svg)]
[![Tampermonkey Compatible](https://img.shields.io/badge/Tampermonkey-Compatible-green.svg)]
</div>

# IFRC Feedback Form Auto‑Filler

A Tampermonkey user script that fills the IFRC feedback form, selecting communes and village provided by the user, with a 5‑second delay between submissions (the delay is customized).

---

## Installation

1. **Install Tampermonkey** in your browser.
2. **Create a new script** and paste the entire metadata + code (see below) into the editor.
3. **Save** the script. It will run automatically on pages matching `https://ee.ifrc.org/x/5x6PxyDj`.

```js
// ==UserScript==
// @name         IFRC Feedback Form Auto-Filler (No Autre, 5s Delay)
// @namespace    http://tampermonkey.net/
// @version      6.7
// @description  Fills IFRC feedback form 50 times, only Ijoukak or Talat_N_Yaaqoub for commune, never picks Autre/Other for village, 5s delay
// @match        https://ee.ifrc.org/x/5x6PxyDj
// @grant        none
// ==/UserScript==

(function() {
    /* Your script code here... */
})();
```

---

## Usage

1. Navigate to the IFRC feedback form URL: `https://ee.ifrc.org/x/5x6PxyDj`.
2. The script will automatically fill in fields and prompt you with an alert after each submission (up to 50 times).
3. Review each auto‑filled form within the 5‑second delay if needed, then let it reload for the next try.

---

## Configuration

All configurable values are at the top of the script:

* **NomdeCollecteurdeDonnees**: your name as data collector.
* **languages**, **feedbackChannels**, **sexes**, etc.: arrays to randomize or fix choices.
* **allowedCommunes**: only these communes will be selected.
* **douarsByCommune**: maps each allowed commune to its list of douars.
* **allowedDates**: restricts which dates can be chosen.
* **maxTries** and **delay**: adjust number of submissions and delay between reloads.

---

## Development

1. Fork or clone this repository.
2. Update version in the metadata (`@version`).
3. Edit script logic or data arrays as needed.
4. Test in your browser with Tampermonkey.
5. Commit changes and push, then update the `@version` tag on the main copy.

---

## License

Distributed under the MIT License. See [LICENSE](./LICENSE) for details.

---

## Author

**Yasser BAOUZIL** – [GitHub](https://github.com/xxxxxxxx15339)
