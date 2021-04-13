---
title: Vorgehensweise beim Hinzufügen von Tree-View Elementen
description: Sie fügen ein Element zu einem Strukturansicht-Steuerelement hinzu, indem Sie die TVM \_ InsertItem-Meldung an das Steuerelement senden.
ms.assetid: CD6376F4-8B1A-489D-8538-6C1620E98F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7da0846b57f422de83984b197df0770286882
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389938"
---
# <a name="how-to-add-tree-view-items"></a><span data-ttu-id="3db15-103">Vorgehensweise beim Hinzufügen von Tree-View Elementen</span><span class="sxs-lookup"><span data-stu-id="3db15-103">How to Add Tree-View Items</span></span>

<span data-ttu-id="3db15-104">Sie fügen ein Element zu einem Strukturansicht-Steuerelement hinzu, indem Sie die [**TVM \_ InsertItem**](tvm-insertitem.md) -Meldung an das Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="3db15-104">You add an item to a tree-view control by sending the [**TVM\_INSERTITEM**](tvm-insertitem.md) message to the control.</span></span> <span data-ttu-id="3db15-105">Die Nachricht enthält die Adresse einer [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) -Struktur, die das übergeordnete Element, das Element, nach dem das neue Element eingefügt wird, und eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die die Attribute des Elements definiert, angibt.</span><span class="sxs-lookup"><span data-stu-id="3db15-105">The message includes the address of a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure, specifying the parent item, the item after which the new item is inserted, and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that defines the attributes of the item.</span></span> <span data-ttu-id="3db15-106">Die Attribute enthalten die Bezeichnung des Elements, die ausgewählten und nicht ausgewählten Images sowie einen von der 32-Bit-Anwendung definierten Wert.</span><span class="sxs-lookup"><span data-stu-id="3db15-106">The attributes include the item's label, its selected and nonselected images, and a 32-bit application-defined value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3db15-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="3db15-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3db15-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="3db15-108">Technologies</span></span>

-   [<span data-ttu-id="3db15-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3db15-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3db15-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3db15-110">Prerequisites</span></span>

-   <span data-ttu-id="3db15-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="3db15-111">C/C++</span></span>
-   <span data-ttu-id="3db15-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="3db15-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3db15-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="3db15-113">Instructions</span></span>

### <a name="add-items-to-the-tree-view"></a><span data-ttu-id="3db15-114">Hinzufügen von Elementen zum Tree-View</span><span class="sxs-lookup"><span data-stu-id="3db15-114">Add Items to the Tree-View</span></span>

<span data-ttu-id="3db15-115">Im Beispiel in diesem Abschnitt wird veranschaulicht, wie ein Inhaltsverzeichnis auf der Grundlage von Dokumenten Überschriften Informationen erstellt wird, die in einem Anwendungs definierten Array bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3db15-115">The example in this section demonstrates how to create a table of contents based on document heading information that is provided in an application-defined array.</span></span> <span data-ttu-id="3db15-116">Jedes Array Element besteht aus einer Überschriften Zeichenfolge und einer ganzen Zahl, die die Überschriftenebene angibt.</span><span class="sxs-lookup"><span data-stu-id="3db15-116">Each array element consists of a heading string and an integer that indicates the heading level.</span></span> <span data-ttu-id="3db15-117">Das Beispiel unterstützt drei Überschriften Ebenen (1, 2 und 3).</span><span class="sxs-lookup"><span data-stu-id="3db15-117">The example supports three heading levels (1, 2, and 3).</span></span>

<span data-ttu-id="3db15-118">Das Beispiel enthält zwei Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3db15-118">The example includes two functions.</span></span> <span data-ttu-id="3db15-119">Die erste Funktion extrahiert jede Überschrift und die zugehörige Überschriftenebene und übergibt sie an die zweite Funktion.</span><span class="sxs-lookup"><span data-stu-id="3db15-119">The first function extracts each heading and accompanying heading level and then passes them to the second function.</span></span>

<span data-ttu-id="3db15-120">Die zweite Funktion fügt ein Element zu einem Strukturansicht-Steuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="3db15-120">The second function adds an item to a tree-view control.</span></span> <span data-ttu-id="3db15-121">Er verwendet den Überschriften Text als Bezeichnung des Elements und verwendet die Überschriftenebene, um das übergeordnete Element für das neue Element zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3db15-121">It uses the heading text as the item's label, and it uses the heading level to determine the parent item for the new item.</span></span> <span data-ttu-id="3db15-122">Eine Überschrift der Ebene 1 wird dem Stamm des Strukturansicht-Steuer Elements hinzugefügt, eine Überschrift der Ebene 2 wird als untergeordnetes Element der vorherigen Ebene eines Elements hinzugefügt usw.</span><span class="sxs-lookup"><span data-stu-id="3db15-122">A level one heading is added to the root of the tree-view control, a level two heading is added as a child item of the previous level one item, and so on.</span></span> <span data-ttu-id="3db15-123">Die-Funktion weist ein Bild einem Element zu, je nachdem, ob es über untergeordnete Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="3db15-123">The function assigns an image to an item based on whether it has child items.</span></span> <span data-ttu-id="3db15-124">Wenn ein Element über untergeordnete Elemente verfügt, wird ein Bild abgerufen, das einen geschlossenen Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="3db15-124">If an item has child items, it gets an image that represents a closed folder.</span></span> <span data-ttu-id="3db15-125">Andernfalls wird ein Bild abgerufen, das ein Dokument darstellt.</span><span class="sxs-lookup"><span data-stu-id="3db15-125">Otherwise, it gets an image that represents a document.</span></span> <span data-ttu-id="3db15-126">Ein Element verwendet dasselbe Bild für den ausgewählten und den nicht ausgewählten Zustand.</span><span class="sxs-lookup"><span data-stu-id="3db15-126">An item uses the same image for both the selected and nonselected states.</span></span>


```C++
// Adds items to a tree-view control. 
// Returns the handle to the newly added item. 
// hwndTV - handle to the tree-view control. 
// lpszItem - text of the item to add. 
// nLevel - level at which to add the item. 
//
// g_nClosed, and g_nDocument - global indexes of the images.

HTREEITEM AddItemToTree(HWND hwndTV, LPTSTR lpszItem, int nLevel)
{ 
    TVITEM tvi; 
    TVINSERTSTRUCT tvins; 
    static HTREEITEM hPrev = (HTREEITEM)TVI_FIRST; 
    static HTREEITEM hPrevRootItem = NULL; 
    static HTREEITEM hPrevLev2Item = NULL; 
    HTREEITEM hti; 

    tvi.mask = TVIF_TEXT | TVIF_IMAGE 
               | TVIF_SELECTEDIMAGE | TVIF_PARAM; 

    // Set the text of the item. 
    tvi.pszText = lpszItem; 
    tvi.cchTextMax = sizeof(tvi.pszText)/sizeof(tvi.pszText[0]); 

    // Assume the item is not a parent item, so give it a 
    // document image. 
    tvi.iImage = g_nDocument; 
    tvi.iSelectedImage = g_nDocument; 

    // Save the heading level in the item's application-defined 
    // data area. 
    tvi.lParam = (LPARAM)nLevel; 
    tvins.item = tvi; 
    tvins.hInsertAfter = hPrev; 

    // Set the parent item based on the specified level. 
    if (nLevel == 1) 
        tvins.hParent = TVI_ROOT; 
    else if (nLevel == 2) 
        tvins.hParent = hPrevRootItem; 
    else 
        tvins.hParent = hPrevLev2Item; 

    // Add the item to the tree-view control. 
    hPrev = (HTREEITEM)SendMessage(hwndTV, TVM_INSERTITEM, 
        0, (LPARAM)(LPTVINSERTSTRUCT)&tvins); 

    if (hPrev == NULL)
        return NULL;

    // Save the handle to the item. 
    if (nLevel == 1) 
        hPrevRootItem = hPrev; 
    else if (nLevel == 2) 
        hPrevLev2Item = hPrev; 

    // The new item is a child item. Give the parent item a 
    // closed folder bitmap to indicate it now has child items. 
    if (nLevel > 1)
    { 
        hti = TreeView_GetParent(hwndTV, hPrev); 
        tvi.mask = TVIF_IMAGE | TVIF_SELECTEDIMAGE; 
        tvi.hItem = hti; 
        tvi.iImage = g_nClosed; 
        tvi.iSelectedImage = g_nClosed; 
        TreeView_SetItem(hwndTV, &tvi); 
    } 

    return hPrev; 
} 

// Extracts heading text and heading levels from a global 
// array and passes them to a function that adds them as
// parent and child items to a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 

BOOL InitTreeViewItems(HWND hwndTV)
{ 
    HTREEITEM hti;

    // g_rgDocHeadings is an application-defined global array of 
    // the following structures: 
    //     typedef struct 
    //       { 
    //         TCHAR tchHeading[MAX_HEADING_LEN]; 
    //         int tchLevel; 
    //     } Heading; 
    for (int i = 0; i < ARRAYSIZE(g_rgDocHeadings); i++) 
    { 
        // Add the item to the tree-view control. 
        hti = AddItemToTree(hwndTV, g_rgDocHeadings[i].tchHeading, 
            g_rgDocHeadings[i].tchLevel); 

        if (hti == NULL)
            return FALSE;
    } 
           
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="3db15-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3db15-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3db15-128">Verwenden von Tree-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="3db15-128">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="3db15-129">Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3db15-129">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




