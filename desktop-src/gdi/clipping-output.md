---
description: Nachdem der Benutzer im Menü auf Clip geklickt hat, verwendet die Anwendung die Koordinaten des Rechtecks, das der Benutzer erstellt hat, um einen Clippingbereich zu definieren.
ms.assetid: 5ae60181-c72e-4a28-99eb-e23d35c46685
title: Clipping-Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc0181340b03421815ebe0f5cd8328d4793a406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959315"
---
# <a name="clipping-output"></a><span data-ttu-id="c8f44-103">Clipping-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c8f44-103">Clipping Output</span></span>

<span data-ttu-id="c8f44-104">Nachdem der Benutzer im Menü auf Clip geklickt hat, verwendet die Anwendung die Koordinaten des Rechtecks, das der Benutzer erstellt hat, um einen Clippingbereich zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c8f44-104">After the user clicks Clip from the menu, the application uses the coordinates of the rectangle the user created to define a clipping region.</span></span> <span data-ttu-id="c8f44-105">Nachdem der Clippingbereich definiert und in den Gerätekontext der Anwendung ausgewählt wurde, zeichnet die Anwendung das Bitmap-Bild neu.</span><span class="sxs-lookup"><span data-stu-id="c8f44-105">After defining the clipping region and selecting it into the application's device context, the application redraws the bitmapped image.</span></span> <span data-ttu-id="c8f44-106">Die Anwendung führt diese Aufgaben wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="c8f44-106">The application performs these tasks, as follows.</span></span>


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
 
    case IDM_CLIP: 
 
    hdc = GetDC(hwnd); 
 
    // Retrieve the application's client rectangle and paint  
    // with the default (white) brush.  
 
    GetClientRect(hwnd, &rctTmp); 
    FillRect(hdc, &rctTmp, GetStockObject(WHITE_BRUSH)); 
 
    // Use the rect coordinates to define a clipping region.  
 
    hrgn = CreateRectRgn(aptRect[0].x, aptRect[0].y, 
        aptRect[2].x, aptRect[2].y); 
    SelectClipRgn(hdc, hrgn); 
 
    // Transfer (draw) the bitmap into the clipped rectangle.  
 
    BitBlt(hdc, 
       0, 0, 
       bmp.bmWidth, bmp.bmHeight, 
       hdcCompatible, 
       0, 0, 
       SRCCOPY); 
 
    ReleaseDC(hwnd, hdc); 
    break; 
    }
```



 

 



