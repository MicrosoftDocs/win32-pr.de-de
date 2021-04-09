---
title: Anzeigen von Quick Infos für Schaltflächen
description: Wenn Sie den tbstyle- \_ Tooltips-Stil angeben, erstellt und verwaltet die Symbolleiste ein QuickInfo-Steuerelement. Das QuickInfo-Steuerelement ist ausgeblendet und wird nur angezeigt, wenn Benutzer den Mauszeiger über eine Symbolleisten Schaltfläche bewegen und diese für ungefähr eine Sekunde belassen.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103858103"
---
# <a name="how-to-display-tooltips-for-buttons"></a><span data-ttu-id="42d34-104">Anzeigen von Quick Infos für Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="42d34-104">How to Display Tooltips for Buttons</span></span>

<span data-ttu-id="42d34-105">Wenn Sie den [**tbstyle- \_ Tooltips**](toolbar-control-and-button-styles.md) -Stil angeben, erstellt und verwaltet die Symbolleiste ein QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="42d34-105">When you specify the [**TBSTYLE\_TOOLTIPS**](toolbar-control-and-button-styles.md) style, the toolbar creates and manages a tooltip control.</span></span> <span data-ttu-id="42d34-106">Das QuickInfo-Steuerelement ist ausgeblendet und wird nur angezeigt, wenn Benutzer den Mauszeiger über eine Symbolleisten Schaltfläche bewegen und diese für ungefähr eine Sekunde belassen.</span><span class="sxs-lookup"><span data-stu-id="42d34-106">The tooltip control is hidden and appears only when users move the pointer over a toolbar button and leave it there for approximately one second.</span></span>

<span data-ttu-id="42d34-107">Die Anwendung kann Text für das QuickInfo-Steuerelement mit einer der folgenden Methoden bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="42d34-107">Your application can supply text to the tooltip control in any one of the following ways:</span></span>

-   <span data-ttu-id="42d34-108">Legen Sie den QuickInfo-Text für jede Schaltfläche als **IString** -Member der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="42d34-108">Set the tooltip text as the **iString** member of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure for each button.</span></span> <span data-ttu-id="42d34-109">Außerdem müssen Sie eine [**TB- \_ setmaxtextrows**](tb-setmaxtextrows.md) -Nachricht senden und die maximalen Textzeilen auf 0 festlegen, sodass der Text nicht als Schaltflächen Bezeichnung und nicht als QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="42d34-109">You must also send a [**TB\_SETMAXTEXTROWS**](tb-setmaxtextrows.md) message and set the maximum text rows to 0, so that the text does not appear as the button label rather than as a tooltip.</span></span>
-   <span data-ttu-id="42d34-110">Erstellen Sie die Symbolleiste mit dem [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil, und legen Sie dann den erweiterten Stil [**tbstyle \_ Ex \_ mixedbuttons**](toolbar-extended-styles.md) fest.</span><span class="sxs-lookup"><span data-stu-id="42d34-110">Create the toolbar with the [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style and then set the [**TBSTYLE\_EX\_MIXEDBUTTONS**](toolbar-extended-styles.md) extended style.</span></span> <span data-ttu-id="42d34-111">Bezeichnungen werden nur für Schaltflächen mit dem [**btns- \_ ShowText**](toolbar-control-and-button-styles.md) -Stil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42d34-111">Labels are shown only for buttons that have the [**BTNS\_SHOWTEXT**](toolbar-control-and-button-styles.md) style.</span></span> <span data-ttu-id="42d34-112">Für Schaltflächen, die nicht über diesen Stil verfügen, wird eine QuickInfo angezeigt, die den Schaltflächen Text enthält.</span><span class="sxs-lookup"><span data-stu-id="42d34-112">For buttons that do not have this style, a tooltip is shown that contains the button text.</span></span>
-   <span data-ttu-id="42d34-113">Reagieren Sie auf den [TTN \_ getdispinfo](ttn-getdispinfo.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="42d34-113">Respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification code.</span></span>
-   <span data-ttu-id="42d34-114">Reagieren Sie auf den [TBN- \_ getinfotip](tbn-getinfotip.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="42d34-114">Respond to the [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code.</span></span>

<span data-ttu-id="42d34-115">Eine Anwendung, die Nachrichten direkt an das ToolTip-Steuerelement senden muss, kann das Handle für das Steuerelement abrufen, indem die [**TB \_ gettooltips**](tb-gettooltips.md) -Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42d34-115">An application that needs to send messages directly to the tooltip control can retrieve the handle to the control by using the [**TB\_GETTOOLTIPS**](tb-gettooltips.md) message.</span></span> <span data-ttu-id="42d34-116">Eine Anwendung kann das ToolTip-Steuerelement einer Symbolleiste durch ein anderes QuickInfo-Steuerelement ersetzen, indem die [**TB- \_ SetToolTips**](tb-settooltips.md) -Nachricht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="42d34-116">An application can replace the tooltip control of a toolbar with another tooltip control by using the [**TB\_SETTOOLTIPS**](tb-settooltips.md) message.</span></span>

<span data-ttu-id="42d34-117">Die flexibelste Möglichkeit zum Bereitstellen von QuickInfo-Text ist die Reaktion auf den [TTN \_ getdispinfo](ttn-getdispinfo.md) -oder [TBN \_ getinfotip](tbn-getinfotip.md) -Benachrichtigungs Code, der vom Symbolleisten-Steuerelement in Form einer WM-Benachrichtigungs Meldung gesendet wird. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="42d34-117">The most flexible way of supplying tooltip text is to respond to the [TTN\_GETDISPINFO](ttn-getdispinfo.md) or [TBN\_GETINFOTIP](tbn-getinfotip.md) notification code sent by the toolbar control to its parent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="42d34-118">Für [TTN \_ getdispinfo](ttn-getdispinfo.md)enthält der *LPARAM* -Parameter einen Zeiger auf eine [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur (auch als **lptooltiptext** definiert), die den Befehls Bezeichner der Schaltfläche angibt, für die Hilfetext benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="42d34-118">For [TTN\_GETDISPINFO](ttn-getdispinfo.md), the *lParam* parameter includes a pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure (also defined as **LPTOOLTIPTEXT**) that specifies the command identifier of the button for which Help text is needed.</span></span> <span data-ttu-id="42d34-119">Dieser Bezeichner befindet sich im Member **nmttdispinfo. HDR. idfrom** .</span><span class="sxs-lookup"><span data-stu-id="42d34-119">This identifier is in the **NMTTDISPINFO.hdr.idFrom** member.</span></span> <span data-ttu-id="42d34-120">Eine Anwendung kann den Hilfetext in die Struktur kopieren, die Adresse einer Zeichenfolge angeben, die den Hilfetext enthält, oder den Instanzhandle und den Ressourcen Bezeichner einer Zeichen folgen Ressource angeben.</span><span class="sxs-lookup"><span data-stu-id="42d34-120">An application can copy the Help text to the structure, specify the address of a string containing the Help text, or specify the instance handle and resource identifier of a string resource.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="42d34-121">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="42d34-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="42d34-122">Technologien</span><span class="sxs-lookup"><span data-stu-id="42d34-122">Technologies</span></span>

-   [<span data-ttu-id="42d34-123">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="42d34-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="42d34-124">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="42d34-124">Prerequisites</span></span>

-   <span data-ttu-id="42d34-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="42d34-125">C/C++</span></span>
-   <span data-ttu-id="42d34-126">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="42d34-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="42d34-127">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="42d34-127">Instructions</span></span>

### <a name="display-a-tooltip-for-a-button"></a><span data-ttu-id="42d34-128">Anzeigen einer QuickInfo für eine Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="42d34-128">Display a Tooltip for a Button</span></span>

<span data-ttu-id="42d34-129">Der folgende Beispielcode behandelt den [TTN \_ getdispinfo-QuickInfo](ttn-getdispinfo.md) -Benachrichtigungs Code durch Bereitstellen von Text von Ressourcen bezeichtern.</span><span class="sxs-lookup"><span data-stu-id="42d34-129">The following example code handles the [TTN\_GETDISPINFO](ttn-getdispinfo.md) tooltip notification code by providing text from resource identifiers.</span></span>


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="42d34-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="42d34-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42d34-131">Verwenden von Symbolleisten</span><span class="sxs-lookup"><span data-stu-id="42d34-131">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="42d34-132">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="42d34-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




