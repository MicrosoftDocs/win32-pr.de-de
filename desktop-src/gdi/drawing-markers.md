---
description: Sie können die Linienfunktionen zum Zeichnen von Markern verwenden.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Zeichnungs Marker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b725e3a266e296950394a9bb9b2b76a17cb25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754432"
---
# <a name="drawing-markers"></a><span data-ttu-id="f9b8d-103">Zeichnungs Marker</span><span class="sxs-lookup"><span data-stu-id="f9b8d-103">Drawing Markers</span></span>

<span data-ttu-id="f9b8d-104">Sie können die Linienfunktionen zum Zeichnen von Markern verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-104">You can use the line functions to draw markers.</span></span> <span data-ttu-id="f9b8d-105">Ein Marker ist ein Symbol, das auf einen Punkt zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-105">A marker is a symbol centered over a point.</span></span> <span data-ttu-id="f9b8d-106">Zeichen Anwendungen verwenden Marker, um Anfangspunkte, Endpunkte und Steuerungs Punkte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-106">Drawing applications use markers to designate starting points, ending points, and control points.</span></span> <span data-ttu-id="f9b8d-107">Arbeitsblatt Anwendungen verwenden Marker, um relevante Punkte in einem Diagramm oder Diagramm zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-107">Spreadsheet applications use markers to designate points of interest on a chart or graph.</span></span>

<span data-ttu-id="f9b8d-108">Im folgenden Codebeispiel erstellt die Anwendungs definierte markerfunktion einen Marker mithilfe der Funktionen " [**muveumex**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) " und " [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) ".</span><span class="sxs-lookup"><span data-stu-id="f9b8d-108">In the following code sample, the application-defined Marker function creates a marker by using the [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) and [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) functions.</span></span> <span data-ttu-id="f9b8d-109">Diese Funktionen zeichnen zwei überlappende Zeilen mit einer Länge von 20 Pixeln, die auf die Cursor Koordinaten zentriert sind.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-109">These functions draw two intersecting lines, 20 pixels in length, centered over the cursor coordinates.</span></span>


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



<span data-ttu-id="f9b8d-110">Das System speichert die Koordinaten des Cursors im *LPARAM* -Parameter der [**WM \_ lbuttondown**](../inputdev/wm-lbuttondown.md) -Meldung, wenn der Benutzer die linke Maustaste drückt.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-110">The system stores the coordinates of the cursor in the *lParam* parameter of the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message when the user presses the left mouse button.</span></span> <span data-ttu-id="f9b8d-111">Der folgende Code veranschaulicht, wie eine Anwendung diese Koordinaten abruft, bestimmt, ob Sie in Ihrem Client Bereich liegen, und übergibt sie an die markerfunktion, um den Marker zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-111">The following code demonstrates how an application gets these coordinates, determines whether they lie within its client area, and passes them to the Marker function to draw the marker.</span></span>


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



 

 
