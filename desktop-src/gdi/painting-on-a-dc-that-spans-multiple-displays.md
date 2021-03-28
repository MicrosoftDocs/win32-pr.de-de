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
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>Zeichnen auf einem Domänen Controller, der mehrere anzeigen umfasst

Um auf eine **WM- \_** Zeichnungs Nachricht zu reagieren, verwenden Sie Code wie den folgenden.


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



 

 



