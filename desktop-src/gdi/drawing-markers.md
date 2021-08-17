---
description: Sie können die Linienfunktionen verwenden, um Marker zu zeichnen.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Zeichnen von Markern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5e05c651bf95aa48a8ef11fd0819523ee5da7652e27ecebaeff8ee9de4f1e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887118"
---
# <a name="drawing-markers"></a>Zeichnen von Markern

Sie können die Linienfunktionen verwenden, um Marker zu zeichnen. Ein Marker ist ein Symbol, das über einem Punkt zentriert ist. Zeichenanwendungen verwenden Marker, um Ausgangspunkte, Endpunkte und Kontrollpunkte zu bestimmen. Tabellenkalkulationsanwendungen verwenden Marker, um Points of Interest in einem Diagramm oder Diagramm zu bestimmen.

Im folgenden Codebeispiel erstellt die anwendungsdefinierte Markerfunktion mithilfe der [**Funktionen MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) und [**LineTo einen Marker.**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) Diese Funktionen zeichnen zwei sich überschneidende Linien mit einer Länge von 20 Pixeln, die über den Cursorkoordinaten zentriert sind.


```C++
void Marker(LONG x, LONG y, HWND hwnd) 
{ 
    HDC hdc; 
 
    hdc = GetDC(hwnd); 
        MoveToEx(hdc, (int) x - 10, (int) y, (LPPOINT) NULL); 
        LineTo(hdc, (int) x + 10, (int) y); 
        MoveToEx(hdc, (int) x, (int) y - 10, (LPPOINT) NULL); 
        LineTo(hdc, (int) x, (int) y + 10); 

    ReleaseDC(hwnd, hdc); 
} 
```



Das System speichert die Koordinaten des Cursors im *lParam-Parameter* der [**\_ WM-LBUTTONDOWN-Nachricht,**](../inputdev/wm-lbuttondown.md) wenn der Benutzer die linke Maustaste drückt. Der folgende Code veranschaulicht, wie eine Anwendung diese Koordinaten erhält, bestimmt, ob sie sich innerhalb ihres Clientbereichs liegen, und übergibt sie an die Markerfunktion, um den Marker zu zeichnen.


```C++
// Line- and arc-drawing variables  
 
static BOOL bCollectPoints; 
static POINT ptMouseDown[32]; 
static int index; 
POINTS ptTmp; 
RECT rc; 
 
    case WM_LBUTTONDOWN: 
 
 
        if (bCollectPoints && index < 32)
        { 
            // Create the region from the client area.  
 
            GetClientRect(hwnd, &rc); 
            hrgn = CreateRectRgn(rc.left, rc.top, 
                rc.right, rc.bottom); 
 
            ptTmp = MAKEPOINTS((POINTS FAR *) lParam); 
            ptMouseDown[index].x = (LONG) ptTmp.x; 
            ptMouseDown[index].y = (LONG) ptTmp.y; 
 
            // Test for a hit in the client rectangle.  
 
            if (PtInRegion(hrgn, ptMouseDown[index].x, 
                    ptMouseDown[index].y)) 
            { 
                // If a hit occurs, record the mouse coords.  
 
                Marker(ptMouseDown[index].x, ptMouseDown[index].y, 
                    hwnd); 
                index++; 
            } 
        } 
        break; 
```



 

 
