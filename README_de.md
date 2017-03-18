[![License](https://img.shields.io/badge/license-Public%20Domain-blue.svg)](https://github.com/tekezo/Karabiner-Elements/blob/master/LICENSE.md)

# Karabiner-Elements-Neo

Karabiner-Elements-Neo implementiert die Ebenen 4 und 6 der
[Tastaturbelegung *Neo*](http://neo-layout.org/) für macOS Sierra.
Grundlage ist [takahasix' fork](https://github.com/takahasix/Karabiner-Elements)
von [Karabiner-Elements](https://github.com/tekezo/Karabiner-Elements), einer
eingeschränkten Reimplementierung von [Karabiner](https://github.com/tekezo/Karabiner)
für macOS Sierra.

## Status des Projekts

Beta – sollten Fehler auftreten oder Unklarheiten bzgl. der Installation
bestehen, mache bitte [ein Github Issue](https://github.com/jgosmann/Karabiner-Elements-Neo/issues)
auf (auf Englisch oder Deutsch).

## Bekannte Probleme

* Caps lock (aktiviert durch Drücken beider Shift-Tasten zur gleichen Zeit)
  funktioniert unter Umständen nicht. Dies ist ein Problem vom ursprünglichen
  Karabiner-Elemennts (tekezo/Karabiner-Elements#467). Für einige Nutzer lässt
  sich das Problem beheben, in dem man den `karabiner_grabber` process beendet.

## Installation

Karabiner-Elements-Neo steht bisher noch nicht als fertiges, installierbares
Paket zur Verfügung (denn dazu ist eine kommerzielle Apple Developer Lizenz
nötig). Stattdessen muss man die Software selbst bauen.

[Im Wiki findet sich hierzu eine detaillierte Anleitung.](https://github.com/jgosmann/Karabiner-Elements-Neo/wiki/Karabiner-Elements-Neo-selbst-bauen)

Nach dem Bauen des Pakets folgt die eigentliche Installation und Konfiguration:

1. Öffne die DMG-Datei und folge den Anweisungen des darin enthaltenen Installers.
2. Öffne Karabiner-Elements and füge unter „Simple Modifications“ folgende Einträge hinzu:
   * `backslash (\)` zu `right_option` (bei manchen externen Tastaturen kann es
     nötig sein `non_us_backslash` statt `backslash (\)` um zu belegen)
   * `caps_lock` zu `right_option`
   * ``grave_accent_and_tilde (`)`` zu `right_command`
   * `right_option` zu `left_command`
3. Installiere das Neo-Tastaturlayout (sofern noch nicht geschehen).
   Folge dazu der [Anleitung im Neo-Wiki](https://wiki.neo-layout.org/wiki/Neo%20auf%20dem%20Apple%20Macintosh%20einrichten),
   die hier in Kurzform wiedergegeben wird:
   * Lade entweder [die offizielle Layout-Datei](http://wiki.neo-layout.org/browser/mac_osx/neo.keylayout?format=raw)
     oder [@jgosmann's Variante](https://github.com/jgosmann/neo2-layout-osx)
     (mit verbessertem Capslock-Verhalten) herunter.
   * Platziere diese Datei entweder im Ordner `~/Library/Keyboard Layouts`
     oder `/Library/Keyboard Layouts` (letzteres stellt das Layout allen
     Nutzer-Accounts zur Verfügung).
4. Wähle in den Systemeinstellungen (unter „Tastatur → Eingabequellen“) das
   Neo-Layout („Deutsch (Neo 2)“) aus.
