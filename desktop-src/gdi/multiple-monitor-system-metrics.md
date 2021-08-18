---
description: Die GetSystemMetrics-Funktion gibt Werte für den primären Monitor zurück, mit Ausnahme von SM \_ CXMAXTRACK und SM \_ CYMAXTRACK, die auf den gesamten Desktop verweisen.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Systemmetriken mit mehreren Monitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3143562116561bb220bc6f0b5ecfa4ad8f5103c3e4532cab639c4c2b37f59467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037708"
---
# <a name="multiple-monitor-system-metrics"></a>Systemmetriken mit mehreren Monitoren

Die [**GetSystemMetrics-Funktion**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) gibt Werte für den primären Monitor zurück, mit Ausnahme von SM \_ CXMAXTRACK und SM \_ CYMAXTRACK, die auf den gesamten Desktop verweisen. Die folgenden Metriken sind für alle Gerätetreiber identisch: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON. Die folgenden Anzeigefunktionen sind für alle Monitore identisch: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) verfügt auch über Konstanten, die nur auf ein System mit mehreren Monitoren verweisen. \_SMTOPUALSCREEN und SM \_ YVIRTUALSCREEN identifizieren die obere linke Ecke des virtuellen \_ Bildschirms, SM CXVIRTUALSCREEN und SM \_ CYVIRTUALSCREEN sind die vertikalen und horizontalen Messungen des virtuellen Bildschirms, SM \_ CMONITORS ist die Anzahl der monitoren, die an den Desktop angefügt sind, und SM \_ SAMEDISPLAYFORMAT gibt an, ob alle Monitore auf dem Desktop das gleiche Farbformat aufweisen.

Verwenden Sie EnumDisplayMonitors, um Informationen zu einem einzelnen Anzeigemonitor oder allen Anzeigemonitoren auf einem Desktop abzurufen. Das Rechteck des Desktopfensters, das von [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) oder [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) zurückgegeben wird, entspricht immer dem Rechteck des primären Monitors, um Kompatibilität mit vorhandenen Anwendungen zu gewährleisten. Daher das Ergebnis von


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



wird sein:


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



Um den Arbeitsbereich eines Monitors zu ändern, rufen [**Sie SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) mit SPI \_ SETWORKAREA und *pvParam* auf, die auf eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) zeigen, die sich auf dem gewünschten Monitor befindet. Wenn *pvParam* **NULL** ist, wird der Arbeitsbereich des primären Monitors geändert. Bei Verwendung von SPI \_ GETWORKAREA wird immer der Arbeitsbereich des primären Monitors zurückgegeben. Rufen [**Sie GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)auf, um den Arbeitsbereich eines anderen Monitors als des primären Monitors abzurufen.

 

 
