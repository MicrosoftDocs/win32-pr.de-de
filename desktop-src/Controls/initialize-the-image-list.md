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
# <a name="how-to-initialize-the-image-list"></a><span data-ttu-id="be17d-103">Initialisieren der Bildliste</span><span class="sxs-lookup"><span data-stu-id="be17d-103">How to Initialize the Image List</span></span>

<span data-ttu-id="be17d-104">Jedem Element in einem Strukturansicht-Steuerelement können zwei Bilder zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="be17d-104">Every item in a tree-view control can have two images associated with it.</span></span> <span data-ttu-id="be17d-105">Ein Element zeigt ein Bild an, wenn es ausgewählt wird, und das andere, wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="be17d-105">An item displays one image when it is selected and the other when it is not.</span></span> <span data-ttu-id="be17d-106">Um Bilder in Struktur Ansichts Elemente einzuschließen, verwenden Sie zuerst die Funktionen der [Bild](image-lists.md) Liste, um eine Bildliste zu erstellen und Ihr Bilder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="be17d-106">To include images with tree-view items, first use the [Image Lists](image-lists.md) functions to create an image list and add images to it.</span></span> <span data-ttu-id="be17d-107">Ordnen Sie dann die Bildliste dem Strukturansicht-Steuerelement mithilfe der [**TVM-Meldung " \_ SetImageList**](tvm-setimagelist.md) " zu.</span><span class="sxs-lookup"><span data-stu-id="be17d-107">Then associate the image list with the tree-view control by using the [**TVM\_SETIMAGELIST**](tvm-setimagelist.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="be17d-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="be17d-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="be17d-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="be17d-109">Technologies</span></span>

-   [<span data-ttu-id="be17d-110">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="be17d-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="be17d-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="be17d-111">Prerequisites</span></span>

-   <span data-ttu-id="be17d-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="be17d-112">C/C++</span></span>
-   <span data-ttu-id="be17d-113">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="be17d-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="be17d-114">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="be17d-114">Instructions</span></span>

### <a name="initialize-the-image-list"></a><span data-ttu-id="be17d-115">Initialisieren der Bildliste</span><span class="sxs-lookup"><span data-stu-id="be17d-115">Initialize the Image List</span></span>

<span data-ttu-id="be17d-116">Im folgenden Beispiel wird eine Bildliste erstellt, drei Bitmaps werden der Liste hinzugefügt, und die Bildliste wird einem Strukturansicht-Steuerelement zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="be17d-116">The following example creates an image list, adds three bitmaps to the list, and associates the image list with a tree-view control.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="be17d-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be17d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be17d-118">Verwenden von Tree-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="be17d-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="be17d-119">Custdtv-Beispiel veranschaulicht benutzerdefiniertes Zeichnen in einem Tree-View-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="be17d-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




