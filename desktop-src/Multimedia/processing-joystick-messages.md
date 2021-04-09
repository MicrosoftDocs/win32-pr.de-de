---
title: Verarbeiten von Joystick Nachrichten
description: Verarbeiten von Joystick Nachrichten
ms.assetid: d21a9d49-1fc0-4899-9083-87c3cf4e0e62
keywords:
- Joysticks, Meldungen
- MM_JOY1MOVE Meldung
- MM_JOY1BUTTONDOWN Meldung
- MM_JOY1BUTTONUP Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f2337d392c0104dcb49839b19c5fb615481ee2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036764"
---
# <a name="processing-joystick-messages"></a><span data-ttu-id="7d729-107">Verarbeiten von Joystick Nachrichten</span><span class="sxs-lookup"><span data-stu-id="7d729-107">Processing Joystick Messages</span></span>

<span data-ttu-id="7d729-108">Im folgenden Beispiel wird veranschaulicht, wie eine Anwendung auf Joystick Bewegungen und Änderungen in den Schaltflächen Zuständen reagieren könnte.</span><span class="sxs-lookup"><span data-stu-id="7d729-108">The following example illustrates how an application could respond to joystick movements and changes in the button states.</span></span> <span data-ttu-id="7d729-109">Wenn sich der Joystick an der Position ändert, verschiebt die Anwendung den Cursor und zeichnet, wenn eine der beiden Schaltflächen gedrückt ist, ein Aufzählungs Zeichen auf dem Desktop auf.</span><span class="sxs-lookup"><span data-stu-id="7d729-109">When the joystick changes position, the application moves the cursor and, if either button is pressed, draws a bullet hole on the desktop.</span></span> <span data-ttu-id="7d729-110">Wenn eine Joystick Schaltfläche gedrückt wird, zeichnet die Anwendung ein Loch auf dem Desktop und wiederholt einen Sound, bis eine Schaltfläche losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="7d729-110">When a joystick button is pressed, the application draws a hole on the desktop and plays a sound continuously until a button is released.</span></span> <span data-ttu-id="7d729-111">Die zu überwachenden Nachrichten lauten [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md)und [**mm \_ JOY1BUTTONUP**](mm-joy1buttonup.md).</span><span class="sxs-lookup"><span data-stu-id="7d729-111">The messages to watch are [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1BUTTONDOWN**](mm-joy1buttondown.md), and [**MM\_JOY1BUTTONUP**](mm-joy1buttonup.md).</span></span>


```C++
case MM_JOY1MOVE :                     // changed position 
    if((UINT) wParam & (JOY_BUTTON1 | JOY_BUTTON2)) 
        DrawFire(hWnd); 
    DrawSight(lParam);                 // calculates new cursor position 
    break; 
case MM_JOY1BUTTONDOWN :               // button is down 
    if((UINT) wParam & JOY_BUTTON1) 
    { 
        PlaySound(lpButton1, SND_LOOP | SND_ASYNC | SND_MEMORY); 
        DrawFire(hWnd); 
    } 
    else if((UINT) wParam & JOY_BUTTON2) 
    { 
        PlaySound(lpButton2, SND_ASYNC | SND_MEMORY |  SND_LOOP); 
        DrawFire(hWnd); 
    } 
    break; 
case MM_JOY1BUTTONUP :                 // button is up 
    sndPlaySound(NULL, 0);             // stops the sound 
    break; 

```



 

 




