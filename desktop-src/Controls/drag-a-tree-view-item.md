---
title: Ziehen eines Tree-View Elements
description: In diesem Thema wird Code für das Ziehen und Ablegen von Strukturansichtselementen veranschaulicht.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ee7cfc9d4fa7a6e73abd042df583ae9175de8583b050ff9621b7d2789e0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413114"
---
# <a name="how-to-drag-a-tree-view-item"></a>Ziehen eines Tree-View Elements

In diesem Thema wird Code für das Ziehen und Ablegen von Strukturansichtselementen veranschaulicht. Der Beispielcode besteht aus drei Funktionen. Die erste Funktion startet den Ziehvorgang, die zweite Funktion zieht das Bild, und die dritte Funktion beendet den Ziehvorgang.

> [!Note]  
> Das Ziehen eines Strukturansichtselements umfasst in der Regel die Verarbeitung des [TVN \_ BEGINDRAG-Benachrichtigungscodes](tvn-begindrag.md) (oder [TVN \_ BEGINRDRAG),](tvn-beginrdrag.md)der [**WM \_ MOUSEMOVE-Nachricht**](/windows/desktop/inputdev/wm-mousemove) und der [**\_ WM-LBUTTONUP-Nachricht**](/windows/desktop/inputdev/wm-lbuttonup) (oder [**WM \_ RBUTTONUP).**](/windows/desktop/inputdev/wm-rbuttonup) Es umfasst auch die Verwendung der [Bildlistenfunktionen,](image-lists.md) um das Element zu zeichnen, während es gezogen wird.

 

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Schritt 1: Beginnen des Strukturansichts-Ziehvorgang

Ein Strukturansicht-Steuerelement sendet dem übergeordneten Fenster immer dann einen [TVN \_ BEGINDRAG-Benachrichtigungscode](tvn-begindrag.md) (oder [TVN \_ BEGINRDRAG),](tvn-beginrdrag.md)wenn der Benutzer beginnt, ein Element zu ziehen. Das übergeordnete Fenster empfängt die Benachrichtigung in Form einer [**WM \_ NOTIFY-Nachricht,**](wm-notify.md) deren *lParam-Parameter* die Adresse einer [**NMTREEVIEW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) ist. Zu den Membern dieser Struktur gehören die Bildschirmkoordinaten des Mauszeigers und eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die Informationen über das zu ziehende Element enthält.

Das folgende Beispiel zeigt, wie sie die [**WM \_ NOTIFY-Nachricht**](wm-notify.md) verarbeiten, um [TVN \_ BEGINDRAG zu erhalten.](tvn-begindrag.md)


```C++
    case WM_NOTIFY: 
        switch (((LPNMHDR)lParam)->code) 
        {
            case TVN_BEGINDRAG:
                Main_OnBeginDrag(((LPNMHDR)lParam)->hwndFrom, (LPNMTREEVIEW)lParam);
                break;
        
            // Handle other cases here. 
        }
        break; 
```



Zum Starten des Ziehvorgang wird die [**Funktion ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) verwendet. Die Parameter der Funktion enthalten das Handle für die Bildliste, die das während des Ziehvorgang zu verwendende Bild enthält, und den Index des Bilds. Sie können entweder eine eigene Bildliste und ein eigenes Bild bereitstellen, oder Sie können das Strukturansicht-Steuerelement mithilfe der [**TVM \_ CREATEDRAGIMAGE-Meldung**](tvm-createdragimage.md) erstellen lassen.

Da das Ziehbild den Mauszeiger für die Dauer des Ziehvorgang ersetzt, müssen Sie für [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) einen Hotspot im Bild angeben. Die Koordinaten des Hotspots sind relativ zur oberen linken Ecke des Bilds. **ImageList \_ BeginDrag erfordert** auch, dass Sie die Anfangsposition des Ziehbilds angeben. Eine Anwendung legt in der Regel die Anfangsposition so fest, dass der Hotspot des Ziehbilds dem des Mauszeigers zum Zeitpunkt entspricht, zu dem der Benutzer den Ziehvorgang begonnen hat.

Die folgende Funktion veranschaulicht, wie mit dem Ziehen eines Strukturansichtselements begonnen wird. Es verwendet das vom Strukturansicht-Steuerelement bereitgestellte Ziehbild und erhält das umgebundene Rechteck des Elements, um den entsprechenden Punkt für den Hotspot zu bestimmen. Die Abmessungen des umgebundenen Rechtecks sind mit denen des Bilds identisch.

Die Funktion erfasst Mauseingaben und führt dazu, dass Mausnachrichten an das übergeordnete Fenster gesendet werden. Das übergeordnete Fenster benötigt die nachfolgenden [**WM \_ MOUSEMOVE-Meldungen,**](/windows/desktop/inputdev/wm-mousemove) um zu bestimmen, wo das Bild ziehbar ist, und die [**WM \_ LBUTTONUP-Meldung,**](/windows/desktop/inputdev/wm-lbuttonup) um zu bestimmen, wann der Ziehvorgang beendet werden soll.


```C++
// Begin dragging an item in a tree-view control. 
// hwndTV - handle to the image list. 
// lpnmtv - address of information about the item being dragged.
//
// g_fDragging -- global BOOL that specifies whether dragging is underway.

void Main_OnBeginDrag(HWND hwndTV, LPNMTREEVIEW lpnmtv)
{ 
    HIMAGELIST himl;    // handle to image list 
    RECT rcItem;        // bounding rectangle of item 

    // Tell the tree-view control to create an image to use 
    // for dragging. 
    himl = TreeView_CreateDragImage(hwndTV, lpnmtv->itemNew.hItem); 

    // Get the bounding rectangle of the item being dragged. 
    TreeView_GetItemRect(hwndTV, lpnmtv->itemNew.hItem, &rcItem, TRUE); 

    // Start the drag operation. 
    ImageList_BeginDrag(himl, 0, 0, 0);
    ImageList_DragEnter(hwndTV, lpnmtv->ptDrag.x, lpnmtv->ptDrag.x); 

    // Hide the mouse pointer, and direct mouse input to the 
    // parent window. 
    ShowCursor(FALSE); 
    SetCapture(GetParent(hwndTV)); 
    g_fDragging = TRUE; 

    return; 

} 
```



### <a name="step-2-dragging-the-tree-view-item"></a>Schritt 2: Ziehen des Strukturansichtselements

Sie ziehen ein Strukturansichtselement, indem Sie die [**\_ Funktion ImageList DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) aufrufen, wenn das übergeordnete Fenster eine [**WM \_ MOUSEMOVE-Meldung**](/windows/desktop/inputdev/wm-mousemove) empfängt, wie im folgenden Beispiel gezeigt. Im Beispiel wird auch veranschaulicht, wie Treffertests während des Ziehvorganges durchgeführt werden, um zu bestimmen, ob andere Elemente in der Strukturansicht als Ziele eines Drag & Drop-Vorgangs hervorhebt werden sollen.


```C++
// Drag an item in a tree-view control, 
// highlighting the item that is the target. 
// hwndParent - handle to the parent window. 
// hwndTV - handle to the tree-view control.
// xCur and yCur - coordinates of the mouse pointer,
//     relative to the parent window. 
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnMouseMove(HWND hwndParent, HWND hwndTV, LONG xCur, LONG yCur) 
{ 
    HTREEITEM htiTarget;  // Handle to target item. 
    TVHITTESTINFO tvht;   // Hit test information. 

    if (g_fDragging) 
    { 
       // Drag the item to the current position of the mouse pointer. 
       // First convert the dialog coordinates to control coordinates. 
       POINT point;
       point.x = xCur;
       point.y = yCur;
       ClientToScreen(hwndParent, &point);
       ScreenToClient(hwndTV, &point);
       ImageList_DragMove(point.x, point.y);
       // Turn off the dragged image so the background can be refreshed.
       ImageList_DragShowNolock(FALSE); 
                
        // Find out if the pointer is on the item. If it is, 
        // highlight the item as a drop target. 
        tvht.pt.x = point.x; 
        tvht.pt.y = point.y; 
        if ((htiTarget = TreeView_HitTest(hwndTV, &tvht)) != NULL) 
        { 
            TreeView_SelectDropTarget(hwndTV, htiTarget); 
        } 
        ImageList_DragShowNolock(TRUE);
    } 
    return; 
}
```



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Schritt 3: Beenden des Strukturansicht-Ziehvorgang

Das folgende Beispiel zeigt, wie ein Ziehvorgang beendet wird. Die [**ImageList \_ EndDrag-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) wird aufgerufen, wenn das übergeordnete Fenster eine [**\_ WM-LBUTTONUP-Nachricht empfängt.**](/windows/desktop/inputdev/wm-lbuttonup) Das Handle des Strukturansicht-Steuerelements wird an die Funktion übergeben.


```C++
// Stops dragging a tree-view item, releases the 
// mouse capture, and shows the mouse pointer.
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnLButtonUp(HWND hwndTV) 
{ 
    if (g_fDragging) 
    { 
        // Get destination item.
        HTREEITEM htiDest = TreeView_GetDropHilight(hwndTV);
        if (htiDest != NULL)
        {
            // To do: handle the actual moving of the dragged node.
        }
        ImageList_EndDrag(); 
        TreeView_SelectDropTarget(hwndTV, NULL);
        ReleaseCapture(); 
        ShowCursor(TRUE); 
        g_fDragging = FALSE; 
    } 
    return; 
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Tree-View Steuerelementen](using-treeview.md)
</dt> <dt>

[CustDTv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 