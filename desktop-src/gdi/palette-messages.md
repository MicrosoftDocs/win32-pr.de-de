---
description: Änderungen an der Systempalette für das Anzeigegerät können dramatische und mitunter unerwünschte Auswirkungen auf die in Windows auf dem Desktop verwendeten Farben haben.
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: Palettennachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f19a5458ec89d8d9a0524fd2ec383de740c0179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978449"
---
# <a name="palette-messages"></a>Palettennachrichten

Änderungen an der Systempalette für das Anzeigegerät können dramatische und mitunter unerwünschte Auswirkungen auf die in Windows auf dem Desktop verwendeten Farben haben. Um die Auswirkungen dieser Änderungen zu minimieren, stellt das System eine Reihe von Nachrichten bereit, mit deren Hilfe Anwendungen ihre logischen Paletten verwalten können und gleichzeitig sichergestellt werden, dass die Farben im aktiven Fenster so nah wie möglich an den gewünschten Farben sind.

Das System sendet eine [**WM \_ querynewpalette**](wm-querynewpalette.md) -Nachricht an ein überlappendes Fenster der obersten Ebene oder direkt vor dem Aktivieren des Fensters. Diese Meldung gibt einer Anwendung die Möglichkeit, die logische Palette auszuwählen und zu erkennen, sodass Sie die bestmögliche Zuordnung von Farben für die logische Palette erhält. Wenn die Anwendung die Nachricht empfängt, sollte Sie die Funktionen " [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette)", " [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)" und " [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) " verwenden, um die logische Palette auszuwählen und zu erkennen. Dadurch wird das System angewiesen, Farben in der Systempalette zu aktualisieren, sodass seine Farben so viele Farben in der logischen Palette wie möglich entsprechen.

Wenn eine Anwendung Änderungen an der Systempalette aufgrund der erkannten logischen Palette bewirkt, sendet das System eine [**WM \_ palettechanged**](wm-palettechanged.md) -Nachricht an alle Fenster der obersten Ebene und überlappende Fenster. Diese Meldung gibt Anwendungen die Möglichkeit, die Farben in den Client Bereichen ihrer Fenster zu aktualisieren und Farben zu ersetzen, die sich mit Farben geändert haben, die den gewünschten Farben genauer entsprechen. Eine Anwendung, die die **WM \_ palettechanged** -Nachricht empfängt, sollte [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) und [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) verwenden, um die logischen Paletten zurückzusetzen, die allen inaktiven Fenstern zugeordnet sind, und dann die Farben im Client Bereich für jedes inaktive Fenster mithilfe der [**updatecolors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) -Funktion zu aktualisieren. Diese Technik garantiert nicht die höchste Anzahl von exakten Farb Übereinstimmungen. Allerdings wird sichergestellt, dass die Farben in der logischen Palette den sinnvollen Farben in der Systempalette zugeordnet werden.

> [!Note]  
> Um zu vermeiden, dass eine Endlosschleife erstellt wird, sollte eine Anwendung niemals die Palette für das Fenster erkennen, dessen Handle mit dem Handle übereinstimmt, das im *wParam* -Parameter der [**WM \_ palettechanged**](wm-palettechanged.md) -Nachricht übergeben wird.

 

Die Funktion [**updatecolors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) aktualisiert in der Regel einen Client Bereich eines inaktiven Fensters schneller, als den Bereich neu zu zeichnen. Da **updatecolors** jedoch eine Farb Übersetzung basierend auf der Farbe jedes Pixels vor der Änderung der Systempalette durchführt, führt jeder Rückruf dieser Funktion zu einem Verlust der Farbgenauigkeit. Dies bedeutet, dass **updatecolors** nicht zum Aktualisieren von Farben verwendet werden können, wenn das Fenster aktiv wird. In solchen Fällen sollte die Anwendung den Client Bereich neu zeichnen.

Das System kann die [**WM- \_ Abfrage "querynewpalette**](wm-querynewpalette.md) " senden, wenn Änderungen an der logischen Palette vorgenommen werden. Außerdem kann das System die WM- [**\_ paletteischanging**](wm-paletteischanging.md) -Nachricht an alle Fenster der obersten Ebene und überlappende Fenster senden, wenn sich die Systempalette ändert.

 

 



