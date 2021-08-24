---
description: Sie verwenden die Funktionen BeginPaint und EndPaint, um die Zeichnung im Clientbereich vorzubereiten und zu vervollständigen.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Zeichnen im Clientbereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d01331ae60a7814602f6c10c0d9109ae665da39aa140223e31ac03303048b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832020"
---
# <a name="drawing-in-the-client-area"></a>Zeichnen im Clientbereich

Sie verwenden die [**Funktionen BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) und [**EndPaint,**](/windows/desktop/api/Winuser/nf-winuser-endpaint) um die Zeichnung im Clientbereich vorzubereiten und zu vervollständigen. **BeginPaint gibt** ein Handle für den Anzeigegerätekontext zurück, der zum Zeichnen im Clientbereich verwendet wird. **EndPaint beendet** die Farbanforderung und gibt den Gerätekontext frei.

Im folgenden Beispiel schreibt die Fensterprozedur die Meldung "Hello, Windows!" im Clientbereich. Um sicherzustellen, dass die Zeichenfolge beim ersten Erstellen des Fensters sichtbar ist, ruft die [**WinMain-Funktion**](/windows/win32/api/winbase/nf-winbase-winmain) [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) unmittelbar nach dem Erstellen und Anzeigen des Fensters auf. Dies bewirkt, dass [**eine WM \_ PAINT-Nachricht**](wm-paint.md) sofort an die Fensterprozedur gesendet wird.


```C++
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
 
    switch (message) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            TextOut(hdc, 0, 0, "Hello, Windows!", 15); 
            EndPaint(hwnd, &ps); 
            return 0L; 

        // Process other messages.   
    } 
} 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    HWND hwnd; 
 
    hwnd = CreateWindowEx( 
        // parameters  
        ); 
 
    ShowWindow(hwnd, SW_SHOW); 
    UpdateWindow(hwnd); 
 
    return msg.wParam; 
} 
```



 

 
