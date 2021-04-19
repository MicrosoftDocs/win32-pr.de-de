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
# <a name="creating-an-mciwnd-window"></a><span data-ttu-id="d7b73-105">Erstellen eines mciwnd-Fensters</span><span class="sxs-lookup"><span data-stu-id="d7b73-105">Creating an MCIWnd Window</span></span>

<span data-ttu-id="d7b73-106">Die Funktion " [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) " registriert und erstellt ein mciwnd-Fenster.</span><span class="sxs-lookup"><span data-stu-id="d7b73-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function registers and creates an MCIWnd window.</span></span> <span data-ttu-id="d7b73-107">Das Fenster kann ein übergeordnetes Element, ein untergeordnetes Element oder ein Popup Fenster sein.</span><span class="sxs-lookup"><span data-stu-id="d7b73-107">The window can be a parent, child, or pop-up window.</span></span> <span data-ttu-id="d7b73-108">Im folgenden Beispiel wird ein mciwnd-Fenster als untergeordnetes Fenster erstellt und die Wiedergabe des Benutzer Steuer Elements ermöglicht, indem der Zugriff auf die TrackBar und die **Menü** Schaltflächen wiedergeben, **Beenden** und Menü bereit **gestellt wird.**</span><span class="sxs-lookup"><span data-stu-id="d7b73-108">The following example creates an MCIWnd window as a child window and lets the user control playback by providing access to the trackbar and the **Play**, **Stop**, and **Menu** buttons.</span></span> <span data-ttu-id="d7b73-109">Das Beispiel gibt ein Handle eines übergeordneten Fensters an und gibt **null** für die Fenster Stile an, sodass die Standardfenster Stile von WS \_ Child, WS \_ Border und WS \_ Visible verwendet werden, um das mciwnd-Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7b73-109">The example specifies a handle of a parent window and specifies **NULL** for the window styles, so the default window styles of WS\_CHILD, WS\_BORDER, and WS\_VISIBLE are used to create the MCIWnd window.</span></span>


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
> <span data-ttu-id="d7b73-110">Sie können auch für das übergeordnete Fenster Handle und die Fenster Stile **null** angeben. in diesem Fall werden die Standardfenster Stile als überlappende \_ und als \_ sichtbar angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7b73-110">You could also specify **NULL** for both the parent window handle and the window styles, in which case the default window styles would be WS\_OVERLAPPED and WS\_VISIBLE.</span></span>

 

 

 




