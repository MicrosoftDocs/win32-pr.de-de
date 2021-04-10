---
title: Erstellen einer QuickInfo für ein Steuerelement
description: Die folgende Beispiel Funktion erstellt eine QuickInfo und verknüpft Sie mit dem-Steuerelement, dessen Ressourcen-ID an Sie übermittelt wird.
ms.assetid: FDA3B2A0-1256-4DAC-86CF-8F123894E760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f341c1be1e749c4e0d6f18caf97a3f897cf429e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036539"
---
# <a name="how-to-create-a-tooltip-for-a-control"></a><span data-ttu-id="61ac3-103">Erstellen einer QuickInfo für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="61ac3-103">How to Create a Tooltip for a Control</span></span>

<span data-ttu-id="61ac3-104">Die folgende Beispiel Funktion erstellt eine QuickInfo und verknüpft Sie mit dem-Steuerelement, dessen Ressourcen-ID an Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="61ac3-104">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="61ac3-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="61ac3-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="61ac3-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="61ac3-106">Technologies</span></span>

-   [<span data-ttu-id="61ac3-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="61ac3-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="61ac3-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="61ac3-108">Prerequisites</span></span>

-   <span data-ttu-id="61ac3-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="61ac3-109">C/C++</span></span>
-   <span data-ttu-id="61ac3-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="61ac3-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="61ac3-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="61ac3-111">Instructions</span></span>

### <a name="create-a-tooltip-for-a-control"></a><span data-ttu-id="61ac3-112">Erstellen einer QuickInfo für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="61ac3-112">Create a Tooltip for a Control</span></span>

<span data-ttu-id="61ac3-113">Die folgende Beispiel Funktion erstellt eine QuickInfo und verknüpft Sie mit dem-Steuerelement, dessen Ressourcen-ID an Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="61ac3-113">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span>


```C++
// Description:
//   Creates a tooltip for an item in a dialog box. 
// Parameters:
//   idTool - identifier of an dialog box item.
//   nDlg - window handle of the dialog box.
//   pszText - string to use as the tooltip text.
// Returns:
//   The handle to the tooltip.
//
HWND CreateToolTip(int toolID, HWND hDlg, PTSTR pszText)
{
    if (!toolID || !hDlg || !pszText)
    {
        return FALSE;
    }
    // Get the window of the tool.
    HWND hwndTool = GetDlgItem(hDlg, toolID);
    
    // Create the tooltip. g_hInst is the global instance handle.
    HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                              WS_POPUP |TTS_ALWAYSTIP | TTS_BALLOON,
                              CW_USEDEFAULT, CW_USEDEFAULT,
                              CW_USEDEFAULT, CW_USEDEFAULT,
                              hDlg, NULL, 
                              g_hInst, NULL);
    
   if (!hwndTool || !hwndTip)
   {
       return (HWND)NULL;
   }                              
                              
    // Associate the tooltip with the tool.
    TOOLINFO toolInfo = { 0 };
    toolInfo.cbSize = sizeof(toolInfo);
    toolInfo.hwnd = hDlg;
    toolInfo.uFlags = TTF_IDISHWND | TTF_SUBCLASS;
    toolInfo.uId = (UINT_PTR)hwndTool;
    toolInfo.lpszText = pszText;
    SendMessage(hwndTip, TTM_ADDTOOL, 0, (LPARAM)&toolInfo);

    return hwndTip;
}
```



## <a name="related-topics"></a><span data-ttu-id="61ac3-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61ac3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61ac3-115">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="61ac3-115">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




