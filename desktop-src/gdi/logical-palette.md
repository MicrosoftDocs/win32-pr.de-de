---
description: Eine logische Palette ist eine Farbpalette, die von einer Anwendung erstellt und einem bestimmten Gerätekontext zugeordnet wird.
ms.assetid: 7cc86771-237d-4539-8f48-2474edb764a4
title: Logische Palette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597e049c4320ff3ac30099e767c35a3438237904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978568"
---
# <a name="logical-palette"></a>Logische Palette

Eine *logische Palette* ist eine Farbpalette, die von einer Anwendung erstellt und einem bestimmten Gerätekontext zugeordnet wird. Mit logischen Paletten können Anwendungen Farben definieren und verwenden, die Ihren speziellen Anforderungen entsprechen. Anwendungen können beliebig viele logische Paletten erstellen, die Sie für separate Geräte Kontexte verwenden oder zwischen Ihnen für einen einzelnen Gerätekontext wechseln. Die maximale Anzahl von Paletten, die eine Anwendung erstellen kann, hängt von den Ressourcen des Systems ab.

Eine Anwendung erstellt eine logische Palette mithilfe der [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) -Funktion. Die Anwendung füllt eine [**LOGPALETTE**](/windows/win32/api/wingdi/ns-wingdi-logpalette) -Struktur, die die Anzahl der Einträge und die Farbwerte für jeden Eintrag angibt, und die Anwendung übergibt dann die Struktur an **CreatePalette**. Die-Funktion gibt ein Palettenhandle zurück, das die Anwendung in allen nachfolgenden Vorgängen verwendet, um die Palette zu identifizieren. Um Farben in der logischen Palette zu verwenden, wählt die Anwendung die Palette mithilfe der [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) -Funktion in einen Gerätekontext aus und erkennt dann die Palette mithilfe der [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) -Funktion. Die Farben in der Palette sind verfügbar, sobald die logische Palette realisiert wird.

Eine Anwendung sollte die Größe der logischen Paletten auf genau genug Einträge beschränken, um die benötigten Farben darzustellen. Anwendungen können keine logischen Paletten erstellen, die größer als die maximale Palettengröße sind, einem geräteabhängigen Wert. Anwendungen können die maximale Größe abrufen, indem Sie die [**getde vicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion verwenden, um den SIZEPALETTE-Wert abzurufen.

Obwohl eine Anwendung beliebige Farbwerte für einen bestimmten Eintrag in einer logischen Palette angeben kann, können nicht alle Farben vom angegebenen Gerät generiert werden. Das System bietet keine Möglichkeit, herauszufinden, welche Farben unterstützt werden, aber die Anwendung kann die Gesamtzahl dieser Farben ermitteln, indem die Farbauflösung des Geräts abgerufen wird. Die in Farbbits pro Pixel angegebene Farbauflösung ist gleich dem colorres-Wert, der von der [**getde vicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion zurückgegeben wird. Ein Gerät mit einer Farbauflösung von 18 hat 262.144 mögliche Farben. Wenn eine Anwendung eine nicht unterstützte Farbe anfordert, wählt das System eine entsprechende Näherung aus.

Nachdem eine logische Palette erstellt wurde, kann eine Anwendung die Farben in der Palette mithilfe der [**setpaletteentries**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries) -Funktion ändern. Wenn die logische Palette ausgewählt und erkannt wurde, wirkt sich das Ändern der Palette nicht sofort auf die angezeigten Farben aus. Die Anwendung muss die [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) -Funktion und die [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) -Funktion verwenden, um die Farben zu aktualisieren. In einigen Fällen muss die Anwendung möglicherweise die Auswahl der logischen Palette deaktivieren, Sie nicht erkennen, auswählen und erkennen, um sicherzustellen, dass die Farben genau wie angefordert aktualisiert werden. Wenn eine Anwendung eine logische Palette in mehr als einen Gerätekontext auswählt, wirken sich die Änderungen an der logischen Palette auf alle Geräte Kontexte aus, für die Sie ausgewählt ist.

Eine Anwendung kann die Anzahl von Einträgen in einer logischen Palette mithilfe der [**ResizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette) -Funktion ändern. Wenn die Größe der Anwendung verringert wird, werden die verbleibenden Einträge unverändert. Wenn die Anwendung die Größe erweitert, legt das System die Farbe für jeden neuen Eintrag auf schwarz (0, 0, 0) und das-Flag auf 0 (null) fest.

Eine Anwendung kann die Farb-und Flagwerte für Einträge in einer gegebenen logischen Palette mithilfe der [**GetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries) -Funktion abrufen. Eine Anwendung kann den Index für den Eintrag in einer gegebenen logischen Palette abrufen, der mit einem angegebenen Farbwert am ehesten mit der [**getnearestpaletteindex**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex) -Funktion übereinstimmt.

Wenn eine Anwendung keine logische Palette mehr benötigt, kann Sie mithilfe der [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) -Funktion gelöscht werden. Die Anwendung muss sicherstellen, dass die logische Palette nicht mehr in einem Gerätekontext ausgewählt ist, bevor die Palette gelöscht wird.

 

 



