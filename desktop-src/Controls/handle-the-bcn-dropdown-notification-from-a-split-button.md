---
title: Behandeln von BCN_DROPDOWN Benachrichtigungen von splitbuttons
description: In diesem Thema wird beschrieben, wie Sie \_ in einem Dialogfeld Prozeduren auf die BCN-Dropdown Benachrichtigung reagieren können.
ms.assetid: 847DD645-AE29-4F62-BC32-F235BA409E1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a368dd28c5347f438feff75fbddb129a420caae7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102443"
---
# <a name="how-to-handle-the-bcn_dropdown-notification-from-a-split-button"></a>Behandeln der BCN- \_ Dropdown Benachrichtigung über eine unterteilte Schaltfläche

In diesem Thema wird beschrieben, wie Sie in einem Dialogfeld Prozeduren auf die [BCN- \_ Dropdown](bcn-dropdown.md) Benachrichtigung reagieren können.

Die C++-Anwendung ruft die Client Koordinaten der Schaltfläche aus dem Benachrichtigungs Header ab und konvertiert sie in Bildschirm Koordinaten. Anschließend wird ein Popupmenü erstellt und am unteren Rand der Schaltfläche angezeigt. Um das Beispiel einfach zu halten, sind keine Tastenkombinationen für das Menü implementiert.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="step-1-wait-for-the-bcn_dropdown-notification"></a>Schritt 1: warten auf die *BCN- \_ Dropdown* Benachrichtigung.


```C++
case BCN_DROPDOWN:
{
    NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
    if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
    {
```



### <a name="step-2-get-the-screen-coordinates-of-the-button"></a>Schritt 2: Sie erhalten die Bildschirm Koordinaten der Schaltfläche.

Verwenden Sie die [**clientdescreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) -Funktion, um die Fenster Koordinaten der unteren linken Kante der Schaltfläche in Bildschirm Koordinaten zu konvertieren.


```C++
POINT pt;
pt.x = pDropDown->rcButton.left;
pt.y = pDropDown->rcButton.bottom;
ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
```



### <a name="step-3-create-a-menu-and-add-items"></a>Schritt 3: Erstellen Sie ein Menü, und fügen Sie Elemente hinzu.

Verwenden Sie die Funktion " [**kreatepopupmenu**](/windows/desktop/api/winuser/nf-winuser-createpopupmenu) ", um ein Menü zu erstellen. Verwenden Sie die [**AppendMenu**](/windows/desktop/menurc/u) -Funktion, um dem Menü Elemente hinzuzufügen. IDC \_ MENUCOMMAND1 und IDC \_ MENUCOMMAND2 sind Anwendungs definierte Konstanten für Menübefehle.


```C++
HMENU hSplitMenu = CreatePopupMenu();
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
```



### <a name="step-4-display-the-menu"></a>Schritt 4: zeigen Sie das Menü an.

Die [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) -Funktion zeigt ein Kontextmenü an der angegebenen Position an und verfolgt die Auswahl der Elemente im Menü.


```C++
TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
```



## <a name="complete-example"></a>Vollständiges Beispiel


```C++
case WM_NOTIFY:
    switch (((LPNMHDR)lParam)->code)
    {
        case BCN_DROPDOWN:
        {
            NMBCDROPDOWN* pDropDown = (NMBCDROPDOWN*)lParam;
            if (pDropDown->hdr.hwndFrom = GetDlgItem(hDlg, IDC_SPLIT))
            {

                // Get screen coordinates of the button.
                POINT pt;
                pt.x = pDropDown->rcButton.left;
                pt.y = pDropDown->rcButton.bottom;
                ClientToScreen(pDropDown->hdr.hwndFrom, &pt);
        
                // Create a menu and add items.
                HMENU hSplitMenu = CreatePopupMenu();
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND1, L"Menu item 1");
                AppendMenu(hSplitMenu, MF_BYPOSITION, IDC_MENUCOMMAND2, L"Menu item 2");
        
                // Display the menu.
                TrackPopupMenu(hSplitMenu, TPM_LEFTALIGN | TPM_TOPALIGN, pt.x, pt.y, 0, hDlg, NULL);
                return TRUE;
            }
            break;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[BCN- \_ Dropdown-Benachrichtigungs Code](bcn-dropdown.md)
</dt> <dt>

[Informationen zu Schaltflächen](about-buttons.md)
</dt> <dt>

[Button-Steuerelement Verweis](bumper-button-button-control-reference.md)
</dt> <dt>

[Verwenden von Schaltflächen](using-buttons.md)
</dt> <dt>

[Schaltfläche](buttons.md)
</dt> </dl>

 

 