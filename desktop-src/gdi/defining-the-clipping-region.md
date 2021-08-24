---
description: Wenn der Benutzer auf Clipbereich definieren klickt, gibt das System eine WM \_ COMMAND-Meldung aus.
ms.assetid: 4b20f310-98c0-42c1-b3b3-eadf9bb2003c
title: Definieren des Ausschneidebereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa56c2eb036430b90e3c8f7b6fc0894abdc37306edef77438afae796cb1cc04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115310"
---
# <a name="defining-the-clipping-region"></a>Definieren des Ausschneidebereichs

Wenn der Benutzer auf Clipbereich definieren klickt, gibt das System eine [**WM \_ COMMAND-Meldung**](../menurc/wm-command.md) aus. Der *wParam-Parameter* dieser Nachricht enthält eine anwendungsdefinierte Konstante IDM \_ DEFINE, die angibt, dass der Benutzer diese Option im Menü ausgewählt hat. Die Anwendung verarbeitet diese Eingabe durch Festlegen des booleschen Flags fDefineRegion, wie im folgenden Codebeispiel gezeigt.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
 
        case IDM_DEFINE: 
            fDefineRegion = TRUE; 
            break; 
```



Nach dem Klicken auf **Clippingbereich definieren** kann der Benutzer mit dem Zeichnen des Rechtecks beginnen, indem er klickt und die Maus zieht, während sich der Cursor im Clientbereich der Anwendung befindet.

Wenn der Benutzer die linke Schaltfläche drückt, gibt das System eine [**\_ WM-LBUTTONDOWN-Meldung**](../inputdev/wm-lbuttondown.md) aus. Der *lParam-Parameter* dieser Nachricht enthält die Cursorkoordinaten, die der oberen linken Ecke eines Rechtecks entsprechen, das zum Definieren des Ausschneidebereichs verwendet wird. Die Anwendung verarbeitet die **\_ WM-LBUTTONDOWN-Nachricht** wie folgt.


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



Wenn der Benutzer die Maus zieht, gibt das System [**WM \_ MOUSEMOVE-Meldungen**](../inputdev/wm-mousemove.md) aus und speichert die neuen Cursorkoordinaten im *lParam-Parameter.* Jedes Mal, wenn die Anwendung eine neue **WM \_ MOUSEMOVE-Nachricht** empfängt, löscht sie das vorherige Rechteck (sofern vorhanden) und zeichnet das neue Rechteck, indem sie die [**Polyline-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) aufruft und die Koordinaten der vier Ecken des Rechtecks übergibt. Die Anwendung führt die folgenden Aufgaben aus.


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



 

 
