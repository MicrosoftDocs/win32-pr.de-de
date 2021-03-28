---
description: Wenn der Benutzer auf Clip Bereich definieren klickt, gibt das System eine WM- \_ Befehls Meldung aus.
ms.assetid: 4b20f310-98c0-42c1-b3b3-eadf9bb2003c
title: Definieren des Clippingbereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e49693c0e94ab9b43af817f80985af98ae2ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528379"
---
# <a name="defining-the-clipping-region"></a><span data-ttu-id="1612e-103">Definieren des Clippingbereichs</span><span class="sxs-lookup"><span data-stu-id="1612e-103">Defining the Clipping Region</span></span>

<span data-ttu-id="1612e-104">Wenn der Benutzer auf Clip Bereich definieren klickt, gibt das System eine [**WM- \_ Befehls**](../menurc/wm-command.md) Meldung aus.</span><span class="sxs-lookup"><span data-stu-id="1612e-104">When the user clicks Define Clip Region , the system issues a [**WM\_COMMAND**](../menurc/wm-command.md) message.</span></span> <span data-ttu-id="1612e-105">Der *wParam* -Parameter dieser Nachricht enthält eine Anwendungs definierte Konstante, IDM- \_ Definition, die angibt, dass der Benutzer diese Option im Menü ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="1612e-105">The *wParam* parameter of this message contains an application-defined constant, IDM\_DEFINE, that indicates that the user selected this option from the menu.</span></span> <span data-ttu-id="1612e-106">Die Anwendung verarbeitet diese Eingabe, indem Sie wie im folgenden Codebeispiel gezeigt ein boolesches Flag ("f defineregion") festlegt.</span><span class="sxs-lookup"><span data-stu-id="1612e-106">The application processes this input by setting a Boolean flag, fDefineRegion, as shown in the following code sample.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
 
        case IDM_DEFINE: 
            fDefineRegion = TRUE; 
            break; 
```



<span data-ttu-id="1612e-107">Nachdem Sie auf **Clippingbereich definieren** geklickt haben, kann der Benutzer mit dem Zeichnen des Rechtecks beginnen, indem er auf die Maus klickt, während sich der Cursor im Client Bereich der Anwendung befindet.</span><span class="sxs-lookup"><span data-stu-id="1612e-107">After clicking **Define Clipping Region** , the user can begin drawing the rectangle by clicking and dragging the mouse while the cursor is in the application's client area.</span></span>

<span data-ttu-id="1612e-108">Wenn der Benutzer die linke Maustaste drückt, gibt das System eine [**WM- \_ lbuttondown**](../inputdev/wm-lbuttondown.md) -Meldung aus.</span><span class="sxs-lookup"><span data-stu-id="1612e-108">When the user presses the left button, the system issues a [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message.</span></span> <span data-ttu-id="1612e-109">Der *LPARAM* -Parameter dieser Nachricht enthält die Cursor Koordinaten, die der oberen linken Ecke eines Rechtecks entsprechen, das zum Definieren des Clippingbereichs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1612e-109">The *lParam* parameter of this message contains the cursor coordinates, which correspond to the upper left corner of a rectangle used to define the clipping region.</span></span> <span data-ttu-id="1612e-110">Die Anwendung verarbeitet die **WM \_ lbuttondown** -Nachricht wie folgt.</span><span class="sxs-lookup"><span data-stu-id="1612e-110">The application processes the **WM\_LBUTTONDOWN** message, as follows.</span></span>


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
 
switch (message) 
{ 
 
    case WM_LBUTTONDOWN: 
        if (fDefineRegion) 
        { 
 
        // Retrieve the new upper left corner.  
 
            ptsTmp = MAKEPOINTS(lParam); 
            ptUpperLeft.x = (LONG) ptsTmp.x; 
            ptUpperLeft.y = (LONG) ptsTmp.y; 
        } 
 
        if (fRegionExists) 
        { 
 
            // Erase the previous rectangle.  
 
            hdc = GetDC(hwnd); 
            SetROP2(hdc, R2_NOTXORPEN); 
 
            if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
                errhandler("Polyline Failed", hwnd); 
            ReleaseDC(hwnd, hdc); 
 
            // Clear the rectangle coordinates.  
 
            for (i = 0; i < 4; i++) 
            { 
                aptRect[i].x = 0; 
                aptRect[i].y = 0; 
            } 
 
            // Clear the temporary point structure.  
 
            ptTmp.x = 0; 
            ptTmp.y = 0; 
 
            // Clear the lower right coordinates.  
 
            ptLowerRight.x = 0; 
            ptLowerRight.y = 0; 
 
            // Reset the flag.  
 
            fRegionExists = FALSE; 
            fDefineRegion = TRUE; 
 
            // Retrieve the new upper left corner.  
 
            ptsTmp = MAKEPOINTS(lParam); 
            ptUpperLeft.x = (LONG) ptsTmp.x; 
            ptUpperLeft.y = (LONG) ptsTmp.y; 
        } 
    break; 
}
```



<span data-ttu-id="1612e-111">Wenn der Benutzer die Maus zieht, gibt das System [**WM- \_ MouseMove**](../inputdev/wm-mousemove.md) -Nachrichten aus und speichert die neuen Cursor Koordinaten im *LPARAM* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="1612e-111">As the user drags the mouse, the system issues [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages and stores the new cursor coordinates in the *lParam* parameter.</span></span> <span data-ttu-id="1612e-112">Jedes Mal, wenn die Anwendung eine neue **WM- \_ MouseMove** -Nachricht empfängt, löscht Sie das vorherige Rechteck (sofern vorhanden) und zeichnet das neue Rechteck durch Aufrufen der [**polylinienfunktion**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) , wobei die Koordinaten der vier Ecken des Rechtecks übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1612e-112">Each time the application receives a new **WM\_MOUSEMOVE** message, it erases the previous rectangle (if one exists) and draws the new rectangle by calling the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function, passing it the coordinates of the four corners of the rectangle.</span></span> <span data-ttu-id="1612e-113">Die Anwendung führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="1612e-113">The application performs the following tasks.</span></span>


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
 
switch (message) 
{ 
 
    case WM_MOUSEMOVE: 
 
    if (wParam & MK_LBUTTON && fDefineRegion) 
    { 
 
        // Get a window DC.  
 
        hdc = GetDC(hwnd); 
 
        if (!SetROP2(hdc, R2_NOTXORPEN)) 
            errhandler("SetROP2 Failed", hwnd); 
 
        // If previous mouse movement occurred, store the original  
        // lower right corner coordinates in a temporary structure.  
 
        if (ptLowerRight.x) 
        { 
            ptTmp.x = ptLowerRight.x; 
            ptTmp.y = ptLowerRight.y; 
        } 
 
        // Get the new coordinates of the clipping region's lower  
        // right corner.  
 
        ptsTmp = MAKEPOINTS(lParam); 
        ptLowerRight.x = (LONG) ptsTmp.x; 
        ptLowerRight.y = (LONG) ptsTmp.y; 
 
        // If previous mouse movement occurred, erase the original  
        // rectangle.  
 
        if (ptTmp.x) 
        { 
            aptRect[0].x = ptUpperLeft.x; 
            aptRect[0].y = ptUpperLeft.y; 
            aptRect[1].x = ptTmp.x; 
            aptRect[1].y = ptUpperLeft.y; 
            aptRect[2].x = ptTmp.x; 
            aptRect[2].y = ptTmp.y; 
            aptRect[3].x = ptUpperLeft.x; 
            aptRect[3].y = ptTmp.y; 
            aptRect[4].x = aptRect[0].x; 
            aptRect[4].y = aptRect[0].y; 
 
            if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
                errhandler("Polyline Failed", hwnd); 
        } 
 
        aptRect[0].x = ptUpperLeft.x; 
        aptRect[0].y = ptUpperLeft.y; 
        aptRect[1].x = ptLowerRight.x; 
        aptRect[1].y = ptUpperLeft.y; 
        aptRect[2].x = ptLowerRight.x; 
        aptRect[2].y = ptLowerRight.y; 
        aptRect[3].x = ptUpperLeft.x; 
        aptRect[3].y = ptLowerRight.y; 
        aptRect[4].x = aptRect[0].x; 
        aptRect[4].y = aptRect[0].y; 
 
        if (!Polyline(hdc, (CONST POINT *) aptRect, 5)) 
             errhandler("Polyline Failed", hwnd); 
 
        ReleaseDC(hwnd, hdc); 
    } 
    break; 
```



 

 
