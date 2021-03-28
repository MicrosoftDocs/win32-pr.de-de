---
description: Um auf eine WM-Zeichnungs Nachricht zu reagieren \_ , verwenden Sie Code wie den folgenden.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Zeichnen auf einem Domänen Controller, der mehrere anzeigen umfasst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5b1b85c8aab20b7ef2415c1d67188ecab7728c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528310"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a><span data-ttu-id="08eb6-103">Zeichnen auf einem Domänen Controller, der mehrere anzeigen umfasst</span><span class="sxs-lookup"><span data-stu-id="08eb6-103">Painting on a DC That Spans Multiple Displays</span></span>

<span data-ttu-id="08eb6-104">Um auf eine **WM- \_** Zeichnungs Nachricht zu reagieren, verwenden Sie Code wie den folgenden.</span><span class="sxs-lookup"><span data-stu-id="08eb6-104">To respond to a **WM\_PAINT** message, use code like the following.</span></span>


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



<span data-ttu-id="08eb6-105">Um die obere Hälfte eines Fensters zu zeichnen, verwenden Sie Code wie den folgenden.</span><span class="sxs-lookup"><span data-stu-id="08eb6-105">To paint the top half of a window, use code like the following.</span></span>


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



<span data-ttu-id="08eb6-106">Um den gesamten virtuellen Bildschirm für jeden Monitor optimal zu zeichnen, verwenden Sie Code wie den folgenden.</span><span class="sxs-lookup"><span data-stu-id="08eb6-106">To paint the entire virtual screen optimally for each monitor, use code like the following.</span></span>


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



