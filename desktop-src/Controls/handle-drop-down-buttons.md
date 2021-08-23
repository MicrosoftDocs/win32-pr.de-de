---
title: Behandeln von Dropdownschaltflächen
description: Eine Dropdownschaltfläche kann Benutzern eine Liste von Optionen anzeigen.
ms.assetid: 2D908D4B-AA8B-4DEF-B656-C37B673ABB4D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74443b0d29b3ab39255d7417fd13677769f6a762ebe176e8301a76029db0c37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544949"
---
# <a name="how-to-handle-drop-down-buttons"></a>Behandeln von Dropdownschaltflächen

Eine Dropdownschaltfläche kann Benutzern eine Liste von Optionen anzeigen. Um diesen Stil der Schaltfläche zu erstellen, geben Sie den [**BTNS-DROPDOWN-Stil \_**](toolbar-control-and-button-styles.md) an (aus Kompatibilitäts- und Kompatibilitäts- mit früheren Versionen der allgemeinen Steuerelemente auch [**ALS \_ TBSTYLE-DROPDOWN**](toolbar-control-and-button-styles.md) bezeichnet). Um eine Dropdownschaltfläche mit einem Pfeil anzuzeigen, müssen Sie auch den [**TBSTYLE \_ EX \_ DRAWDDARROWS-Symbolleistenstil**](toolbar-extended-styles.md) festlegen, indem Sie eine [**TB \_ SETEXTENDEDSTYLE-Meldung**](tb-setextendedstyle.md) senden.

Die folgende Abbildung zeigt eine Dropdownschaltfläche "Öffnen", in der das Kontextmenü geöffnet ist und eine Liste von Dateien angezeigt wird. In diesem Beispiel hat die Symbolleiste den [**TBSTYLE \_ EX \_ DRAWDDARROWS-Stil.**](toolbar-extended-styles.md)

![Screenshot eines Dialogfelds mit drei Symbolleistenelementen, die durch Symbole dargestellt werden; eine verfügt über einen erweiterten Dropdownpfeil und ein Kontextmenü mit drei Elemente.](images/tb-dropdown.png)

Die folgende Abbildung zeigt dieselbe Symbolleiste, dieses Mal ohne [**den TBSTYLE \_ EX \_ DRAWDDARROWS-Stil.**](toolbar-extended-styles.md)

![Screenshot eines vorherigen Dialogfelds, aber das Symbol mit dem Kontextmenü hat keinen Dropdownpfeil](images/tb-dropdown2.png)

Wenn Benutzer auf eine Symbolleistenschaltfläche klicken, die das [**DROPDOWN-Format von BTNS \_**](toolbar-control-and-button-styles.md) verwendet, sendet das Symbolleisten-Steuerelement dem übergeordneten Fenster einen [TBN-DROPDOWN-Benachrichtigungscode. \_](tbn-dropdown.md)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="handle-a-drop-down-button"></a>Behandeln einer Dropdownschaltfläche

Im folgenden Codebeispiel wird veranschaulicht, wie eine Anwendung eine Dropdownschaltfläche in einem Symbolleisten-Steuerelement unterstützen kann.


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

[Verwenden von Symbolleisten-Steuerelementen](using-toolbar-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




