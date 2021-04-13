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
# <a name="how-to-add-tree-view-items"></a>Vorgehensweise beim Hinzufügen von Tree-View Elementen

Sie fügen ein Element zu einem Strukturansicht-Steuerelement hinzu, indem Sie die [**TVM \_ InsertItem**](tvm-insertitem.md) -Meldung an das Steuerelement senden. Die Nachricht enthält die Adresse einer [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) -Struktur, die das übergeordnete Element, das Element, nach dem das neue Element eingefügt wird, und eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die die Attribute des Elements definiert, angibt. Die Attribute enthalten die Bezeichnung des Elements, die ausgewählten und nicht ausgewählten Images sowie einen von der 32-Bit-Anwendung definierten Wert.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="add-items-to-the-tree-view"></a>Hinzufügen von Elementen zum Tree-View

Im Beispiel in diesem Abschnitt wird veranschaulicht, wie ein Inhaltsverzeichnis auf der Grundlage von Dokumenten Überschriften Informationen erstellt wird, die in einem Anwendungs definierten Array bereitgestellt werden. Jedes Array Element besteht aus einer Überschriften Zeichenfolge und einer ganzen Zahl, die die Überschriftenebene angibt. Das Beispiel unterstützt drei Überschriften Ebenen (1, 2 und 3).

Das Beispiel enthält zwei Funktionen. Die erste Funktion extrahiert jede Überschrift und die zugehörige Überschriftenebene und übergibt sie an die zweite Funktion.

Die zweite Funktion fügt ein Element zu einem Strukturansicht-Steuerelement hinzu. Er verwendet den Überschriften Text als Bezeichnung des Elements und verwendet die Überschriftenebene, um das übergeordnete Element für das neue Element zu bestimmen. Eine Überschrift der Ebene 1 wird dem Stamm des Strukturansicht-Steuer Elements hinzugefügt, eine Überschrift der Ebene 2 wird als untergeordnetes Element der vorherigen Ebene eines Elements hinzugefügt usw. Die-Funktion weist ein Bild einem Element zu, je nachdem, ob es über untergeordnete Elemente verfügt. Wenn ein Element über untergeordnete Elemente verfügt, wird ein Bild abgerufen, das einen geschlossenen Ordner darstellt. Andernfalls wird ein Bild abgerufen, das ein Dokument darstellt. Ein Element verwendet dasselbe Bild für den ausgewählten und den nicht ausgewählten Zustand.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Tree-View Steuerelementen](using-treeview.md)
</dt> <dt>

[Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




