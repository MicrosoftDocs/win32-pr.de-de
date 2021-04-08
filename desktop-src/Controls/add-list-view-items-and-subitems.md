---
title: Vorgehensweise beim Hinzufügen von List-View Elementen und unter Elementen
description: In diesem Thema wird veranschaulicht, wie Elemente und unter Elemente zu einem Listenansicht-Steuerelement hinzugefügt werden.
ms.assetid: B7E204DC-FD08-4639-985D-1459A1AC0ED6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b3d20008edc10fda810261427507c77e9cfe34
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102566"
---
# <a name="how-to-add-list-view-items-and-subitems"></a>Vorgehensweise beim Hinzufügen von List-View Elementen und unter Elementen

In diesem Thema wird veranschaulicht, wie Elemente und unter Elemente zu einem Listenansicht-Steuerelement hinzugefügt werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Um einem Listenansicht-Steuerelement ein Element hinzuzufügen, muss eine Anwendung zunächst eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur definieren und dann eine [**LVM \_ InsertItem**](lvm-insertitem.md) -Nachricht senden, wobei die Adresse der **lvitem** -Struktur angegeben wird. Wenn eine Anwendung die Berichtsansicht verwendet, muss der untergeordnete Text angegeben werden.

Im folgenden C++-Codebeispiel wird eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur gefüllt, und die Listen Ansichts Elemente werden mithilfe der [**LVM- \_ InsertItem**](lvm-insertitem.md) -Nachricht oder des entsprechenden " [**\_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)"-Makros von ListView hinzugefügt. Da die Anwendung ihren eigenen Text speichert, gibt Sie den LPSTR- \_ textcallback-Wert für den **pszText** -Member der **lvitem** -Struktur an. Wenn Sie den LPSTR- \_ textcallback-Wert angeben, sendet das Steuerelement einen [**LVN \_ getdispinfo**](lvn-getdispinfo.md) -Benachrichtigungs Code an das Besitzer Fenster, wenn ein Element angezeigt werden muss.


```C++
// InsertListViewItems: Inserts items into a list view. 
// hWndListView:        Handle to the list-view control.
// cItems:              Number of items to insert.
// Returns TRUE if successful, and FALSE otherwise.
BOOL InsertListViewItems(HWND hWndListView, int cItems)
{
    LVITEM lvI;

    // Initialize LVITEM members that are common to all items.
    lvI.pszText   = LPSTR_TEXTCALLBACK; // Sends an LVN_GETDISPINFO message.
    lvI.mask      = LVIF_TEXT | LVIF_IMAGE |LVIF_STATE;
    lvI.stateMask = 0;
    lvI.iSubItem  = 0;
    lvI.state     = 0;

    // Initialize LVITEM members that are different for each item.
    for (int index = 0; index < cItems; index++)
    {
        lvI.iItem  = index;
        lvI.iImage = index;
    
        // Insert items into the list.
        if (ListView_InsertItem(hWndListView, &lvI) == -1)
            return FALSE;
    }

    return TRUE;
}

// HandleWM_NOTIFY - Handles the LVN_GETDISPINFO notification code that is 
//         sent in a WM_NOTIFY to the list view parent window. The function 
//        provides display strings for list view items and subitems.
//
// lParam - The LPARAM parameter passed with the WM_NOTIFY message.
// rgPetInfo - A global array of structures, defined as follows:
//         struct PETINFO
//        {
//            TCHAR szKind[10];
//            TCHAR szBreed[50];
//            TCHAR szPrice[20];
//        };
//
//        PETINFO rgPetInfo[ ] = 
//        {
//            {TEXT("Dog"),  TEXT("Poodle"),     TEXT("$300.00")},
//            {TEXT("Cat"),  TEXT("Siamese"),    TEXT("$100.00")},
//            {TEXT("Fish"), TEXT("Angel Fish"), TEXT("$10.00")},
//            {TEXT("Bird"), TEXT("Parakeet"),   TEXT("$5.00")},
//            {TEXT("Toad"), TEXT("Woodhouse"),  TEXT("$0.25")},
//        };
//
void HandleWM_NOTIFY(LPARAM lParam)
{
    NMLVDISPINFO* plvdi;

    switch (((LPNMHDR) lParam)->code)
    {
        case LVN_GETDISPINFO:

            plvdi = (NMLVDISPINFO*)lParam;

            switch (plvdi->item.iSubItem)
            {
                case 0:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szKind;
                    break;
                      
                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;
                
                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;
                
                default:
                    break;
            }

        break;

    }
    // NOTE: In addition to setting pszText to point to the item text, you could 
    // copy the item text into pszText using StringCchCopy. For example:
    //
    // StringCchCopy(plvdi->item.pszText, 
    //                         plvdi->item.cchTextMax, 
    //                         rgPetInfo[plvdi->item.iItem].szKind);

    return;
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

 

 




