---
title: Menü Benachrichtigungen
description: .
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61f5303253fd3201fd9a4510ecf90fa76c10524
ms.sourcegitcommit: e98f40bef170ae9ce30d91ba96b90600b0446a24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2020
ms.locfileid: "104314576"
---
# <a name="menu-notifications"></a>Menü Benachrichtigungen

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**WM- \_ Befehl**](wm-command.md)
-   [**WM- \_ ContextMenu**](wm-contextmenu.md)
-   [**WM- \_ entermenuloop**](wm-entermenuloop.md)
-   [**WM- \_ exitmenuloop**](wm-exitmenuloop.md)
-   [**WM \_ gettitlebarinfoex**](wm-gettitlebarinfoex.md)
-   [**WM ( \_ MenuCommand)**](wm-menucommand.md)
-   [**WM- \_ menudrag**](wm-menudrag.md)
-   [**WM \_ menugetobject**](wm-menugetobject.md)
-   [**WM- \_ menurbuttonup**](wm-menurbuttonup.md)
-   [**WM- \_ nextmenu**](wm-nextmenu.md)
-   [**WM- \_ uninitmenupopup**](wm-uninitmenupopup.md)


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
Beispiel für [klassische Windows-Beispiele](https://github.com/microsoft/Windows-classic-samples) auf GitHub.

 




