---
description: Sie können Ihren eigenen Fenster Hintergrund zeichnen, anstatt das System für Sie zu zeichnen.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Zeichnen eines benutzerdefinierten Fenster Hintergrunds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978649"
---
# <a name="drawing-a-custom-window-background"></a><span data-ttu-id="fa24a-103">Zeichnen eines benutzerdefinierten Fenster Hintergrunds</span><span class="sxs-lookup"><span data-stu-id="fa24a-103">Drawing a Custom Window Background</span></span>

<span data-ttu-id="fa24a-104">Sie können Ihren eigenen Fenster Hintergrund zeichnen, anstatt das System für Sie zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="fa24a-104">You can draw your own window background rather than having the system draw it for you.</span></span> <span data-ttu-id="fa24a-105">Die meisten Anwendungen geben ein Pinsel handle oder einen System Farbwert für den klassenhintergrund Pinsel beim Registrieren der Fenster Klasse an. Das System verwendet den Pinsel oder die Farbe zum Zeichnen des Hintergrunds.</span><span class="sxs-lookup"><span data-stu-id="fa24a-105">Most applications specify a brush handle or system color value for the class background brush when registering the window class; the system uses the brush or color to draw the background.</span></span> <span data-ttu-id="fa24a-106">Wenn Sie den klassenhintergrund Pinsel jedoch auf **null** festlegen, sendet das System immer dann eine [**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Meldung an die Fenster Prozedur, wenn der Hintergrund des Fensters gezeichnet werden muss, sodass Sie einen benutzerdefinierten Hintergrund zeichnen können.</span><span class="sxs-lookup"><span data-stu-id="fa24a-106">If you set the class background brush to **NULL**, however, the system sends a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to your window procedure whenever the window background must be drawn, letting you draw a custom background.</span></span>

<span data-ttu-id="fa24a-107">Im folgenden Beispiel zeichnet die Fenster Prozedur ein großes Prüf Board-Muster, das sauber in das Fenster passt.</span><span class="sxs-lookup"><span data-stu-id="fa24a-107">In the following example, the window procedure draws a large checkerboard pattern that fits neatly in the window.</span></span> <span data-ttu-id="fa24a-108">Die Prozedur füllt den Client Bereich mit einem weißen Pinsel und zeichnet dann 13 20-bis-20 Rechtecke mit einem grauen Pinsel.</span><span class="sxs-lookup"><span data-stu-id="fa24a-108">The procedure fills the client area with a white brush and then draws thirteen 20-by-20 rectangles using a gray brush.</span></span> <span data-ttu-id="fa24a-109">Der Anzeigegeräte Kontext, der beim Zeichnen des Hintergrunds verwendet werden soll, wird im *wParam* -Parameter für die Nachricht angegeben.</span><span class="sxs-lookup"><span data-stu-id="fa24a-109">The display device context to use when drawing the background is specified in the *wParam* parameter for the message.</span></span>


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



<span data-ttu-id="fa24a-110">Wenn die Anwendung ein eigenes minimiertes Fenster zeichnet, sendet das System auch die " [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) "-Meldung an die Fenster Prozedur, um den Hintergrund für das minimierte Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="fa24a-110">If the application draws its own minimized window, the system also sends the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to the window procedure to draw the background for the minimized window.</span></span> <span data-ttu-id="fa24a-111">Sie können das gleiche Verfahren verwenden, das von [**WM \_ Paint**](wm-paint.md) verwendet wird, um zu bestimmen, ob das Fenster minimiert ist, und die Funktion [**isienic**](/windows/win32/api/winuser/nf-winuser-isiconic) aufzurufen und den Rückgabewert **true** zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fa24a-111">You can use the same technique used by [**WM\_PAINT**](wm-paint.md) to determine whether the window is minimized that is, call the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function and check for the return value **TRUE**.</span></span>

 

 
