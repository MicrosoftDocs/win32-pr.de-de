---
description: Normalerweise können die Systempaletteneinträge, die das System für statische Farben reserviert, nicht geändert werden.
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: Systempalette und statische Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffc555331ea7ad14675b4155a76d14cc61f3bef3fa7e92b331ad89449b97884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613380"
---
# <a name="system-palette-and-static-colors"></a>Systempalette und statische Farben

Normalerweise können die Systempaletteneinträge, die das System für statische Farben reserviert, nicht geändert werden. Eine Anwendung kann dieses Standardverhalten überschreiben, indem sie die [**SetSystemPaletteUse-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) verwendet, um die Anzahl statischer Farbeinträge zu reduzieren und dadurch die Anzahl der nicht verwendeten Systempaletteneinträge zu erhöhen. Da das Ändern der statischen Farben jedoch sofortige und drastische Auswirkungen auf alle Fenster auf der Anzeige haben kann, sollte eine Anwendung **SetSystemPaletteUse** nur aufrufen, wenn sie über ein maximiertes Fenster und den Eingabefokus verfügt.

Wenn eine Anwendung [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) mit dem SYSPAL \_ NOSTATIC-Wert aufruft, gibt das System alle bis auf zwei der reservierten Einträge frei, sodass diese Einträge neue Farbwerte erhalten, wenn die Anwendung anschließend ihre logische Palette erkennt. Die verbleibenden beiden statischen Farbeinträge bleiben reserviert und sind auf Weiß und Schwarz festgelegt. Eine Anwendung kann die reservierten Einträge wiederherstellen, indem **Sie SetSystemPaletteUse** mit dem SYSPAL \_ STATIC-Wert aufrufen. Die aktuelle Systempalettenverwendung kann mithilfe der [**GetSystemPaletteUse-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse) ermittelt werden.

Darüber hinaus muss die Anwendung nach dem Festlegen der Systempalettenverwendung auf SYSPAL \_ NOSTATIC sofort ihre logische Palette erkennen, die [**GetSysColor-Funktion**](/windows/win32/api/winuser/nf-winuser-getsyscolor) aufrufen, um die aktuellen Systemfarbeinstellungen zu speichern, die [**SetSysColors-Funktion**](/windows/win32/api/winuser/nf-winuser-setsyscolors) aufrufen, um die Systemfarben mithilfe von Schwarz und Weiß auf sinnvolle Werte festzulegen, und schließlich die [**\_ WM-SYSCOLORCHANGE-Nachricht**](wm-syscolorchange.md) an andere Fenster der obersten Ebene senden, damit sie mit den neuen Systemfarben neu gezeichnet werden können. Beim Festlegen von Systemfarben mit Schwarz und Weiß sollte die Anwendung sicherstellen, dass angrenzende oder überlappende Elemente wie Fensterrahmen und Rahmen auf Schwarz bzw. Weiß festgelegt sind.

Bevor die Anwendung den Eingabefokus verliert, ihr Fenster schließt oder beendet wird, muss sie [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) sofort mit dem SYSPAL \_ STATIC-Wert aufrufen, ihre logische Palette realisieren, die Systemfarben auf ihre vorherigen Werte wiederherstellen und die [**\_ WM-SYSCOLORCHANGE-Nachricht**](wm-syscolorchange.md) senden. Das System sendet eine [**WM \_ PAINT-Nachricht**](wm-paint.md) an ein beliebiges Fenster, das von einer Systemfarbänderung betroffen ist. Anwendungen mit Pinseln, die die vorhandenen Systemfarben verwenden, sollten diese Pinsel löschen und mit den neuen Systemfarben neu erstellen.

 

 
