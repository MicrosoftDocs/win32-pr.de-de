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
# <a name="how-to-drag-a-tree-view-item"></a><span data-ttu-id="05c8c-103">Ziehen eines Tree-View Elements</span><span class="sxs-lookup"><span data-stu-id="05c8c-103">How to Drag a Tree-View Item</span></span>

<span data-ttu-id="05c8c-104">In diesem Thema wird der Code für die Behandlung von Drag & Drop von Struktur Ansichts Elementen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="05c8c-104">This topic demonstrates code for handling dragging and dropping of tree-view items.</span></span> <span data-ttu-id="05c8c-105">Der Beispielcode besteht aus drei Funktionen.</span><span class="sxs-lookup"><span data-stu-id="05c8c-105">The sample code consists of three functions.</span></span> <span data-ttu-id="05c8c-106">Die erste Funktion startet den Zieh Vorgang, die zweite Funktion zieht das Bild, und die dritte Funktion beendet den Zieh Vorgang.</span><span class="sxs-lookup"><span data-stu-id="05c8c-106">The first function begins the drag operation, the second function drags the image, and the third function ends the drag operation.</span></span>

> [!Note]  
> <span data-ttu-id="05c8c-107">Das Ziehen eines Struktur Ansichts Elements umfasst in der Regel die Verarbeitung der [TVN \_ BeginDrag](tvn-begindrag.md) (oder [TVN \_ beginrdrag](tvn-beginrdrag.md))-Benachrichtigungs Codes, der [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Meldung und der [**WM- \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldung (oder der [**WM- \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup)).</span><span class="sxs-lookup"><span data-stu-id="05c8c-107">Dragging a tree-view item typically involves processing the [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code, the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (or [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) message.</span></span> <span data-ttu-id="05c8c-108">Es umfasst auch die Verwendung der [Bildlisten](image-lists.md) Funktionen, um das Element zu zeichnen, wenn es gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="05c8c-108">It also involves using the [Image Lists](image-lists.md) functions to draw the item as it is being dragged.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="05c8c-109">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="05c8c-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="05c8c-110">Technologien</span><span class="sxs-lookup"><span data-stu-id="05c8c-110">Technologies</span></span>

-   [<span data-ttu-id="05c8c-111">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="05c8c-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="05c8c-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="05c8c-112">Prerequisites</span></span>

-   <span data-ttu-id="05c8c-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="05c8c-113">C/C++</span></span>
-   <span data-ttu-id="05c8c-114">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="05c8c-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="05c8c-115">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="05c8c-115">Instructions</span></span>

### <a name="step-1-beginning-the-tree-view-drag-operation"></a><span data-ttu-id="05c8c-116">Schritt 1: Starten des Struktur Ansichts Zieh Vorgangs</span><span class="sxs-lookup"><span data-stu-id="05c8c-116">Step 1: Beginning the tree-view drag operation</span></span>

<span data-ttu-id="05c8c-117">Ein Strukturansicht-Steuerelement sendet das übergeordnete Fenster, wenn der Benutzer mit dem Ziehen eines Elements beginnt, eine [TVN \_ BeginDrag](tvn-begindrag.md) (oder [TVN \_ beginrdrag](tvn-beginrdrag.md))-Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="05c8c-117">A tree-view control sends the parent window a [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code whenever the user starts to drag an item.</span></span> <span data-ttu-id="05c8c-118">Das übergeordnete Fenster empfängt die Benachrichtigung in Form einer WM-Benachrichtigungs Meldung, deren *LPARAM* -Parameter die Adresse einer [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur ist. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="05c8c-118">The parent window receives the notification in the form of a [**WM\_NOTIFY**](wm-notify.md) message whose *lParam* parameter is the address of an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="05c8c-119">Die Member dieser Struktur enthalten die Bildschirm Koordinaten des Mauszeigers und eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die Informationen über das Element enthält, das gezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="05c8c-119">The members of this structure include the screen coordinates of the mouse pointer and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains information about the item to be dragged.</span></span>

<span data-ttu-id="05c8c-120">Im folgenden Beispiel wird gezeigt, wie die [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung zum Abrufen von [TVN \_ BeginDrag](tvn-begindrag.md)verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="05c8c-120">The following example shows how to process the [**WM\_NOTIFY**](wm-notify.md) message to obtain [TVN\_BEGINDRAG](tvn-begindrag.md).</span></span>


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



<span data-ttu-id="05c8c-121">Das Starten des Zieh Vorgangs umfasst die Verwendung der [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="05c8c-121">Beginning the drag operation involves using the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function.</span></span> <span data-ttu-id="05c8c-122">Die Parameter der Funktion enthalten das Handle für die Bildliste, das das Bild enthält, das während des Zieh Vorgangs und den Index des Bilds verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="05c8c-122">The function's parameters include the handle to the image list that contains the image to use during the drag operation and the index of the image.</span></span> <span data-ttu-id="05c8c-123">Sie können entweder Ihre eigene Bildliste und Ihr Image bereitstellen, oder Sie können das Strukturansicht-Steuerelement erstellen, indem Sie die [**TVM-Nachricht " \_ fiatedragimage**](tvm-createdragimage.md) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="05c8c-123">You can either provide your own image list and image, or you can have the tree-view control create them for you by using the [**TVM\_CREATEDRAGIMAGE**](tvm-createdragimage.md) message.</span></span>

<span data-ttu-id="05c8c-124">Da das Zieh Bild den Mauszeiger für die Dauer des Zieh Vorgangs ersetzt, erfordert [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) , dass Sie einen Hot-Spot innerhalb des Bilds angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="05c8c-124">Because the drag image replaces the mouse pointer for the duration of the drag operation, [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requires you to specify a hot spot within the image.</span></span> <span data-ttu-id="05c8c-125">Die Koordinaten des Hotspots sind relativ zur linken oberen Ecke des Bilds.</span><span class="sxs-lookup"><span data-stu-id="05c8c-125">The coordinates of the hot spot are relative to the upper left corner of the image.</span></span> <span data-ttu-id="05c8c-126">**ImageList \_ BeginDrag** erfordert auch, dass Sie den ursprünglichen Speicherort des Zieh Bilds angeben.</span><span class="sxs-lookup"><span data-stu-id="05c8c-126">**ImageList\_BeginDrag** also requires you to specify the initial location of the drag image.</span></span> <span data-ttu-id="05c8c-127">Eine Anwendung legt in der Regel den ursprünglichen Speicherort fest, sodass der Hotspot des Zieh Bilds dem Mauszeiger zu dem Zeitpunkt entspricht, an dem der Benutzer den Zieh Vorgang gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="05c8c-127">An application typically sets the initial location so that the hot spot of the drag image corresponds to that of the mouse pointer at the time the user began the drag operation.</span></span>

<span data-ttu-id="05c8c-128">Die folgende Funktion veranschaulicht, wie mit dem Ziehen eines Struktur Ansichts Elements begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="05c8c-128">The following function demonstrates how to begin dragging a tree-view item.</span></span> <span data-ttu-id="05c8c-129">Er verwendet das Zieh Bild, das vom Strukturansicht-Steuerelement bereitgestellt wird, und ruft das umgebende Rechteck des Elements ab, um den entsprechenden Punkt für den Hotspot zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="05c8c-129">It uses the drag image provided by the tree-view control and obtains the bounding rectangle of the item to determine the appropriate point for the hot spot.</span></span> <span data-ttu-id="05c8c-130">Die Dimensionen des umgebenden Rechtecks sind identisch mit denen des Bilds.</span><span class="sxs-lookup"><span data-stu-id="05c8c-130">The dimensions of the bounding rectangle are the same as those of the image.</span></span>

<span data-ttu-id="05c8c-131">Die Funktion erfasst Maus Eingaben und bewirkt, dass Maus Meldungen an das übergeordnete Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="05c8c-131">The function captures mouse input, causing mouse messages to be sent to the parent window.</span></span> <span data-ttu-id="05c8c-132">Das übergeordnete Fenster benötigt die nachfolgenden [**WM- \_ mouposimove**](/windows/desktop/inputdev/wm-mousemove) -Meldungen, um zu bestimmen, wohin das Bild gezogen werden soll, und die [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldung, um zu bestimmen, wann der Zieh Vorgang beendet</span><span class="sxs-lookup"><span data-stu-id="05c8c-132">The parent window needs the subsequent [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to determine where to drag the image and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message to determine when to end the drag operation.</span></span>


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



### <a name="step-2-dragging-the-tree-view-item"></a><span data-ttu-id="05c8c-133">Schritt 2: Ziehen des Struktur Ansichts Elements</span><span class="sxs-lookup"><span data-stu-id="05c8c-133">Step 2: Dragging the tree-view item</span></span>

<span data-ttu-id="05c8c-134">Sie ziehen ein Struktur Ansichts Element, indem Sie die [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) -Funktion aufrufen, wenn das übergeordnete Fenster eine [**WM- \_ mousetmove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht empfängt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="05c8c-134">You drag a tree-view item by calling the [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function when the parent window receives a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, as the following example shows.</span></span> <span data-ttu-id="05c8c-135">Das Beispiel veranschaulicht auch das Ausführen von Treffer Tests während des Zieh Vorgangs, um zu bestimmen, ob andere Elemente in der Strukturansicht als Ziele eines Drag & Drop-Vorgangs hervorgehoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="05c8c-135">The example also demonstrates how to perform hit testing during the drag operation to determine whether to highlight other items in the tree view as targets of a drag-and-drop operation.</span></span>


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a><span data-ttu-id="05c8c-136">Schritt 3: Beenden des Struktur Ansichts Zieh Vorgangs</span><span class="sxs-lookup"><span data-stu-id="05c8c-136">Step 3: Ending the tree-view drag operation</span></span>

<span data-ttu-id="05c8c-137">Im folgenden Beispiel wird gezeigt, wie ein Zieh Vorgang beendet wird.</span><span class="sxs-lookup"><span data-stu-id="05c8c-137">The following example shows how to end a drag operation.</span></span> <span data-ttu-id="05c8c-138">Die [**ImageList- \_ EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) -Funktion wird aufgerufen, wenn das übergeordnete Fenster eine [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="05c8c-138">The [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function is called when the parent window receives a [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message.</span></span> <span data-ttu-id="05c8c-139">Das Handle des Strukturansicht-Steuer Elements wird an die Funktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="05c8c-139">The handle of the tree-view control is passed to the function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="05c8c-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05c8c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05c8c-141">Verwenden von Tree-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="05c8c-141">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="05c8c-142">Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="05c8c-142">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 