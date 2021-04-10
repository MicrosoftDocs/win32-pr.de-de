---
title: Initialisieren der Bildliste
description: Jedem Element in einem Strukturansicht-Steuerelement können zwei Bilder zugeordnet werden.
ms.assetid: 3683DB35-D70F-4181-9181-95354599B9FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011d789da4eec39febae9d93436e23c23fa59507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101286"
---
# <a name="how-to-initialize-the-image-list"></a>Initialisieren der Bildliste

Jedem Element in einem Strukturansicht-Steuerelement können zwei Bilder zugeordnet werden. Ein Element zeigt ein Bild an, wenn es ausgewählt wird, und das andere, wenn dies nicht der Fall ist. Um Bilder in Struktur Ansichts Elemente einzuschließen, verwenden Sie zuerst die Funktionen der [Bild](image-lists.md) Liste, um eine Bildliste zu erstellen und Ihr Bilder hinzuzufügen. Ordnen Sie dann die Bildliste dem Strukturansicht-Steuerelement mithilfe der [**TVM-Meldung " \_ SetImageList**](tvm-setimagelist.md) " zu.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="initialize-the-image-list"></a>Initialisieren der Bildliste

Im folgenden Beispiel wird eine Bildliste erstellt, drei Bitmaps werden der Liste hinzugefügt, und die Bildliste wird einem Strukturansicht-Steuerelement zugeordnet.


```C++
// InitTreeViewImageLists - creates an image list, adds three bitmaps 
// to it, and associates the image list with a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 
//
// Global variables and constants: 
// g_hInst - the global instance handle.
// g_nOpen, g_nClosed, and g_nDocument - global indexes of the images. 
// CX_BITMAP and CY_BITMAP - width and height of an icon. 
// NUM_BITMAPS - number of bitmaps to add to the image list. 
// IDB_OPEN_FILE, IDB_CLOSED_FILE, IDB_DOCUMENT -
//     resource identifiers of the bitmaps.

BOOL InitTreeViewImageLists(HWND hwndTV) 
{ 
    HIMAGELIST himl;  // handle to image list 
    HBITMAP hbmp;     // handle to bitmap 

    // Create the image list. 
    if ((himl = ImageList_Create(CX_BITMAP, 
                                 CY_BITMAP,
                                 FALSE, 
                                 NUM_BITMAPS, 0)) == NULL) 
        return FALSE; 

    // Add the open file, closed file, and document bitmaps. 
    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_OPEN_FILE)); 
    g_nOpen = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CLOSED_FILE)); 
    g_nClosed = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_DOCUMENT)); 
    g_nDocument = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    // Fail if not all of the images were added. 
    if (ImageList_GetImageCount(himl) < 3) 
        return FALSE; 

    // Associate the image list with the tree-view control. 
    TreeView_SetImageList(hwndTV, himl, TVSIL_NORMAL); 

    return TRUE; 
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Tree-View Steuerelementen](using-treeview.md)
</dt> <dt>

[Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




