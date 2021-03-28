---
description: Eine Anwendung, die zahlreiche Zeichnungsvorgänge im Client Bereich des Fensters ausführt, muss einen privaten Anzeige Domänen Controller verwenden.
ms.assetid: 9c4ed127-a88f-4946-9d7c-f77899152c31
title: Abrufen eines privaten Anzeigegeräte Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed679ecadd694cd8781d0de8b4409fde15d22b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754361"
---
# <a name="obtaining-a-private-display-device-context"></a><span data-ttu-id="b16e0-103">Abrufen eines privaten Anzeigegeräte Kontexts</span><span class="sxs-lookup"><span data-stu-id="b16e0-103">Obtaining a Private Display Device Context</span></span>

<span data-ttu-id="b16e0-104">Eine Anwendung, die zahlreiche Zeichnungsvorgänge im Client Bereich des Fensters ausführt, muss einen privaten Anzeige Domänen Controller verwenden.</span><span class="sxs-lookup"><span data-stu-id="b16e0-104">An application performing numerous drawing operations in the client area of its window must use a private display DC.</span></span> <span data-ttu-id="b16e0-105">Um diese Art von DC zu erstellen, muss die Anwendung die **CS- \_ owndc** -Konstante für den Stilelement der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur angeben, wenn die Fenster Klasse registriert wird.</span><span class="sxs-lookup"><span data-stu-id="b16e0-105">To create this type of DC, the application must specify the **CS\_OWNDC** constant for the style member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when registering the window class.</span></span> <span data-ttu-id="b16e0-106">Nach dem Registrieren der Fenster Klasse erhält die Anwendung ein Handle, das einen privaten Anzeige-DC durch Aufrufen der [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b16e0-106">After registering the window class, the application obtains a handle identifying a private display DC by calling the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="b16e0-107">Im folgenden Beispiel wird gezeigt, wie ein privater Anzeige-DC erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b16e0-107">The following example shows how to create a private display DC.</span></span>


```C++
#include <windows.h>    // required for all Windows-based applications  
#include <stdio.h>      // C run-time header for i/o 
#include <string.h>     // C run-time header for strtok_s  
#include "dc.h"         // specific to this program  
 
// Function prototypes. 
 
BOOL InitApplication(HINSTANCE); 
long FAR PASCAL MainWndProc(HWND, UINT, UINT, LONG); 
 
// Global variables  
 
HINSTANCE hinst;       // handle to current instance  
HDC hdc;               // display device context handle  
 
BOOL InitApplication(HINSTANCE hinstance) 
{ 
    WNDCLASS  wc; 
 
    // Fill in the window class structure with parameters  
    // describing the main window.  
 
    wc.style = CS_OWNDC;         // Private-DC constant  
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
 
    wc.hIcon = LoadIcon((HINSTANCE) NULL, 
        MAKEINTRESOURCE(IDI_APPLICATION)); 
 
    wc.hCursor = LoadCursor((HINSTANCE) NULL, 
        MAKEINTRESOURCE(IDC_ARROW)); 
 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "GenericMenu"; 
    wc.lpszClassName = "GenericWClass"; 
 
    // Register the window class and return the resulting code.  
 
    return RegisterClass(&wc); 
} 
 
LRESULT APIENTRY MainWndProc( 
        HWND hwnd,           // window handle  
        UINT message,        // type of message  
        WPARAM wParam,       // additional information  
        LPARAM lParam)       // additional information  
{ 
 
    PAINTSTRUCT ps;              // paint structure  
 
    // Retrieve a handle identifying the private DC.  
 
    hdc = GetDC(hwnd); 
 
    switch (message) 
    { 
        case WM_PAINT: 
              hdc = BeginPaint(hwnd, &ps); 
 
        // Draw and paint using private DC. 
        
                 EndPaint(hwnd, &ps);
              
        case WM_DESTROY:
                     PostQuitMessage(0);
                     break;
        default:
                return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 
