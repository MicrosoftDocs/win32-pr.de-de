---
title: Ersten Einstieg in Windows-Touchbewegungen
description: In diesem Abschnitt werden die grundlegenden Schritte für die Verwendung von multitouchgesten beschrieben.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Windows-Toucheingabe, Gesten
- Windows-Fingereingabe, Meldungen
- Gesten, Informationen
- Gesten, Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388012"
---
# <a name="getting-started-with-windows-touch-gestures"></a>Ersten Einstieg in Windows-Touchbewegungen

In diesem Abschnitt werden die grundlegenden Schritte für die Verwendung von multitouchgesten beschrieben.

Die folgenden Schritte werden in der Regel bei der Verwendung von Windows-Touchgesten durchgeführt:

1.  Einrichten eines Fensters zum Empfangen von Gesten.
2.  Behandelt die Gesten Nachrichten.
3.  Interpretiert die Gesten Nachrichten.

## <a name="setting-up-a-window-to-receive-gestures"></a>Einrichten eines Fensters zum Empfangen von Gesten

Standardmäßig erhalten Sie [**WM- \_ Gesten**](wm-gesture.md) Nachrichten.

> [!Note]  
> Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)aufrufen, wird der Empfang von [**WM- \_ Gesten**](wm-gesture.md) Nachrichten beendet. Wenn Sie keine Nachrichten der **WM- \_ Geste** empfangen, stellen Sie sicher, dass Sie **RegisterTouchWindow** nicht aufgerufen haben.

 

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



## <a name="handling-gesture-messages"></a>Verarbeiten von Gesten Nachrichten

Ähnlich wie bei der Handhabung von Windows-toucheingabenachrichten können Sie Gesten Nachrichten in vielerlei Hinsicht verarbeiten. Wenn Sie Win32 verwenden, können Sie in WndProc nach der Meldung der [**WM- \_ Geste**](wm-gesture.md) suchen. Wenn Sie einen anderen Anwendungstyp erstellen, können Sie die **WM- \_ Gesten** Nachricht der Meldungs Zuordnung hinzufügen und dann einen benutzerdefinierten Handler implementieren.

Der folgende Code zeigt, wie Gesten Nachrichten behandelt werden könnten.


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



## <a name="interpreting-the-gesture-messages"></a>Interpretieren der Gesten Nachrichten

Mit der [**getgestureinfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) -Funktion wird eine Gesten Nachricht in eine Struktur interpretiert, in der die Geste beschrieben wird. Die Struktur " [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)" enthält Informationen über die Geste, wie z. b. den Speicherort, an dem die Geste ausgeführt wurde, und den Typ der Geste. Der folgende Code zeigt, wie Sie eine Gesten Nachricht abrufen und interpretieren können.


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

[Windows-Touchgesten](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




