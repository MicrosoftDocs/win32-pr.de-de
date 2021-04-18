---
title: Verwenden von Syslink-Benachrichtigungen
description: Dem Syslink-Steuerelement \ 8212 sind zwei Benachrichtigungs Meldungen zugeordnet, eine für die Maus (nm \_ Click (Syslink)) und eine für die Tastatur (nm \_ Return).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "106338448"
---
# <a name="how-to-use-syslink-notifications"></a><span data-ttu-id="cec64-103">Verwenden von Syslink-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="cec64-103">How to Use SysLink Notifications</span></span>

<span data-ttu-id="cec64-104">Dem Syslink-Steuerelement sind zwei Benachrichtigungs Meldungen zugeordnet – eine für die Maus ([nm \_ Click (Syslink)](nm-click-syslink.md)) und eine für die Tastatur ([nm \_ Return](nm-return.md)).</span><span class="sxs-lookup"><span data-stu-id="cec64-104">There are two notification messages associated with the SysLink control—one for the mouse ([NM\_CLICK (syslink)](nm-click-syslink.md)), and one for the keyboard ([NM\_RETURN](nm-return.md)).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cec64-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="cec64-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cec64-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="cec64-106">Technologies</span></span>

-   [<span data-ttu-id="cec64-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="cec64-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cec64-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="cec64-108">Prerequisites</span></span>

-   <span data-ttu-id="cec64-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="cec64-109">C/C++</span></span>
-   <span data-ttu-id="cec64-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="cec64-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cec64-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="cec64-111">Instructions</span></span>

### <a name="use-syslink-notifications"></a><span data-ttu-id="cec64-112">Verwenden von Syslink-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="cec64-112">Use SysLink Notifications</span></span>

<span data-ttu-id="cec64-113">Der folgende Beispielcode zeigt, wie die Syslink-Benachrichtigungen verarbeitet werden, die generiert werden, wenn der Benutzer auf einen der beiden Links im [vorherigen Beispiel](create-syslink-controls.md)klickt.</span><span class="sxs-lookup"><span data-stu-id="cec64-113">The following example code shows how to process the SysLink notifications that are generated when the user clicks either of the two links in the [previous example](create-syslink-controls.md).</span></span> <span data-ttu-id="cec64-114">Wenn der Benutzer auf die Internet-URL klickt, wird die zugehörige Webseite im Standardbrowser geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cec64-114">When the user clicks the Internet URL, the associated webpage opens in the default browser.</span></span> <span data-ttu-id="cec64-115">Wenn der Benutzer auf den von der Anwendung definierten Hyperlink klickt, wird ein Meldungs Feld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cec64-115">When the user clicks the application-defined hyperlink, a message box is displayed.</span></span>


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a><span data-ttu-id="cec64-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cec64-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cec64-117">Verwenden von Syslink-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="cec64-117">Using SysLink Controls</span></span>](using-syslink-controls.md)
</dt> <dt>

<span data-ttu-id="cec64-118">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="cec64-118">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




