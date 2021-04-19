---
title: Erstellen eines mciwnd-Fensters
description: Erstellen eines mciwnd-Fensters
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Mciwnd-Fenster, erstellen
- Mciwndcreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341646"
---
# <a name="creating-an-mciwnd-window"></a>Erstellen eines mciwnd-Fensters

Die Funktion " [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) " registriert und erstellt ein mciwnd-Fenster. Das Fenster kann ein übergeordnetes Element, ein untergeordnetes Element oder ein Popup Fenster sein. Im folgenden Beispiel wird ein mciwnd-Fenster als untergeordnetes Fenster erstellt und die Wiedergabe des Benutzer Steuer Elements ermöglicht, indem der Zugriff auf die TrackBar und die **Menü** Schaltflächen wiedergeben, **Beenden** und Menü bereit **gestellt wird.** Das Beispiel gibt ein Handle eines übergeordneten Fensters an und gibt **null** für die Fenster Stile an, sodass die Standardfenster Stile von WS \_ Child, WS \_ Border und WS \_ Visible verwendet werden, um das mciwnd-Fenster zu erstellen.


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> Sie können auch für das übergeordnete Fenster Handle und die Fenster Stile **null** angeben. in diesem Fall werden die Standardfenster Stile als überlappende \_ und als \_ sichtbar angezeigt.

 

 

 




