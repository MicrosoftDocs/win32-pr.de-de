---
title: Hinzufügen von List-View Spalten
description: In diesem Thema wird veranschaulicht, wie Einem Listenansicht-Steuerelement Spalten hinzugefügt werden.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee71065729502410d189493527af0e3e37663a4a2aaf541852454af7fa4a5aac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922080"
---
# <a name="how-to-add-list-view-columns"></a>Hinzufügen von List-View Spalten

In diesem Thema wird veranschaulicht, wie Einem Listenansicht-Steuerelement Spalten hinzugefügt werden. Spalten werden verwendet, um die Elemente und Unterelemente anzuzeigen, wenn sich ein Listenansicht-Steuerelement in der Berichtsansicht (Details) befindet. Text aus ausgewählten Spalten kann auch in der Kachelansicht angezeigt werden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Um einem Listenansicht-Steuerelement eine Spalte hinzuzufügen, senden Sie die [**LVM \_ INSERTCOLUMN-Nachricht,**](lvm-insertcolumn.md) oder verwenden Sie das [**ListView \_ InsertColumn-Makro.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) Um eine Spalte zu löschen, verwenden Sie die [**LVM \_ DELETECOLUMN-Meldung.**](lvm-deletecolumn.md)

Im folgenden C++-Codebeispiel wird das [**ListView \_ InsertColumn-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) zum Hinzufügen von Spalten zu einem Listenansicht-Steuerelement aufruft. Die Spaltenüberschriften werden in der Headerdatei der Anwendung als Zeichenfolgenressourcen definiert, die nacheinander beginnend mit IDS \_ FIRSTCOLUMN nummeriert werden. Die Anzahl der Spalten wird in der Headerdatei als **C \_ COLUMNS definiert.**


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

[List-View-Steuerelementreferenz](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 




