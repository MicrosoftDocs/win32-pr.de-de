---
description: Um auf eine WM \_ PAINT-Nachricht zu reagieren, verwenden Sie Code wie den folgenden.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Painting on a DC That Spans Multiple Displays
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550279d003c7d32fc97923ea6ebe4c95364773e514a69e4c66bdb4b100784384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759481"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>Painting on a DC That Spans Multiple Displays

Um auf eine **WM \_ PAINT-Nachricht** zu reagieren, verwenden Sie Code wie den folgenden.


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



Um die obere Hälfte eines Fensters zu zeichnen, verwenden Sie Code wie den folgenden.


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



Um den gesamten virtuellen Bildschirm für jeden Monitor optimal zu zeichnen, verwenden Sie Code wie den folgenden.


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



