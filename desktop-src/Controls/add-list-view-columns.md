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
# <a name="how-to-add-list-view-columns"></a>Vorgehensweise beim Hinzufügen von List-View Spalten

In diesem Thema wird veranschaulicht, wie Sie einem Listenansicht-Steuerelement Spalten hinzufügen. Spalten werden verwendet, um die Elemente und unter Elemente anzuzeigen, wenn sich ein Listenansicht-Steuerelement in der Berichtsansicht (Details) befindet. Text aus ausgewählten Spalten kann auch in der Kachel Ansicht angezeigt werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Zum Hinzufügen einer Spalte zu einem Listenansicht-Steuerelement senden Sie die [**LVM- \_ InsertColumn**](lvm-insertcolumn.md) -Nachricht, oder verwenden Sie das [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) -Makro. Um eine Spalte zu löschen, verwenden Sie die " [**LVM \_ deleteColumn**](lvm-deletecolumn.md) "-Nachricht.

Im folgenden C++-Codebeispiel wird das [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) -Makro aufgerufen, um einem Listenansicht-Steuerelement Spalten hinzuzufügen. Die Spaltenüberschriften werden in der Header Datei der Anwendung als Zeichen folgen Ressourcen definiert, die nacheinander beginnend mit den IDs \_ FirstColumn nummeriert werden. Die Anzahl der Spalten wird in der Header Datei als **C- \_ Spalten** definiert.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Listenansicht-Steuerelement Verweis](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen zu List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 




