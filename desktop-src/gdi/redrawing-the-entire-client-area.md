---
description: Sie können ihre Anwendung den gesamten Inhalt des Clientbereichs neu zeichnen lassen, wenn sich die Größe des Fensters ändert, indem Sie die CS \_ HREDRAW- und CS \_ VREDRAW-Stile für die Fensterklasse festlegen.
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: Neuzeichnen des gesamten Clientbereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3c438fe36160f27b1015daf7874e237035f927825199b93b3a508668f40bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759146"
---
# <a name="redrawing-the-entire-client-area"></a>Neuzeichnen des gesamten Clientbereichs

Sie können ihre Anwendung den gesamten Inhalt des Clientbereichs neu zeichnen lassen, wenn sich die Größe des Fensters ändert, indem Sie die CS \_ HREDRAW- und CS \_ VREDRAW-Stile für die Fensterklasse festlegen. Anwendungen, die die Größe der Zeichnung basierend auf der Größe des Fensters anpassen, verwenden diese Stile, um sicherzustellen, dass sie beim Zeichnen mit einem vollständig leeren Clientbereich beginnen.

Im folgenden Beispiel zeichnet die Fensterprozedur einen fünfzackigen Stern, der gut in den Clientbereich passt. Er verwendet einen allgemeinen Gerätekontext und muss bei jeder Verarbeitung der [**WM \_ PAINT-Nachricht**](wm-paint.md) den Zuordnungsmodus sowie Fenster- und Viewport-Erweiterungen festlegen.


```C++
LRESULT APIENTRY WndProc(HWMD hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
    RECT rc; 
    POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
    . 
    . 
    . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            GetClientRect(hwnd, &rc); 
            SetMapMode(hdc, MM_ANISOTROPIC); 
            SetWindowExtEx(hdc, 100, 100, NULL); 
            SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
            Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
        . 
        . 
        . 
} 
 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    WNDCLASS wc; 
 
    . 
    . 
    . 
 
        wc.style = CS_HREDRAW | CS_VREDRAW; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
 
    . 
    . 
    . 
 
        RegisterClass(&wc); 
 
    . 
    . 
    . 
 
    return msg.wParam; 
} 
```



 

 



