---
description: Mit den Funktionen BeginPaint und endpaint können Sie die Zeichnung im Client Bereich vorbereiten und vervollständigen.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Zeichnen im Client Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e14c8492a11a7ad9764416b2453cea3264fbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863652"
---
# <a name="drawing-in-the-client-area"></a>Zeichnen im Client Bereich

Mit den Funktionen [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) und [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) können Sie die Zeichnung im Client Bereich vorbereiten und vervollständigen. **BeginPaint** gibt ein Handle für den Anzeigegeräte Kontext zurück, der zum Zeichnen im Client Bereich verwendet wird. **Endpaint** beendet die Zeichnungs Anforderung und gibt den Gerätekontext frei.

Im folgenden Beispiel schreibt die Fenster Prozedur die Meldung "Hello, Windows!" im Client Bereich. Um sicherzustellen, dass die Zeichenfolge bei der ersten Erstellung des Fensters sichtbar ist, ruft die [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) sofort nach dem Erstellen und Anzeigen des Fensters auf. Dies bewirkt, dass eine [**WM- \_ Paint**](wm-paint.md) -Meldung direkt an die Fenster Prozedur gesendet wird.


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



 

 
