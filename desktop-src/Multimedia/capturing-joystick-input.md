---
title: Erfassen von Joystick Eingaben
description: Erfassen von Joystick Eingaben
ms.assetid: 1214fe5a-5a6a-4c6c-9b77-94eeb73f60da
keywords:
- Joysticks, Erfassen von Eingaben
- Erfassen von Joystick Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23fd3717ad09fd2e52f1a815f7d13b91963a13e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101611"
---
# <a name="capturing-joystick-input"></a><span data-ttu-id="1ccc3-105">Erfassen von Joystick Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ccc3-105">Capturing Joystick Input</span></span>

<span data-ttu-id="1ccc3-106">Der größte Teil des Codes, der den Joystick steuert, befindet sich in der Hauptfenster Funktion.</span><span class="sxs-lookup"><span data-stu-id="1ccc3-106">Most of the code controlling the joystick is in the main window function.</span></span> <span data-ttu-id="1ccc3-107">Im folgenden Teil des Nachrichten Handlers Ruft die Anwendung [**joysetcapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) auf, um Eingaben aus dem Joystick JOYSTICKID1 aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="1ccc3-107">In the following portion of the message handler, the application calls [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to capture input from the joystick JOYSTICKID1.</span></span>


```C++
case WM_CREATE: 
    if(joySetCapture(hWnd, JOYSTICKID1, NULL, FALSE)) 
    { 
        MessageBeep(MB_ICONEXCLAMATION); 
        MessageBox(hWnd, "Couldn't capture the joystick.", NULL, 
            MB_OK | MB_ICONEXCLAMATION); 
        PostMessage(hWnd,WM_CLOSE,0,0L); 
    } 
    break; 
 
```



 

 