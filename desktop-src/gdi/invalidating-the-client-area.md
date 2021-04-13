---
description: Das System ist nicht die einzige Quelle von WM \_ Paint-Nachrichten. Die invalidateruor InvalidateRgn-Funktion kann indirekt WM \_ Paint-Meldungen für Ihre Fenster generieren. Diese Funktionen markieren den gesamten oder einen Teil eines Client Bereichs als ungültig (der neu gezeichnet werden muss).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Der Client Bereich wird ungültig gemacht.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76fb02be44f600b80f87ec8f05c022fa3c35d827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993959"
---
# <a name="invalidating-the-client-area"></a><span data-ttu-id="b50e7-105">Der Client Bereich wird ungültig gemacht.</span><span class="sxs-lookup"><span data-stu-id="b50e7-105">Invalidating the Client Area</span></span>

<span data-ttu-id="b50e7-106">Das System ist nicht die einzige Quelle von [**WM \_ Paint**](wm-paint.md) -Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="b50e7-106">The system is not the only source of [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="b50e7-107">Die [**invalidateruor**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) -Funktion kann indirekt **WM \_ Paint** -Meldungen für Ihre Fenster generieren.</span><span class="sxs-lookup"><span data-stu-id="b50e7-107">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function can indirectly generate **WM\_PAINT** messages for your windows.</span></span> <span data-ttu-id="b50e7-108">Diese Funktionen markieren den gesamten oder einen Teil eines Client Bereichs als ungültig (der neu gezeichnet werden muss).</span><span class="sxs-lookup"><span data-stu-id="b50e7-108">These functions mark all or part of a client area as invalid (that must be redrawn).</span></span>

<span data-ttu-id="b50e7-109">Im folgenden Beispiel wird der gesamte Client Bereich bei der Verarbeitung von [**WM \_ char**](../inputdev/wm-char.md) -Nachrichten durch die Fenster Prozedur ungültig.</span><span class="sxs-lookup"><span data-stu-id="b50e7-109">In the following example, the window procedure invalidates the entire client area when processing [**WM\_CHAR**](../inputdev/wm-char.md) messages.</span></span> <span data-ttu-id="b50e7-110">Dadurch kann der Benutzer die Abbildung ändern, indem er eine Zahl eingibt und die Ergebnisse anzeigen kann. Diese Ergebnisse werden gezeichnet, sobald in der Nachrichten Warteschlange der Anwendung keine weiteren Meldungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b50e7-110">This allows the user to change the figure by typing a number and view the results; these results are drawn as soon as there are no other messages in the application's message queue.</span></span>


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="b50e7-111">In diesem Beispiel gibt das von [**invalidaterierierten**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) **null** -Argument den gesamten Client Bereich an. Das **true** -Argument bewirkt, dass der Hintergrund gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b50e7-111">In this example, the **NULL** argument used by [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) specifies the entire client area; the **TRUE** argument causes the background to be erased.</span></span> <span data-ttu-id="b50e7-112">Wenn Sie nicht möchten, dass die Anwendung wartet, bis die Nachrichten Warteschlange der Anwendung keine weiteren Nachrichten enthält, erzwingen Sie mithilfe der [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) -Funktion, dass die WM-Zeichnungs Nachricht sofort gesendet wird. [**\_**](wm-paint.md)</span><span class="sxs-lookup"><span data-stu-id="b50e7-112">If you do not want the application to wait until the application's message queue has no other messages, use the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) function to force the [**WM\_PAINT**](wm-paint.md) message to be sent immediately.</span></span> <span data-ttu-id="b50e7-113">Wenn ein ungültiger Teil des Client Bereichs vorhanden ist, sendet **UpdateWindow** die **WM \_** -Zeichnungs Nachricht für das angegebene Fenster direkt an die Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b50e7-113">If there is any invalid part of the client area, **UpdateWindow** sends the **WM\_PAINT** message for the specified window directly to the window procedure.</span></span>

 

 
