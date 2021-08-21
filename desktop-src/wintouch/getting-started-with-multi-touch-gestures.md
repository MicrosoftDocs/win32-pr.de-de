---
title: Erste Schritte mit Windows Touchgesten
description: In diesem Abschnitt werden die grundlegenden Schritte für die Verwendung von Multitouchgesten beschrieben.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Windows Toucheingabe, Gesten
- Windows Toucheingabe, Nachrichten
- Gesten, Informationen
- Gesten, Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47b114eebc80946652d7118cc4eaab23092b779fa8897053aae229072fbc428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030337"
---
# <a name="getting-started-with-windows-touch-gestures"></a>Erste Schritte mit Windows Touchgesten

In diesem Abschnitt werden die grundlegenden Schritte für die Verwendung von Multitouchgesten beschrieben.

Die folgenden Schritte werden in der Regel ausgeführt, wenn Windows Touchgesten verwendet werden:

1.  Richten Sie ein Fenster zum Empfangen von Gesten ein.
2.  Behandeln Sie die Gestenmeldungen.
3.  Interpretieren der Gestenmeldungen.

## <a name="setting-up-a-window-to-receive-gestures"></a>Einrichten eines Fensters zum Empfangen von Gesten

Standardmäßig erhalten Sie [**WM \_ GESTURE-Nachrichten.**](wm-gesture.md)

> [!Note]  
> Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)aufrufen, erhalten Sie keine [**WM \_ GESTURE-Meldungen**](wm-gesture.md) mehr. Wenn Sie keine **WM \_ GESTURE-Meldungen** erhalten, stellen Sie sicher, dass Sie **RegisterTouchWindow** nicht aufgerufen haben.

 

Der folgende Code zeigt eine einfache InitInstance-Implementierung.


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a>Verarbeiten von Gestennachrichten

Ähnlich wie bei der Verarbeitung Windows Toucheingabenachrichten können Sie Gestennachrichten auf unterschiedliche Weise verarbeiten. Wenn Sie Win32 verwenden, können Sie in WndProc nach der [**WM \_ GESTURE-Meldung**](wm-gesture.md) suchen. Wenn Sie einen anderen Anwendungstyp erstellen, können Sie der Meldungszuordnung die **WM \_ GESTURE-Nachricht** hinzufügen und dann einen benutzerdefinierten Handler implementieren.

Der folgende Code zeigt, wie Gestennachrichten behandelt werden können.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a>Interpretieren der Gestenmeldungen

Die [**GetGestureInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) wird verwendet, um eine Gestennachricht in eine Struktur zu interpretieren, die die Geste beschreibt. Die [**Struktur GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)enthält Informationen über die Geste, z. B. die Position, an der die Geste ausgeführt wurde, und den Typ der Geste. Der folgende Code zeigt, wie Sie eine Gestennachricht abrufen und interpretieren können.


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Touchgesten](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




