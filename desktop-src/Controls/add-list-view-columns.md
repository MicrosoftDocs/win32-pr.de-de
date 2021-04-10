---
title: Vorgehensweise beim Hinzufügen von List-View Spalten
description: In diesem Thema wird veranschaulicht, wie Sie einem Listenansicht-Steuerelement Spalten hinzufügen.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e478c57a31fdd7ad91e0089106e93c24c47d5c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039859"
---
# <a name="how-to-add-list-view-columns"></a><span data-ttu-id="431cf-103">Vorgehensweise beim Hinzufügen von List-View Spalten</span><span class="sxs-lookup"><span data-stu-id="431cf-103">How to Add List-View Columns</span></span>

<span data-ttu-id="431cf-104">In diesem Thema wird veranschaulicht, wie Sie einem Listenansicht-Steuerelement Spalten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="431cf-104">This topic demonstrates how to add columns to a list-view control.</span></span> <span data-ttu-id="431cf-105">Spalten werden verwendet, um die Elemente und unter Elemente anzuzeigen, wenn sich ein Listenansicht-Steuerelement in der Berichtsansicht (Details) befindet.</span><span class="sxs-lookup"><span data-stu-id="431cf-105">Columns are used to display the items and subitems when a list-view control is in report (details) view.</span></span> <span data-ttu-id="431cf-106">Text aus ausgewählten Spalten kann auch in der Kachel Ansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="431cf-106">Text from selected columns can also be displayed in tile view.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="431cf-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="431cf-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="431cf-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="431cf-108">Technologies</span></span>

-   [<span data-ttu-id="431cf-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="431cf-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="431cf-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="431cf-110">Prerequisites</span></span>

-   <span data-ttu-id="431cf-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="431cf-111">C/C++</span></span>
-   <span data-ttu-id="431cf-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="431cf-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="431cf-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="431cf-113">Instructions</span></span>


<span data-ttu-id="431cf-114">Zum Hinzufügen einer Spalte zu einem Listenansicht-Steuerelement senden Sie die [**LVM- \_ InsertColumn**](lvm-insertcolumn.md) -Nachricht, oder verwenden Sie das [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) -Makro.</span><span class="sxs-lookup"><span data-stu-id="431cf-114">To add a column to a list-view control, send the [**LVM\_INSERTCOLUMN**](lvm-insertcolumn.md) message or use the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span> <span data-ttu-id="431cf-115">Um eine Spalte zu löschen, verwenden Sie die " [**LVM \_ deleteColumn**](lvm-deletecolumn.md) "-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="431cf-115">To delete a column, use the [**LVM\_DELETECOLUMN**](lvm-deletecolumn.md) message.</span></span>

<span data-ttu-id="431cf-116">Im folgenden C++-Codebeispiel wird das [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) -Makro aufgerufen, um einem Listenansicht-Steuerelement Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="431cf-116">The following C++ code example calls the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro to add columns to a list-view control.</span></span> <span data-ttu-id="431cf-117">Die Spaltenüberschriften werden in der Header Datei der Anwendung als Zeichen folgen Ressourcen definiert, die nacheinander beginnend mit den IDs \_ FirstColumn nummeriert werden.</span><span class="sxs-lookup"><span data-stu-id="431cf-117">The column headings are defined in the application's header file as string resources, which are numbered consecutively starting with IDS\_FIRSTCOLUMN.</span></span> <span data-ttu-id="431cf-118">Die Anzahl der Spalten wird in der Header Datei als **C- \_ Spalten** definiert.</span><span class="sxs-lookup"><span data-stu-id="431cf-118">The number of columns is defined in the header file as **C\_COLUMNS**.</span></span>


```C++
// InitListViewColumns: Adds columns to a list-view control.
// hWndListView:        Handle to the list-view control. 
// Returns TRUE if successful, and FALSE otherwise. 
BOOL InitListViewColumns(HWND hWndListView) 
{ 
    WCHAR szText[256];     // Temporary buffer.
    LVCOLUMN lvc;
    int iCol;

    // Initialize the LVCOLUMN structure.
    // The mask specifies that the format, width, text,
    // and subitem members of the structure are valid.
    lvc.mask = LVCF_FMT | LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM;

    // Add the columns.
    for (iCol = 0; iCol < C_COLUMNS; iCol++)
    {
        lvc.iSubItem = iCol;
        lvc.pszText = szText;
        lvc.cx = 100;               // Width of column in pixels.

        if ( iCol < 2 )
            lvc.fmt = LVCFMT_LEFT;  // Left-aligned column.
        else
            lvc.fmt = LVCFMT_RIGHT; // Right-aligned column.

        // Load the names of the column headings from the string resources.
        LoadString(g_hInst,
                   IDS_FIRSTCOLUMN + iCol,
                   szText,
                   sizeof(szText)/sizeof(szText[0]));

        // Insert the columns into the list view.
        if (ListView_InsertColumn(hWndListView, iCol, &lvc) == -1)
            return FALSE;
    }
    
    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="431cf-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="431cf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="431cf-120">Listenansicht-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="431cf-120">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="431cf-121">Informationen zu List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="431cf-121">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="431cf-122">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="431cf-122">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




