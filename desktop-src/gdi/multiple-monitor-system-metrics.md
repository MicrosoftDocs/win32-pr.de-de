---
description: Die GetSystemMetrics-Funktion gibt Werte für den primären Monitor zurück, mit Ausnahme von SM \_ cxmaxtrack und SM \_ cymaxtrack, die auf den gesamten Desktop verweisen.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Mehrere Monitor Systemmetriken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f4da5c687df28817105e1ec3876ffd1ab5649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130756"
---
# <a name="multiple-monitor-system-metrics"></a>Mehrere Monitor Systemmetriken

Die [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion gibt Werte für den primären Monitor zurück, mit Ausnahme von SM \_ cxmaxtrack und SM \_ cymaxtrack, die auf den gesamten Desktop verweisen. Die folgenden Metriken sind für alle Gerätetreiber identisch: SM \_ cxcursor, SM \_ cycursor, SM \_ cxicon, smcyicon. Die folgenden Anzeigefunktionen sind für alle Monitore identisch: logpixelsx, logpixelsy, destophorzres, desktopvertres.

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) verfügt auch über Konstanten, die nur auf ein System mit mehreren Monitoren verweisen. SM \_ xvirtualscreen und SM \_ yvirtualscreen identifizieren die linke obere Ecke des virtuellen Bildschirms. SM \_ cxvirtualscreen und SM \_ cyvirtualscreen sind die vertikalen und horizontalen Messungen des virtuellen Bildschirms. SM \_ cmonitors ist die Anzahl der Monitore, die an den Desktop angeschlossen sind, und SM \_ samedisplayformat gibt an, ob alle Monitore auf dem Desktop das gleiche Farb Format aufweisen.

Verwenden Sie zum Anzeigen von Informationen zu einem einzelnen Bildschirm oder zu allen Anzeige Monitoren auf einem Desktop "enumdisplaymonitors". Das Rechteck des Desktop Fensters, das von [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) oder [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) zurückgegeben wird, entspricht immer dem Rechteck des primären Monitors, um die Kompatibilität mit vorhandenen Anwendungen zu erhalten. Folglich ist das Ergebnis von


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



wird wie folgt lauten:


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



Um den Arbeitsbereich eines Monitors zu ändern, wenden Sie [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) mit SPI \_ setworkarea und *pvParam* auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur an, die auf dem gewünschten Monitor basiert. Wenn *pvParam* den Wert **null** hat, wird der Arbeitsbereich des primären Monitors geändert. Die Verwendung \_ von SPI getworkarea gibt immer den Arbeitsbereich des primären Monitors zurück. Zum Abrufen des Arbeitsbereichs eines Monitors, der nicht der primäre Monitor ist, müssen Sie [**getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)aufrufen.

 

 
