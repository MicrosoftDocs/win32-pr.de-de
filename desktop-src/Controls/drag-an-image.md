---
title: Vorgehensweise beim Ziehen eines Bilds
description: In diesem Thema wird veranschaulicht, wie Sie ein Bild auf dem Bildschirm ziehen. Die Zieh Funktionen verschieben ein Bild reibungslos, in Farbe und ohne Blinken des Cursors. Sowohl maskierte als auch unmaskierte Bilder können gezogen werden.
ms.assetid: 84AFA770-F495-4312-9631-3335BA8CC799
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da495ef9ee0895c04a856f456fcda3e3125f2957
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730665"
---
# <a name="how-to-drag-an-image"></a>Vorgehensweise beim Ziehen eines Bilds

In diesem Thema wird veranschaulicht, wie Sie ein Bild auf dem Bildschirm ziehen. Die Zieh Funktionen verschieben ein Bild reibungslos, in Farbe und ohne Blinken des Cursors. Sowohl maskierte als auch unmaskierte Bilder können gezogen werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="step-1-begin-the-drag-operation"></a>Schritt 1: Starten Sie den Zieh Vorgang.

Verwenden Sie die " [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) "-Funktion, um einen Zieh Vorgang zu starten.

Die benutzerdefinierte Funktion im folgenden C++-Codebeispiel soll als Antwort auf eine Maustaste aufgerufen werden, z. b. [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown). Die-Funktion bestimmt, ob der Benutzer innerhalb des umgebenden Rechtecks des Bilds geklickt hat. Wenn auf den Benutzer geklickt hat, erfasst die Funktion die Maus Eingaben, löscht das Bild aus dem Client Bereich und berechnet die Position für den Hotspot innerhalb des Bilds. Die-Funktion legt den Hotspot fest, sodass er mit der Hotspot Position des Mauszeigers übereinstimmt. Anschließend beginnt die Funktion den Zieh Vorgang durch Aufrufen von [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).


```C++
// StartDragging - begins dragging a bitmap. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// ptCur - coordinates of the cursor. 
// himl - handle to the image list. 
// 
// Global variables 
//     g_rcImage - bounding rectangle of the image to drag. 
//     g_nImage - index of the image. 
//     g_ptHotSpot - location of the image's hot spot. 
//     g_cxBorder and g_cyBorder - width and height of border. 
//     g_cyCaption and g_cyMenu - height of title bar and menu bar. 
extern RECT g_rcImage; 
extern int g_nImage; 
extern POINT g_ptHotSpot; 
 
BOOL StartDragging(HWND hwnd, POINT ptCur, HIMAGELIST himl) 
{ 
    // Return if the cursor is not in the bounding rectangle of 
    // the image. 
    if (!PtInRect(&g_rcImage, ptCur)) 
        return FALSE; 
 
    // Capture the mouse input. 
    SetCapture(hwnd); 
 
    // Erase the image from the client area. 
    InvalidateRect(hwnd, &g_rcImage, TRUE); 
    UpdateWindow(hwnd); 
 
    // Calculate the location of the hot spot, and save it. 
    g_ptHotSpot.x = ptCur.x - g_rcImage.left; 
    g_ptHotSpot.y = ptCur.y - g_rcImage.top; 
 
    // Begin the drag operation. 
    if (!ImageList_BeginDrag(himl, g_nImage, 
            g_ptHotSpot.x, g_ptHotSpot.y)) 
        return FALSE; 
 
    // Set the initial location of the image, and make it visible. 
    // Because the ImageList_DragEnter function expects coordinates to 
    // be relative to the upper-left corner of the given window, the 
    // width of the border, title bar, and menu bar need to be taken 
    // into account. 
    
    ImageList_DragEnter(hwnd, ptCur.x + g_cxBorder, 
        ptCur.y + g_cyBorder + g_cyCaption + g_cyMenu); 
 
    g_fDragging = TRUE; 
 
    return TRUE; 
} 
```



### <a name="step-2-move-the-image"></a>Schritt 2: Verschieben des Bilds.

Mit der [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) -Funktion wird das Bild an einen neuen Speicherort verschoben.

Die benutzerdefinierte Funktion im folgenden C++-Codebeispiel soll als Antwort auf die [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht aufgerufen werden. Er zieht das Bild an einen neuen Speicherort.


```C++
// MoveTheImage - drags an image to the specified coordinates. 
// Returns TRUE if successful, or FALSE otherwise. 
// ptCur - new coordinates for the image. 
BOOL MoveTheImage(POINT ptCur) 
{ 
    if (!ImageList_DragMove(ptCur.x, ptCur.y)) 
        return FALSE; 
 
    return TRUE; 
} 

```



### <a name="step-3-end-the-drag-operation"></a>Schritt 3: Beenden Sie den Zieh Vorgang.

Die benutzerdefinierte Funktion im folgenden C++-Codebeispiel ruft die [**ImageList- \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) -Funktion auf, um den Zieh Vorgang zu beenden. Anschließend wird die [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) -Funktion aufgerufen, um das Fenster zu entsperren und das Zieh Bild auszublenden, sodass das Fenster aktualisiert werden kann.


```C++
// StopDragging - ends a drag operation and draws the image 
// at its final location. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// himl - handle to the image list. 
// ptCur - coordinates of the cursor. 
// 
// Global variable 
//     g_ptHotSpot - location of the image's hot spot. 
 
extern POINT g_ptHotSpot; 
 
BOOL StopDragging(HWND hwnd, HIMAGELIST himl, POINT ptCur) 
{ 
    ImageList_EndDrag(); 
    ImageList_DragLeave(hwnd); 
 
    g_fDragging = FALSE; 
 
    DrawTheImage(hwnd, himl, ptCur.x - g_ptHotSpot.x, 
        ptCur.y - g_ptHotSpot.y); 
 
    ReleaseCapture(); 
    return TRUE; 
} 

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Bildlisten](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Informationen zu Bildlisten](image-lists.md)
</dt> <dt>

[Verwenden von Bildlisten](using-image-lists.md)
</dt> </dl>

 

 