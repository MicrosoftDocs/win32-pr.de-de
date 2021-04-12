---
title: Vorgehensweise beim Hinzufügen von List-View Bildlisten
description: In diesem Thema wird veranschaulicht, wie Sie einem Listenansicht-Steuerelement Bildlisten hinzufügen.
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f6f5b483ea80b412ab7638c9aceafcac4c5e6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316784"
---
# <a name="how-to-add-list-view-image-lists"></a>Vorgehensweise beim Hinzufügen von List-View Bildlisten

In diesem Thema wird veranschaulicht, wie Sie einem Listenansicht-Steuerelement Bildlisten hinzufügen.

Sie erstellen nur die Bildlisten, die vom Steuerelement verwendet werden. Wenn die Anwendung z. b. nicht zulässt, dass der Benutzer zur Symbol Ansicht wechselt, müssen Sie keine große Symbolliste erstellen und zuweisen. Wenn Sie sowohl große als auch kleine Bildlisten erstellen, müssen Sie dieselben Bilder in derselben Reihenfolge enthalten, da ein einzelner Wert verwendet wird, um das Symbol eines Listen Ansichts Elements in beiden Bildlisten zu identifizieren.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Zum Anzeigen von Element Bildern müssen Sie dem Listenansicht-Steuerelement eine Bildliste zuweisen. Verwenden Sie hierzu die LVM- [**\_ SetImageList**](lvm-setimagelist.md) -Nachricht oder das entsprechende Makro [**ListView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), und geben Sie an, ob die Bildliste Symbole in voller Größe, kleine Symbole oder Zustands Bilder enthält. Um das Handle für eine Bildliste abzurufen, die derzeit einem Listenansicht-Steuerelement zugewiesen ist, verwenden Sie die [**LVM \_ GetImageList**](lvm-getimagelist.md) -Nachricht. Sie können die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion verwenden, um geeignete Dimensionen für die Symbole in voller und kleiner Größe zu bestimmen.

Im folgenden C++-Codebeispiel erstellt die Anwendungs definierte Funktion zuerst Bildlisten und weist Sie dann einem Listenansicht-Steuerelement zu.


```C++
// InitListViewImageLists: Creates image lists for a list-view control.
// This function only creates image lists. It does not insert the items into
// the control, which is necessary for the control to be visible.   
//
// Returns TRUE if successful, or FALSE otherwise. 
//
// hWndListView: Handle to the list-view control. 
// global variable g_hInst: The handle to the module of either a 
// dynamic-link library (DLL) or executable (.exe) that contains
// the image to be loaded. If loading a standard or system
// icon, set g_hInst to NULL.
//
BOOL InitListViewImageLists(HWND hWndListView) 
{ 
    HICON hiconItem;     // Icon for list-view items.
    HIMAGELIST hLarge;   // Image list for icon view.
    HIMAGELIST hSmall;   // Image list for other views.

    // Create the full-sized icon image lists. 
    hLarge = ImageList_Create(GetSystemMetrics(SM_CXICON), 
                              GetSystemMetrics(SM_CYICON), 
                              ILC_MASK, 1, 1); 

    hSmall = ImageList_Create(GetSystemMetrics(SM_CXSMICON), 
                              GetSystemMetrics(SM_CYSMICON), 
                              ILC_MASK, 1, 1); 
    
    // Add an icon to each image list.  
    hiconItem = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ITEM));

    ImageList_AddIcon(hLarge, hiconItem);
    ImageList_AddIcon(hSmall, hiconItem);

    DestroyIcon(hiconItem);
 
// When you are dealing with multiple icons, you can use the previous four lines of 
// code inside a loop. The following code shows such a loop. The 
// icons are defined in the application's header file as resources, which 
// are numbered consecutively starting with IDS_FIRSTICON. The number of 
// icons is defined in the header file as C_ICONS.
/*    
    for(index = 0; index < C_ICONS; index++)
    {
        hIconItem = LoadIcon (g_hinst, MAKEINTRESOURCE(IDS_FIRSTICON + index));
        ImageList_AddIcon(hSmall, hIconItem);
        ImageList_AddIcon(hLarge, hIconItem);
        Destroy(hIconItem);
    }
*/
    
    // Assign the image lists to the list-view control. 
    ListView_SetImageList(hWndListView, hLarge, LVSIL_NORMAL); 
    ListView_SetImageList(hWndListView, hSmall, LVSIL_SMALL); 
    
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

 

 