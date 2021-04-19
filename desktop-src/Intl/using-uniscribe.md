---
description: Uniwriter bietet APIs, um Typografiefunktionen zu unterstützen und die Anzeige und Bearbeitung von internationalem Text zu unterstützen, einschließlich der komplexen Regeln von Nahen und ostasiatischen Skripts.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Verwenden von uniscri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369099"
---
# <a name="using-uniscribe"></a>Verwenden von uniscri

Uniwriter bietet APIs, um Typografiefunktionen zu unterstützen und die Anzeige und Bearbeitung von internationalem Text zu unterstützen, einschließlich der komplexen Regeln von Nahen und ostasiatischen Skripts. Uniwriter stellt Routinen auf niedriger Ebene für die Verarbeitung von vollständig formatiertem Text und einen einfachen scriptstring-API-Satz für unformatierten Text bereit.

Bei Verwendung von unischreiber müssen Anwendungen nur einen Sicherungs Speicher von Unicode-Zeichen Codes verwalten. Textlayoutanwendungen müssen keine andere Puffer-oder Mapping-Tabelle verwalten, um die Reihenfolge der Zeichen zu verfolgen. Jede Anwendung muss nur die Reihenfolge speichern und verwalten, in der die Zeichen vom Benutzer eingegeben werden. Dies ist dieselbe logische Reihenfolge wie durch Unicode definiert. Der Sicherungs Speicher ändert sich nie aufgrund von Layoutvorgängen. Uniscribehält einen Index von den neu bestellten Clustern an den ursprünglichen Zeichen Grenzen bei, die von der Anwendung weitergegeben wurden.

Die folgenden Themen werden in diesem Abschnitt behandelt.

**Strukturierung**

-   [Bestimmen, ob ein Skript eine Symbol Strukturierung erfordert](determining-if-a-script-requires-glyph-shaping.md)
-   [Verwenden von Strukturierungs Modulen](using-shaping-engines.md)

**Andere Verarbeitung**

-   [Zwischenspeichern](caching.md)
-   [Anzeigen von Text mit uniwriter](displaying-text-with-uniscribe.md)
-   [Verarbeiten komplexer Skripts](processing-complex-scripts.md)
-   [Verwenden eines Schriftart-Fallbacks](using-font-fallback.md)
-   [Verwenden der scriptstring-Funktionen](using-the-scriptstring-functions.md)

**Einfügemarke**

-   [Anzeigen des Caretzeichen in bidirektionalen Zeichen folgen](displaying-the-caret-in-bidirectional-strings.md)
-   [Verwalten der Platzierung von Caretzeichen und Treffer Tests](managing-caret-placement-and-hit-testing.md)
-   [Übersetzen des X-Offsets in der Einfügemarke](translating-mouse-hit-x-offset-to-caret-position.md)

**Wörter und Zeichen Cluster**

-   [Verwenden von Zeichen Clustern](using-character-clusters.md)
-   [Verwenden von Wort Break Points](using-word-break-points.md)
-   [Arbeiten mit Beziehungen zwischen Einfügepositionen, Ausrichtungspunkten und Clustern](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



