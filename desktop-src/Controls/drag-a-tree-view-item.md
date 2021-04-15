---
title: Ziehen eines Tree-View Elements
description: In diesem Thema wird der Code für die Behandlung von Drag & Drop von Struktur Ansichts Elementen veranschaulicht.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cedc5f7ec750270ec5d9fb6f567bf473f8c13b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474477"
---
# <a name="how-to-drag-a-tree-view-item"></a>Ziehen eines Tree-View Elements

In diesem Thema wird der Code für die Behandlung von Drag & Drop von Struktur Ansichts Elementen veranschaulicht. Der Beispielcode besteht aus drei Funktionen. Die erste Funktion startet den Zieh Vorgang, die zweite Funktion zieht das Bild, und die dritte Funktion beendet den Zieh Vorgang.

> [!Note]  
> Das Ziehen eines Struktur Ansichts Elements umfasst in der Regel die Verarbeitung der [TVN \_ BeginDrag](tvn-begindrag.md) (oder [TVN \_ beginrdrag](tvn-beginrdrag.md))-Benachrichtigungs Codes, der [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Meldung und der [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldung (oder der [**WM- \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup)). Es umfasst auch die Verwendung der [Bildlisten](image-lists.md) Funktionen, um das Element zu zeichnen, wenn es gezogen wird.

 

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Schritt 1: Starten des Struktur Ansichts Zieh Vorgangs

Ein Strukturansicht-Steuerelement sendet das übergeordnete Fenster, wenn der Benutzer mit dem Ziehen eines Elements beginnt, eine [TVN \_ BeginDrag](tvn-begindrag.md) (oder [TVN \_ beginrdrag](tvn-beginrdrag.md))-Benachrichtigungs Code. Das übergeordnete Fenster empfängt die Benachrichtigung in Form einer WM-Benachrichtigungs Meldung, deren *LPARAM* -Parameter die Adresse einer [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur ist. [**\_**](wm-notify.md) Die Member dieser Struktur enthalten die Bildschirm Koordinaten des Mauszeigers und eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die Informationen über das Element enthält, das gezogen werden soll.

Im folgenden Beispiel wird gezeigt, wie die [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung zum Abrufen von [TVN \_ BeginDrag](tvn-begindrag.md)verarbeitet wird.


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



Das Starten des Zieh Vorgangs umfasst die Verwendung der [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) -Funktion. Die Parameter der Funktion enthalten das Handle für die Bildliste, das das Bild enthält, das während des Zieh Vorgangs und den Index des Bilds verwendet werden soll. Sie können entweder Ihre eigene Bildliste und Ihr Image bereitstellen, oder Sie können das Strukturansicht-Steuerelement erstellen, indem Sie die [**TVM-Nachricht " \_ fiatedragimage**](tvm-createdragimage.md) " verwenden.

Da das Zieh Bild den Mauszeiger für die Dauer des Zieh Vorgangs ersetzt, erfordert [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) , dass Sie einen Hot-Spot innerhalb des Bilds angeben müssen. Die Koordinaten des Hotspots sind relativ zur linken oberen Ecke des Bilds. **ImageList \_ BeginDrag** erfordert auch, dass Sie den ursprünglichen Speicherort des Zieh Bilds angeben. Eine Anwendung legt in der Regel den ursprünglichen Speicherort fest, sodass der Hotspot des Zieh Bilds dem Mauszeiger zu dem Zeitpunkt entspricht, an dem der Benutzer den Zieh Vorgang gestartet hat.

Die folgende Funktion veranschaulicht, wie mit dem Ziehen eines Struktur Ansichts Elements begonnen wird. Er verwendet das Zieh Bild, das vom Strukturansicht-Steuerelement bereitgestellt wird, und ruft das umgebende Rechteck des Elements ab, um den entsprechenden Punkt für den Hotspot zu ermitteln. Die Dimensionen des umgebenden Rechtecks sind identisch mit denen des Bilds.

Die Funktion erfasst Maus Eingaben und bewirkt, dass Maus Meldungen an das übergeordnete Fenster gesendet werden. Das übergeordnete Fenster benötigt die nachfolgenden [**WM- \_ mouposimove**](/windows/desktop/inputdev/wm-mousemove) -Meldungen, um zu bestimmen, wohin das Bild gezogen werden soll, und die [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldung, um zu bestimmen, wann der Zieh Vorgang beendet


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



### <a name="step-2-dragging-the-tree-view-item"></a>Schritt 2: Ziehen des Struktur Ansichts Elements

Sie ziehen ein Struktur Ansichts Element, indem Sie die [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) -Funktion aufrufen, wenn das übergeordnete Fenster eine [**WM- \_ mousetmove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht empfängt, wie im folgenden Beispiel gezeigt. Das Beispiel veranschaulicht auch das Ausführen von Treffer Tests während des Zieh Vorgangs, um zu bestimmen, ob andere Elemente in der Strukturansicht als Ziele eines Drag & Drop-Vorgangs hervorgehoben werden sollen.


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Schritt 3: Beenden des Struktur Ansichts Zieh Vorgangs

Im folgenden Beispiel wird gezeigt, wie ein Zieh Vorgang beendet wird. Die [**ImageList- \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) -Funktion wird aufgerufen, wenn das übergeordnete Fenster eine [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldung empfängt. Das Handle des Strukturansicht-Steuer Elements wird an die Funktion übermittelt.


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

[Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 