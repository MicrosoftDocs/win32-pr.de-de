---
title: Erstellen einer QuickInfo für einen rechteckigen Bereich
description: Im folgenden Beispiel wird veranschaulicht, wie ein Standardmäßiges QuickInfo-Steuerelement für den gesamten Client Bereich eines Fensters erstellt wird.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708652"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="29d34-103">Erstellen einer QuickInfo für einen rechteckigen Bereich</span><span class="sxs-lookup"><span data-stu-id="29d34-103">How to Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="29d34-104">Im folgenden Beispiel wird veranschaulicht, wie ein Standardmäßiges QuickInfo-Steuerelement für den gesamten Client Bereich eines Fensters erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="29d34-104">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>

<span data-ttu-id="29d34-105">Die folgende Abbildung zeigt die QuickInfo, die angezeigt wird, wenn sich der Mauszeiger innerhalb des Client Fensters eines Dialog Felds befindet.</span><span class="sxs-lookup"><span data-stu-id="29d34-105">The following illustration shows the tooltip that is displayed when the mouse pointer is within the client window of a dialog box.</span></span> <span data-ttu-id="29d34-106">Das Handle des Dialog Felds wurde an die im vorherigen Beispiel gezeigte Funktion weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="29d34-106">The handle of the dialog box was passed to the function shown in the preceding example.</span></span>

![Screenshot eines Dialog Felds der Mauszeiger befindet sich innerhalb des Client Fensters, und eine QuickInfo ist sichtbar.](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="29d34-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="29d34-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="29d34-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="29d34-109">Technologies</span></span>

-   [<span data-ttu-id="29d34-110">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="29d34-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="29d34-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="29d34-111">Prerequisites</span></span>

-   <span data-ttu-id="29d34-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="29d34-112">C/C++</span></span>
-   <span data-ttu-id="29d34-113">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="29d34-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="29d34-114">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="29d34-114">Instructions</span></span>

### <a name="create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="29d34-115">Erstellen einer QuickInfo für einen rechteckigen Bereich</span><span class="sxs-lookup"><span data-stu-id="29d34-115">Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="29d34-116">Im folgenden Beispiel wird veranschaulicht, wie ein Standardmäßiges QuickInfo-Steuerelement für den gesamten Client Bereich eines Fensters erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="29d34-116">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="29d34-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29d34-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29d34-118">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="29d34-118">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




