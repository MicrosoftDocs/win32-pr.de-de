---
title: Hinzufügen von List-View Bildlisten
description: In diesem Thema wird veranschaulicht, wie Einem Listenansicht-Steuerelement Bildlisten hinzugefügt werden.
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8875573634cd47fb5ccb271c3dabfca99daf9061469e31c1178b3e4ed938347e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922056"
---
# <a name="how-to-add-list-view-image-lists"></a>Hinzufügen von List-View Bildlisten

In diesem Thema wird veranschaulicht, wie Einem Listenansicht-Steuerelement Bildlisten hinzugefügt werden.

Sie erstellen nur die Bildlisten, die das Steuerelement verwendet. Wenn Ihre Anwendung dem Benutzer z. B. nicht erlaubt, zur Symbolansicht zu wechseln, müssen Sie keine große Symbolliste erstellen und zuweisen. Wenn Sie sowohl große als auch kleine Bildlisten erstellen, müssen diese die gleichen Bilder in der gleichen Reihenfolge enthalten, da ein einzelner Wert verwendet wird, um das Symbol eines Listenansichtselements in beiden Bildlisten zu identifizieren.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Zum Anzeigen von Elementbildern müssen Sie dem Listenansicht-Steuerelement eine Bildliste zuweisen. Verwenden Sie hierzu die [**LVM \_ SETIMAGELIST-Nachricht**](lvm-setimagelist.md) oder das entsprechende [**Makro ListView \_ SetImageList,**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist)um anzugeben, ob die Bildliste Symbole in voller Größe, kleine Symbole oder Zustandsbilder enthält. Verwenden Sie die [**LVM \_ GETIMAGELIST-Nachricht,**](lvm-getimagelist.md) um das Handle für eine Bildliste abzurufen, die derzeit einem Listenansicht-Steuerelement zugewiesen ist. Sie können die [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) verwenden, um geeignete Dimensionen für die Symbole in voller Größe und für kleine Symbole zu bestimmen.

Im folgenden C++-Codebeispiel erstellt die anwendungsdefinierte Funktion zunächst Bildlisten und weist sie dann einem Listenansicht-Steuerelement zu.


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

[List-View-Steuerelementreferenz](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden List-View-Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 