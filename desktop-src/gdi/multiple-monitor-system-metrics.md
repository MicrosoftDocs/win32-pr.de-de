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
# <a name="multiple-monitor-system-metrics"></a><span data-ttu-id="d2c75-103">Mehrere Monitor Systemmetriken</span><span class="sxs-lookup"><span data-stu-id="d2c75-103">Multiple Monitor System Metrics</span></span>

<span data-ttu-id="d2c75-104">Die [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion gibt Werte für den primären Monitor zurück, mit Ausnahme von SM \_ cxmaxtrack und SM \_ cymaxtrack, die auf den gesamten Desktop verweisen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-104">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function returns values for the primary monitor, except for SM\_CXMAXTRACK and SM\_CYMAXTRACK, which refer to the entire desktop.</span></span> <span data-ttu-id="d2c75-105">Die folgenden Metriken sind für alle Gerätetreiber identisch: SM \_ cxcursor, SM \_ cycursor, SM \_ cxicon, smcyicon.</span><span class="sxs-lookup"><span data-stu-id="d2c75-105">The following metrics are the same for all device drivers: SM\_CXCURSOR, SM\_CYCURSOR, SM\_CXICON, SMCYICON.</span></span> <span data-ttu-id="d2c75-106">Die folgenden Anzeigefunktionen sind für alle Monitore identisch: logpixelsx, logpixelsy, destophorzres, desktopvertres.</span><span class="sxs-lookup"><span data-stu-id="d2c75-106">The following display capabilities are the same for all monitors: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span></span>

<span data-ttu-id="d2c75-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) verfügt auch über Konstanten, die nur auf ein System mit mehreren Monitoren verweisen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) also has constants that refer only to a Multiple Monitor system.</span></span> <span data-ttu-id="d2c75-108">SM \_ xvirtualscreen und SM \_ yvirtualscreen identifizieren die linke obere Ecke des virtuellen Bildschirms. SM \_ cxvirtualscreen und SM \_ cyvirtualscreen sind die vertikalen und horizontalen Messungen des virtuellen Bildschirms. SM \_ cmonitors ist die Anzahl der Monitore, die an den Desktop angeschlossen sind, und SM \_ samedisplayformat gibt an, ob alle Monitore auf dem Desktop das gleiche Farb Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-108">SM\_XVIRTUALSCREEN and SM\_YVIRTUALSCREEN identify the upper-left corner of the virtual screen, SM\_CXVIRTUALSCREEN and SM\_CYVIRTUALSCREEN are the vertical and horizontal measurements of the virtual screen, SM\_CMONITORS is the number of monitors attached to the desktop, and SM\_SAMEDISPLAYFORMAT indicates whether all the monitors on the desktop have the same color format.</span></span>

<span data-ttu-id="d2c75-109">Verwenden Sie zum Anzeigen von Informationen zu einem einzelnen Bildschirm oder zu allen Anzeige Monitoren auf einem Desktop "enumdisplaymonitors".</span><span class="sxs-lookup"><span data-stu-id="d2c75-109">To get information about a single display monitor or all of the display monitors in a desktop, use EnumDisplayMonitors.</span></span> <span data-ttu-id="d2c75-110">Das Rechteck des Desktop Fensters, das von [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) oder [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) zurückgegeben wird, entspricht immer dem Rechteck des primären Monitors, um die Kompatibilität mit vorhandenen Anwendungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2c75-110">The rectangle of the desktop window returned by [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) or [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) is always equal to the rectangle of the primary monitor, for compatibility with existing applications.</span></span> <span data-ttu-id="d2c75-111">Folglich ist das Ergebnis von</span><span class="sxs-lookup"><span data-stu-id="d2c75-111">Thus, the result of</span></span>


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



<span data-ttu-id="d2c75-112">wird wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="d2c75-112">will be:</span></span>


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



<span data-ttu-id="d2c75-113">Um den Arbeitsbereich eines Monitors zu ändern, wenden Sie [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) mit SPI \_ setworkarea und *pvParam* auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur an, die auf dem gewünschten Monitor basiert.</span><span class="sxs-lookup"><span data-stu-id="d2c75-113">To change the work area of a monitor, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETWORKAREA and *pvParam* pointing to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that is on the desired monitor.</span></span> <span data-ttu-id="d2c75-114">Wenn *pvParam* den Wert **null** hat, wird der Arbeitsbereich des primären Monitors geändert.</span><span class="sxs-lookup"><span data-stu-id="d2c75-114">If *pvParam* is **NULL**, the work area of the primary monitor is modified.</span></span> <span data-ttu-id="d2c75-115">Die Verwendung \_ von SPI getworkarea gibt immer den Arbeitsbereich des primären Monitors zurück.</span><span class="sxs-lookup"><span data-stu-id="d2c75-115">Using SPI\_GETWORKAREA always returns the work area of the primary monitor.</span></span> <span data-ttu-id="d2c75-116">Zum Abrufen des Arbeitsbereichs eines Monitors, der nicht der primäre Monitor ist, müssen Sie [**getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d2c75-116">To get the work area of a monitor other than the primary monitor, call [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span>

 

 
