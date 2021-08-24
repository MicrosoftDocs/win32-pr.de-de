---
description: Sie können Ihre eigenen minimierten Fenster zeichnen, anstatt sie vom System zeichnen zu lassen.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Zeichnen eines minimierten Fensters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ca955d3ff9f17b7f01e504b9e60c15200eb2b8191a5b4dba0e622956567f98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119360630"
---
# <a name="drawing-a-minimized-window"></a>Zeichnen eines minimierten Fensters

Sie können Ihre eigenen minimierten Fenster zeichnen, anstatt sie vom System zeichnen zu lassen. Die meisten Anwendungen definieren beim Registrieren der Fensterklasse für das Fenster ein Klassensymbol, und das System zeichnet das Symbol, wenn das Fenster minimiert wird. Wenn Sie das Klassensymbol jedoch auf **NULL** festlegen, sendet das System immer dann eine [**WM \_ PAINT-Nachricht**](wm-paint.md) an Ihre Fensterprozedur, wenn das Fenster minimiert wird, sodass die Fensterprozedur im minimierten Fenster zeichnen kann.

Im folgenden Beispiel zeichnet die Fensterprozedur einen Stern im minimierten Fenster. Die Prozedur verwendet die [**IsIconic-Funktion,**](/windows/win32/api/winuser/nf-winuser-isiconic) um zu bestimmen, wann das Fenster minimiert ist. Dadurch wird sichergestellt, dass der Stern nur gezeichnet wird, wenn das Fenster minimiert wird.


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



Sie legen das Klassensymbol auf **NULL** fest, indem Sie den **hIcon-Member** der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) auf **NULL** festlegen, bevor Sie die [**RegisterClass-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassa) für die Fensterklasse aufrufen.

 

 
