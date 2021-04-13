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
# <a name="menu-notifications"></a><span data-ttu-id="72d68-103">Menü Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="72d68-103">Menu Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="72d68-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="72d68-104">In This Section</span></span>

-   [<span data-ttu-id="72d68-105">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="72d68-105">**WM\_COMMAND**</span></span>](wm-command.md)
-   [<span data-ttu-id="72d68-106">**WM- \_ ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="72d68-106">**WM\_CONTEXTMENU**</span></span>](wm-contextmenu.md)
-   [<span data-ttu-id="72d68-107">**WM- \_ entermenuloop**</span><span class="sxs-lookup"><span data-stu-id="72d68-107">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
-   [<span data-ttu-id="72d68-108">**WM- \_ exitmenuloop**</span><span class="sxs-lookup"><span data-stu-id="72d68-108">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
-   [<span data-ttu-id="72d68-109">**WM \_ gettitlebarinfoex**</span><span class="sxs-lookup"><span data-stu-id="72d68-109">**WM\_GETTITLEBARINFOEX**</span></span>](wm-gettitlebarinfoex.md)
-   [<span data-ttu-id="72d68-110">**WM ( \_ MenuCommand)**</span><span class="sxs-lookup"><span data-stu-id="72d68-110">**WM\_MENUCOMMAND**</span></span>](wm-menucommand.md)
-   [<span data-ttu-id="72d68-111">**WM- \_ menudrag**</span><span class="sxs-lookup"><span data-stu-id="72d68-111">**WM\_MENUDRAG**</span></span>](wm-menudrag.md)
-   [<span data-ttu-id="72d68-112">**WM \_ menugetobject**</span><span class="sxs-lookup"><span data-stu-id="72d68-112">**WM\_MENUGETOBJECT**</span></span>](wm-menugetobject.md)
-   [<span data-ttu-id="72d68-113">**WM- \_ menurbuttonup**</span><span class="sxs-lookup"><span data-stu-id="72d68-113">**WM\_MENURBUTTONUP**</span></span>](wm-menurbuttonup.md)
-   [<span data-ttu-id="72d68-114">**WM- \_ nextmenu**</span><span class="sxs-lookup"><span data-stu-id="72d68-114">**WM\_NEXTMENU**</span></span>](wm-nextmenu.md)
-   [<span data-ttu-id="72d68-115">**WM- \_ uninitmenupopup**</span><span class="sxs-lookup"><span data-stu-id="72d68-115">**WM\_UNINITMENUPOPUP**</span></span>](wm-uninitmenupopup.md)


## <a name="example"></a><span data-ttu-id="72d68-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="72d68-116">Example</span></span>

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
<span data-ttu-id="72d68-117">Beispiel für [klassische Windows-Beispiele](https://github.com/microsoft/Windows-classic-samples) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="72d68-117">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

 




