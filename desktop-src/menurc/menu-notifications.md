---
title: Menübenachrichtigungen
description: Menübenachrichtigungen
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7370da93f430c62618b5d459e40bfa56cb7a9ff9f960f95eb6ce614cc7273e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734256"
---
# <a name="menu-notifications"></a>Menübenachrichtigungen

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**\_WM-BEFEHL**](wm-command.md)
-   [**WM \_ CONTEXTMENU**](wm-contextmenu.md)
-   [**WM \_ ENTERMENULOOP**](wm-entermenuloop.md)
-   [**WM \_ EXITMENULOOP**](wm-exitmenuloop.md)
-   [**WM \_ GETTITLEBARINFOEX**](wm-gettitlebarinfoex.md)
-   [**\_WM-MENÜBEFEHL**](wm-menucommand.md)
-   [**WM \_ MENUDRAG**](wm-menudrag.md)
-   [**\_WM-MENÜGETOBJECT**](wm-menugetobject.md)
-   [**WM \_ MENURBUTTONUP**](wm-menurbuttonup.md)
-   [**WM \_ NEXTMENU**](wm-nextmenu.md)
-   [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md)


## <a name="example"></a>Beispiel

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples) auf GitHub.

 




