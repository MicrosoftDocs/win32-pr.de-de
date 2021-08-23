---
description: Änderungen an der Systempalette für das Anzeigegerät können drastische und manchmal unerwünschte Auswirkungen auf die Farben haben, die in Fenstern auf dem Desktop verwendet werden.
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: Palettenmeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a82c5ae2727e9f687f5f7fb628279b7832e896991f703225beec075a6630133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558440"
---
# <a name="palette-messages"></a>Palettenmeldungen

Änderungen an der Systempalette für das Anzeigegerät können drastische und manchmal unerwünschte Auswirkungen auf die Farben haben, die in Fenstern auf dem Desktop verwendet werden. Um die Auswirkungen dieser Änderungen zu minimieren, stellt das System eine Reihe von Nachrichten bereit, die Anwendungen bei der Verwaltung ihrer logischen Paletten unterstützen und gleichzeitig sicherstellen, dass die Farben im aktiven Fenster so nah wie möglich an den gewünschten Farben liegen.

Das System sendet eine [**WM \_ QUERYNEWPALETTE-Nachricht**](wm-querynewpalette.md) direkt vor dem Aktivieren des Fensters an ein Fenster der obersten Ebene oder überlappend. Diese Meldung gibt einer Anwendung die Möglichkeit, ihre logische Palette auszuwählen und zu realisieren, sodass sie die bestmögliche Zuordnung von Farben für ihre logische Palette erhält. Wenn die Anwendung die Nachricht empfängt, sollte sie die Funktionen [**SelectPalette,**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)und [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) verwenden, um die logische Palette auszuwählen und zu realisieren. Dies weist das System an, Farben in der Systempalette so zu aktualisieren, dass ihre Farben so vielen Farben in der logischen Palette wie möglich entsprechen.

Wenn eine Anwendung Änderungen an der Systempalette verursacht, weil die logische Palette erkannt wird, sendet das System eine [**WM \_ PALETTECHANGED-Meldung**](wm-palettechanged.md) an alle Fenster der obersten Ebene und überlappende Fenster. Diese Meldung gibt Anwendungen die Möglichkeit, die Farben in den Clientbereichen ihrer Fenster zu aktualisieren und dabei geänderte Farben durch Farben zu ersetzen, die den gewünschten Farben besser entsprechen. Eine Anwendung, die die **WM \_ PALETTECHANGED-Nachricht** empfängt, sollte [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) und [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) verwenden, um die logischen Paletten zurückzusetzen, die allen inaktiven Fenstern zugeordnet sind, und dann die Farben im Clientbereich für jedes inaktive Fenster mithilfe der [**UpdateColors-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) aktualisieren. Diese Technik garantiert nicht die größte Anzahl genauer Farb übereinstimmungen. Sie stellt jedoch sicher, dass Farben in der logischen Palette angemessenen Farben in der Systempalette zugeordnet werden.

> [!Note]  
> Um das Erstellen einer Endlosschleife zu vermeiden, sollte eine Anwendung nie die Palette für das Fenster erkennen, dessen Handle mit dem handle übereinstimmt, das im *wParam-Parameter* der [**WM \_ PALETTECHANGED-Nachricht**](wm-palettechanged.md) übergeben wird.

 

Die [**UpdateColors-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) aktualisiert in der Regel einen Clientbereich eines inaktiven Fensters schneller als das Neuzeichnen des Bereichs. Da **UpdateColors** jedoch eine Farbübersetzung basierend auf der Farbe jedes Pixels vor der Änderung der Systempalette durchführt, führt jeder Aufruf dieser Funktion zum Verlust einer bestimmten Farbgenauigkeit. Dies bedeutet, dass **UpdateColors** nicht zum Aktualisieren von Farben verwendet werden kann, wenn das Fenster aktiv wird. In solchen Fällen sollte die Anwendung den Clientbereich neu zeichnen.

Das System kann die [**WM \_ QUERYNEWPALETTE-Nachricht**](wm-querynewpalette.md) senden, wenn Änderungen an der logischen Palette vorgenommen werden. Außerdem kann das System die [**WM \_ PALETTEISCHANGING-Nachricht**](wm-paletteischanging.md) an alle Fenster der obersten Ebene und überlappende Fenster senden, wenn die Systempalette geändert wird.

 

 



