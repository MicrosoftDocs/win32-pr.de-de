---
description: Normalerweise können die System Paletteneinträge, die das System für statische Farben reserviert, nicht geändert werden.
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: System Palette und statische Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537bdc87fecdd055334b83a56b0a53f9999be94c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979424"
---
# <a name="system-palette-and-static-colors"></a>System Palette und statische Farben

Normalerweise können die System Paletteneinträge, die das System für statische Farben reserviert, nicht geändert werden. Eine Anwendung kann dieses Standardverhalten überschreiben, indem Sie die [**setsystempaletteuse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) -Funktion verwendet, um die Anzahl der statischen Farbeinträge zu verringern und so die Anzahl der nicht verwendeten System Paletteneinträge zu erhöhen. Da das Ändern der statischen Farben jedoch eine unmittelbare und drastische Auswirkung auf alle Fenster auf der Anzeige haben kann, sollte eine Anwendung **setsystempaletteuse** nicht aufrufen, es sei denn, Sie verfügt über ein maximiertes Fenster und den Eingabefokus.

Wenn eine Anwendung [**setsystempaletteuse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) mit dem nostatic-Wert syspal aufruft \_ , gibt das System alle bis auf zwei reservierte Einträge frei, sodass diese Einträge neue Farbwerte empfangen können, wenn die Anwendung anschließend die logische Palette erkennt. Die verbleibenden zwei statischen Farbeinträge bleiben reserviert und sind auf weiß und schwarz festgelegt. Eine Anwendung kann die reservierten Einträge wiederherstellen, indem **setsystempaletteuse** mit dem statischen syspal-Wert aufgerufen wird \_ . Sie kann die aktuelle Systempalette mithilfe der [**getsystempaletteuse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse) -Funktion ermitteln.

Außerdem müssen Sie nach dem Festlegen der System palettenverwendung auf syspal \_ nostatic die Anwendung muss die logische Palette sofort erkennen, die [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) -Funktion aufrufen, um die aktuellen System Farbeinstellungen zu speichern. Sie muss die [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) -Funktion aufrufen, um die Systemfarben mithilfe von schwarz und weiß auf sinnvolle Werte festzulegen, und schließlich die [**WM- \_ syscolorchange**](wm-syscolorchange.md) -Nachricht an andere Fenster der obersten Ebene senden, damit Sie mit den neuen Wenn Sie Systemfarben mithilfe von schwarz und weiß festlegen, sollte die Anwendung sicherstellen, dass angrenzende oder überlappende Elemente, wie z. b. Fensterrahmen und Rahmen, auf Schwarz bzw. weiß festgelegt sind.

Bevor die Anwendung den Eingabefokus verliert, das Fenster schließt oder beendet, muss Sie sofort [**setsystempaletteuse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) mit dem statischen Wert "syspal" aufrufen \_ , die logische Palette erkennen, die Systemfarben auf die vorherigen Werte zurücksetzen und die [**" \_ syscolorchange**](wm-syscolorchange.md) "-Meldung "WM" senden. Das System sendet eine [**WM \_**](wm-paint.md) -Zeichnungs Meldung an jedes Fenster, das von einer System Farbänderung betroffen ist. Anwendungen mit Pinseln, die die vorhandenen Systemfarben verwenden, sollten diese Pinsel löschen und mithilfe der neuen Systemfarben neu erstellen.

 

 
