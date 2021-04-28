---
title: Menübenachrichtigungen
description: Menübenachrichtigungen
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593e3007dff82241dc9e917a6cfa140cc443679
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112528"
---
# <a name="menu-notifications"></a><span data-ttu-id="c4715-103">Menübenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c4715-103">Menu Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4715-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c4715-104">In This Section</span></span>

-   [<span data-ttu-id="c4715-105">**\_WM-BEFEHL**</span><span class="sxs-lookup"><span data-stu-id="c4715-105">**WM\_COMMAND**</span></span>](wm-command.md)
-   [<span data-ttu-id="c4715-106">**WM \_ CONTEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="c4715-106">**WM\_CONTEXTMENU**</span></span>](wm-contextmenu.md)
-   [<span data-ttu-id="c4715-107">**WM \_ ENTERMENULOOP**</span><span class="sxs-lookup"><span data-stu-id="c4715-107">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
-   [<span data-ttu-id="c4715-108">**WM \_ EXITMENULOOP**</span><span class="sxs-lookup"><span data-stu-id="c4715-108">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
-   [<span data-ttu-id="c4715-109">**WM \_ GETTITLEBARINFOEX**</span><span class="sxs-lookup"><span data-stu-id="c4715-109">**WM\_GETTITLEBARINFOEX**</span></span>](wm-gettitlebarinfoex.md)
-   [<span data-ttu-id="c4715-110">**\_WM-MENÜBEFEHL**</span><span class="sxs-lookup"><span data-stu-id="c4715-110">**WM\_MENUCOMMAND**</span></span>](wm-menucommand.md)
-   [<span data-ttu-id="c4715-111">**WM \_ MENUDRAG**</span><span class="sxs-lookup"><span data-stu-id="c4715-111">**WM\_MENUDRAG**</span></span>](wm-menudrag.md)
-   [<span data-ttu-id="c4715-112">**\_WM-MENÜGETOBJECT**</span><span class="sxs-lookup"><span data-stu-id="c4715-112">**WM\_MENUGETOBJECT**</span></span>](wm-menugetobject.md)
-   [<span data-ttu-id="c4715-113">**\_WM-MENÜRBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="c4715-113">**WM\_MENURBUTTONUP**</span></span>](wm-menurbuttonup.md)
-   [<span data-ttu-id="c4715-114">**WM \_ NEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="c4715-114">**WM\_NEXTMENU**</span></span>](wm-nextmenu.md)
-   [<span data-ttu-id="c4715-115">**WM \_ UNINITMENUPOPUP**</span><span class="sxs-lookup"><span data-stu-id="c4715-115">**WM\_UNINITMENUPOPUP**</span></span>](wm-uninitmenupopup.md)


## <a name="example"></a><span data-ttu-id="c4715-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c4715-116">Example</span></span>

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
<span data-ttu-id="c4715-117">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="c4715-117">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

 




