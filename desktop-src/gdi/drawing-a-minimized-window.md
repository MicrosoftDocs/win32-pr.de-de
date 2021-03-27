---
description: Sie können Ihre eigenen minimierten Fenster zeichnen, damit Sie nicht vom System für Sie gezeichnet werden.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Zeichnen eines minimierten Fensters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393561"
---
# <a name="drawing-a-minimized-window"></a>Zeichnen eines minimierten Fensters

Sie können Ihre eigenen minimierten Fenster zeichnen, damit Sie nicht vom System für Sie gezeichnet werden. Die meisten Anwendungen definieren ein Klassen Symbol, wenn die Fenster Klasse für das Fenster registriert wird, und das System zeichnet das Symbol, wenn das Fenster minimiert wird. Wenn Sie das Klassen Symbol jedoch auf **null** festlegen, sendet das System immer dann eine [**WM \_ Paint**](wm-paint.md) -Meldung an die Fenster Prozedur, wenn das Fenster minimiert wird, sodass die Fenster Prozedur im minimierten Fenster gezeichnet werden kann.

Im folgenden Beispiel zeichnet die Fenster Prozedur einen Stern im minimierten Fenster. [**Die-**](/windows/win32/api/winuser/nf-winuser-isiconic) Prozedur bestimmt, wann das Fenster minimiert wird. Dadurch wird sichergestellt, dass der Stern nur gezeichnet wird, wenn das Fenster minimiert wird.


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



Sie legen das Klassen Symbol auf **null** fest, indem Sie den **HICON** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur auf **null** festlegen, bevor Sie die [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion für die Fenster Klasse aufrufen.

 

 
