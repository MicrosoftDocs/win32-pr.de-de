---
description: Sie können die Menge an Zeichen, die Ihre Anwendung durchführt, bei der Verarbeitung der WM-Zeichnungs Nachricht begrenzen, \_ indem Sie die Größe und den Speicherort des Aktualisierungs Bereichs bestimmen.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Neuzeichnen in der Aktualisierungs Region
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993879"
---
# <a name="redrawing-in-the-update-region"></a><span data-ttu-id="9fe3a-103">Neuzeichnen in der Aktualisierungs Region</span><span class="sxs-lookup"><span data-stu-id="9fe3a-103">Redrawing in the Update Region</span></span>

<span data-ttu-id="9fe3a-104">Sie können die Menge an Zeichen, die Ihre Anwendung durchführt, bei der Verarbeitung der WM-Zeichnungs Nachricht begrenzen, indem Sie die Größe und den Speicherort des Aktualisierungs Bereichs bestimmen. [**\_**](wm-paint.md)</span><span class="sxs-lookup"><span data-stu-id="9fe3a-104">You can limit the amount of drawing your application carries out when processing the [**WM\_PAINT**](wm-paint.md) message by determining the size and location of the update region.</span></span> <span data-ttu-id="9fe3a-105">Da das System beim Erstellen des Clippingbereichs für den Gerätekontext des Fensters den Aktualisierungs Bereich verwendet, können Sie den Aktualisierungs Bereich indirekt ermitteln, indem Sie den Ausschneide Bereich untersuchen.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-105">Because the system uses the update region when creating the clipping region for the window's display device context, you can indirectly determine the update region by examining the clipping region.</span></span>

<span data-ttu-id="9fe3a-106">Im folgenden Beispiel zeichnet die Fenster Prozedur ein Dreieck, ein Rechteck, ein Pentagon und ein Sechseck, aber nur, wenn sich alle oder ein Teil jeder Abbildung innerhalb des Aktualisierungs Bereichs befindet.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-106">In the following example, the window procedure draws a triangle, a rectangle, a pentagon, and a hexagon, but only if all or a portion of each figure lies within the update region.</span></span> <span data-ttu-id="9fe3a-107">Die Fenster Prozedur verwendet die Funktion " [**rectvisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) " und ein "100-by-100"-Rechteck, um zu bestimmen, ob sich eine Abbildung im Ausschneide Bereich (und somit in der Update Region) für den gemeinsamen Gerätekontext befindet, der von [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-107">The window procedure uses the [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) function and a 100-by-100 rectangle to determine whether a figure is within the clipping region (and therefore the update region) for the common device context retrieved by [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span></span>


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



<span data-ttu-id="9fe3a-108">Die Koordinaten jeder Abbildung in diesem Beispiel liegen innerhalb desselben 100-by-100-Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-108">The coordinates of each figure in this example lie within the same 100-by-100 rectangle.</span></span> <span data-ttu-id="9fe3a-109">Vor dem Zeichnen einer Abbildung legt die Fenster Prozedur den Ansichts Anschluss mithilfe der [**setviewportorgex**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) -Funktion auf einen anderen Teil des Client Bereichs fest.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-109">Before drawing a figure, the window procedure sets the viewport origin to a different part of the client area by using the [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) function.</span></span> <span data-ttu-id="9fe3a-110">Dadurch wird verhindert, dass Abbildungen oberhalb der anderen gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-110">This prevents figures from being drawn one on top of the other.</span></span> <span data-ttu-id="9fe3a-111">Das Ändern des Ansichts Ansichts Ursprungs wirkt sich nicht auf den Clippingbereich aus, wirkt sich jedoch darauf aus, wie die Koordinaten des Rechtecks, das an [**rectvisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) übergeben wird</span><span class="sxs-lookup"><span data-stu-id="9fe3a-111">Changing the viewport origin does not affect the clipping region, but does affect how the coordinates of the rectangle passed to [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) are interpreted.</span></span> <span data-ttu-id="9fe3a-112">Wenn Sie den Ursprung ändern, können Sie auch ein einzelnes Rechteck verwenden, um den Aktualisierungs Bereich anstelle einzelner Rechtecke für jede Abbildung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9fe3a-112">Changing the origin also allows you to use a single rectangle to check the update region rather than individual rectangles for each figure.</span></span>

 

 



