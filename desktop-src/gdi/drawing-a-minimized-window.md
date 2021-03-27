---
description: Sie können Ihre eigenen minimierten Fenster zeichnen, damit Sie nicht vom System für Sie gezeichnet werden.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Zeichnen eines minimierten Fensters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393561"
---
# <a name="drawing-a-minimized-window"></a><span data-ttu-id="abfac-103">Zeichnen eines minimierten Fensters</span><span class="sxs-lookup"><span data-stu-id="abfac-103">Drawing a Minimized Window</span></span>

<span data-ttu-id="abfac-104">Sie können Ihre eigenen minimierten Fenster zeichnen, damit Sie nicht vom System für Sie gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="abfac-104">You can draw your own minimized windows rather than having the system draw them for you.</span></span> <span data-ttu-id="abfac-105">Die meisten Anwendungen definieren ein Klassen Symbol, wenn die Fenster Klasse für das Fenster registriert wird, und das System zeichnet das Symbol, wenn das Fenster minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="abfac-105">Most applications define a class icon when registering the window class for the window, and the system draws the icon when the window is minimized.</span></span> <span data-ttu-id="abfac-106">Wenn Sie das Klassen Symbol jedoch auf **null** festlegen, sendet das System immer dann eine [**WM \_ Paint**](wm-paint.md) -Meldung an die Fenster Prozedur, wenn das Fenster minimiert wird, sodass die Fenster Prozedur im minimierten Fenster gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="abfac-106">If you set the class icon to **NULL**, however, the system sends a [**WM\_PAINT**](wm-paint.md) message to your window procedure whenever the window is minimized, enabling the window procedure to draw in the minimized window.</span></span>

<span data-ttu-id="abfac-107">Im folgenden Beispiel zeichnet die Fenster Prozedur einen Stern im minimierten Fenster.</span><span class="sxs-lookup"><span data-stu-id="abfac-107">In the following example, the window procedure draws a star in the minimized window.</span></span> <span data-ttu-id="abfac-108">[**Die-**](/windows/win32/api/winuser/nf-winuser-isiconic) Prozedur bestimmt, wann das Fenster minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="abfac-108">The procedure uses the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function to determine when the window is minimized.</span></span> <span data-ttu-id="abfac-109">Dadurch wird sichergestellt, dass der Stern nur gezeichnet wird, wenn das Fenster minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="abfac-109">This ensures that the star is drawn only when the window is minimized.</span></span>


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="abfac-110">Sie legen das Klassen Symbol auf **null** fest, indem Sie den **HICON** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur auf **null** festlegen, bevor Sie die [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion für die Fenster Klasse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="abfac-110">You set the class icon to **NULL** by setting the **hIcon** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to **NULL** before calling the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function for the window class.</span></span>

 

 
