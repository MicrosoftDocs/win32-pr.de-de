---
description: Das System ist nicht die einzige Quelle für WM \_ PAINT-Nachrichten. Die InvalidateRect- oder InvalidateRgn-Funktion kann indirekt WM \_ PAINT-Meldungen für Ihre Fenster generieren. Diese Funktionen markieren einen Clientbereich ganz oder teilweise als ungültig (der neu gezeichnet werden muss).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Ungültig machen des Clientbereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94a3a5b4e6903c549331788f9e81947dca44e7a699bb1a633bce46525585b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558660"
---
# <a name="invalidating-the-client-area"></a>Ungültig machen des Clientbereichs

Das System ist nicht die einzige Quelle für [**WM \_ PAINT-Nachrichten.**](wm-paint.md) Die [**InvalidateRect-**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) oder [**InvalidateRgn-Funktion**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) kann indirekt **WM \_ PAINT-Meldungen** für Ihre Fenster generieren. Diese Funktionen markieren einen Clientbereich ganz oder teilweise als ungültig (der neu gezeichnet werden muss).

Im folgenden Beispiel macht die Fensterprozedur den gesamten Clientbereich ungültig, wenn [**WM \_ CHAR-Nachrichten verarbeitet**](../inputdev/wm-char.md) werden. Dadurch kann der Benutzer die Abbildung ändern, indem er eine Zahl eintippen und die Ergebnisse anzeigen kann. Diese Ergebnisse werden gezeichnet, sobald keine anderen Nachrichten in der Nachrichtenwarteschlange der Anwendung enthalten sind.


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



In diesem Beispiel gibt das von [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) verwendete **NULL-Argument** den gesamten Clientbereich an. Das **TRUE-Argument** bewirkt, dass der Hintergrund gelöscht wird. Wenn Sie nicht möchten, dass die Anwendung wartet, bis die Nachrichtenwarteschlange der Anwendung keine anderen Nachrichten enthält, verwenden Sie die [**UpdateWindow-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) um zu erzwingen, dass die [**WM \_ PAINT-Nachricht**](wm-paint.md) sofort gesendet wird. Wenn ein ungültiger Teil des Clientbereichs vor liegt, sendet **UpdateWindow** die **WM \_ PAINT-Nachricht** für das angegebene Fenster direkt an die Fensterprozedur.

 

 
