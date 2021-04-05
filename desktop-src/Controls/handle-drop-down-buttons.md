---
title: Behandeln von Dropdown-Schaltflächen
description: Eine Dropdown-Schaltfläche kann Benutzern eine Liste von Optionen zur Verfügung stellen.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d6f59bfa888d346e196e13ce030d1473a07f0f
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724273"
---
# <a name="how-to-handle-drop-down-buttons"></a>Behandeln von Dropdown-Schaltflächen

Eine Dropdown-Schaltfläche kann Benutzern eine Liste von Optionen zur Verfügung stellen. Um diese Art von Schaltfläche zu erstellen, geben Sie den [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil (auch als [**tbstyle- \_ Dropdown**](toolbar-control-and-button-styles.md) bezeichnet) für die Kompatibilität mit früheren Versionen der allgemeinen Steuerelemente an. Um eine Dropdown-Schaltfläche mit einem Pfeil anzuzeigen, müssen Sie auch den Symbolleisten Stil [**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) festlegen, indem Sie eine [**TB- \_ SetExtendedStyle**](tb-setextendedstyle.md) -Nachricht senden.

Die folgende Abbildung zeigt eine Dropdown-Schaltfläche "Öffnen", bei der das Kontextmenü geöffnet ist und eine Liste von Dateien anzeigt. In diesem Beispiel hat die Symbolleiste den Stil [**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) .

![Screenshot eines Dialog Felds mit drei Symbolleisten Elementen, die durch Symbole dargestellt werden. eine verfügt über einen erweiterten Dropdown Pfeil und ein Kontextmenü mit drei Elementen.](images/tb-dropdown.png)

In der folgenden Abbildung wird die gleiche Symbolleiste angezeigt, diesmal ohne den Stil " [**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) ".

![Screenshot eines vorherigen Dialog Felds, aber das Symbol mit dem Kontextmenü enthält keinen Dropdown Pfeil.](images/tb-dropdown2.png)

Wenn Benutzer auf eine Symbolleisten Schaltfläche klicken, die den [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil verwendet, sendet das Symbolleisten-Steuerelement das übergeordnete Fenster mit dem [ \_ Dropdown](tbn-dropdown.md) -Benachrichtigungs Code

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="handle-a-drop-down-button"></a>Behandeln einer Dropdown Schaltfläche

Im folgenden Codebeispiel wird veranschaulicht, wie eine Anwendung eine Dropdown-Schaltfläche in einem Symbolleisten-Steuerelement unterstützen kann.


```C++
BOOL DoNotify(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{

    #define lpnm   ((LPNMHDR)lParam)
    #define lpnmTB ((LPNMTOOLBAR)lParam)

    switch(lpnm->code)
    {
        case TBN_DROPDOWN:
        {
            // Get the coordinates of the button.
            RECT rc;
            SendMessage(lpnmTB->hdr.hwndFrom, TB_GETRECT, (WPARAM)lpnmTB->iItem, (LPARAM)&rc);

            // Convert to screen coordinates.            
            MapWindowPoints(lpnmTB->hdr.hwndFrom, HWND_DESKTOP, (LPPOINT)&rc, 2);                         
        
            // Get the menu.
            HMENU hMenuLoaded = LoadMenu(g_hinst, MAKEINTRESOURCE(IDR_POPUP)); 
         
            // Get the submenu for the first menu item.
            HMENU hPopupMenu = GetSubMenu(hMenuLoaded, 0);

            // Set up the pop-up menu.
            // In case the toolbar is too close to the bottom of the screen, 
            // set rcExclude equal to the button rectangle and the menu will appear above 
            // the button, and not below it.
         
            TPMPARAMS tpm;
         
            tpm.cbSize    = sizeof(TPMPARAMS);
            tpm.rcExclude = rc;
         
            // Show the menu and wait for input. 
            // If the user selects an item, its WM_COMMAND is sent.
         
            TrackPopupMenuEx(hPopupMenu, 
                             TPM_LEFTALIGN | TPM_LEFTBUTTON | TPM_VERTICAL, 
                             rc.left, rc.bottom, g_hwndMain, &tpm);

            DestroyMenu(hMenuLoaded);
         
        return (FALSE);
      
        }
    }
   
    return FALSE;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Symbolleisten](using-toolbar-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




