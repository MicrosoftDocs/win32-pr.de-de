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
# <a name="invalidating-the-client-area"></a>Der Client Bereich wird ungültig gemacht.

Das System ist nicht die einzige Quelle von [**WM \_ Paint**](wm-paint.md) -Nachrichten. Die [**invalidateruor**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) -Funktion kann indirekt **WM \_ Paint** -Meldungen für Ihre Fenster generieren. Diese Funktionen markieren den gesamten oder einen Teil eines Client Bereichs als ungültig (der neu gezeichnet werden muss).

Im folgenden Beispiel wird der gesamte Client Bereich bei der Verarbeitung von [**WM \_ char**](../inputdev/wm-char.md) -Nachrichten durch die Fenster Prozedur ungültig. Dadurch kann der Benutzer die Abbildung ändern, indem er eine Zahl eingibt und die Ergebnisse anzeigen kann. Diese Ergebnisse werden gezeichnet, sobald in der Nachrichten Warteschlange der Anwendung keine weiteren Meldungen vorhanden sind.


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



In diesem Beispiel gibt das von [**invalidaterierierten**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) **null** -Argument den gesamten Client Bereich an. Das **true** -Argument bewirkt, dass der Hintergrund gelöscht wird. Wenn Sie nicht möchten, dass die Anwendung wartet, bis die Nachrichten Warteschlange der Anwendung keine weiteren Nachrichten enthält, erzwingen Sie mithilfe der [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) -Funktion, dass die WM-Zeichnungs Nachricht sofort gesendet wird. [**\_**](wm-paint.md) Wenn ein ungültiger Teil des Client Bereichs vorhanden ist, sendet **UpdateWindow** die **WM \_** -Zeichnungs Nachricht für das angegebene Fenster direkt an die Fenster Prozedur.

 

 
