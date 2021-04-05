---
title: Implementieren von Quick Infos zur Sprechblase
description: Quick Infos für die Sprechblase ähneln Standard-Quick Infos, werden aber in einem Zeichenstil \ 0034; Sprechblase \ 0034; angezeigt. mit einem stem, das auf das Tool zeigt.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708669"
---
# <a name="how-to-implement-balloon-tooltips"></a><span data-ttu-id="8e823-103">Implementieren von Quick Infos zur Sprechblase</span><span class="sxs-lookup"><span data-stu-id="8e823-103">How to Implement Balloon Tooltips</span></span>

<span data-ttu-id="8e823-104">Quick Infos für die Sprechblase ähneln Standard-Quick Infos, werden jedoch in einer "Sprechblase" im Zeichenstil angezeigt, wobei ein stem auf das Tool zeigt.</span><span class="sxs-lookup"><span data-stu-id="8e823-104">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="8e823-105">Quick Infos für die Sprechblase können entweder einzeilige oder mehrzeilige Zeilen sein.</span><span class="sxs-lookup"><span data-stu-id="8e823-105">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="8e823-106">Sie werden auf die gleiche Weise wie Standard-Quick Infos erstellt und behandelt.</span><span class="sxs-lookup"><span data-stu-id="8e823-106">They are created and handled in much the same way as standard tooltips.</span></span>

<span data-ttu-id="8e823-107">Die Standardposition des Stamms und des Rechtecks wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8e823-107">The default position of the stem and rectangle is shown in the following illustration.</span></span> <span data-ttu-id="8e823-108">Wenn das Tool zu nah am oberen Rand des Bildschirms ist, wird die QuickInfo unterhalb des Tool Rechtecks angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e823-108">If the tool is too close to the top of the screen, the tooltip appears below and to the right of the tool's rectangle.</span></span> <span data-ttu-id="8e823-109">Wenn das Tool zu nah am rechten Bildschirmrand ist, gelten ähnliche Prinzipien, aber die QuickInfo wird auf der linken Seite des Tool Rechtecks angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e823-109">If the tool is too close to the right side of the screen, similar principles apply, but the tooltip appears to the left of the tool's rectangle.</span></span>

![Screenshot eines Dialog Felds eine QuickInfo-Sprechblase mit einer Textzeile wird oberhalb und rechts neben dem Ziel angezeigt.](images/tt-balloon.png)

<span data-ttu-id="8e823-111">Sie können die Standard Positionierung ändern, indem Sie das Steuerelement " **ttf \_ centertip** " im **uFlags** -Member der QuickInfo-Struktur " [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="8e823-111">You can change the default positioning by setting the **TTF\_CENTERTIP** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="8e823-112">In diesem Fall verweist das stem normalerweise auf den Mittelpunkt des unteren Randes des Tool Rechtecks, und das Text Rechteck wird direkt unterhalb des Tools angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e823-112">In that case, the stem normally points to the center of the lower edge of the tool's rectangle, and the text rectangle is displayed directly below the tool.</span></span> <span data-ttu-id="8e823-113">Der Stamm wird an das Text Rechteck in der Mitte des oberen Rands angefügt.</span><span class="sxs-lookup"><span data-stu-id="8e823-113">The stem attaches to the text rectangle at the center of the upper edge.</span></span> <span data-ttu-id="8e823-114">Wenn das Tool zu nah am unteren Bildschirmrand ist, wird das Text Rechteck oberhalb des Tools zentriert, und der Stamm wird an die Mitte des unteren Rands angefügt.</span><span class="sxs-lookup"><span data-stu-id="8e823-114">If the tool is too close to the bottom of the screen, the text rectangle is centered above the tool, and the stem attaches to the center of the lower edge.</span></span>

<span data-ttu-id="8e823-115">Die folgende Abbildung zeigt eine QuickInfo, die sich auf das Tool konzentriert.</span><span class="sxs-lookup"><span data-stu-id="8e823-115">The following illustration shows a tooltip that is centered on the tool.</span></span>

![Screenshot eines Dialog Felds eine QuickInfo-Sprechblase mit einer Textzeile wird unter dem Ziel zentriert angezeigt](images/tt-ballooncenter.png)

<span data-ttu-id="8e823-117">Wenn Sie den Speicherort der Stamm Punkte angeben möchten, legen Sie das " **ttf \_ Track** "-Flag im **uFlags** -Member der ToolTip- [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="8e823-117">If you want to specify where the stem points, set the **TTF\_TRACK** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="8e823-118">Anschließend geben Sie die Koordinate an, indem Sie eine [**TTM \_ trackposition**](ttm-trackposition.md) -Nachricht mit den x-und y-Koordinaten im *LPARAM* -Wert senden.</span><span class="sxs-lookup"><span data-stu-id="8e823-118">You then specify the coordinate by sending a [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message, with the x- and y-coordinates in the *lParam* value.</span></span> <span data-ttu-id="8e823-119">Wenn **ttf \_ centertip** ebenfalls festgelegt ist, zeigt das Stamm Modul immer noch auf die Position, die von der **TTM \_ trackposition** -Nachricht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e823-119">If **TTF\_CENTERTIP** is also set, the stem still points to the position specified by the **TTM\_TRACKPOSITION** message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8e823-120">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="8e823-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8e823-121">Technologien</span><span class="sxs-lookup"><span data-stu-id="8e823-121">Technologies</span></span>

-   [<span data-ttu-id="8e823-122">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="8e823-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8e823-123">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8e823-123">Prerequisites</span></span>

-   <span data-ttu-id="8e823-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="8e823-124">C/C++</span></span>
-   <span data-ttu-id="8e823-125">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="8e823-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8e823-126">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="8e823-126">Instructions</span></span>

### <a name="implement-balloon-tooltips"></a><span data-ttu-id="8e823-127">Tooltipps für die Sprechblase implementieren</span><span class="sxs-lookup"><span data-stu-id="8e823-127">Implement Balloon Tooltips</span></span>

<span data-ttu-id="8e823-128">Im folgenden Beispielcode wird veranschaulicht, wie Sie eine zentrierte Sprechblasen-QuickInfo **mit dem Steuer \_** Element Stil der QuickInfo-Sprechblase implementieren</span><span class="sxs-lookup"><span data-stu-id="8e823-128">The following example code shows how to implement a centered balloon tooltip by using the **TTS\_BALLOON** tooltip control style.</span></span>


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a><span data-ttu-id="8e823-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e823-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e823-130">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="8e823-130">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> <dt>

[<span data-ttu-id="8e823-131">**QuickInfo-Stile**</span><span class="sxs-lookup"><span data-stu-id="8e823-131">**Tooltip Styles**</span></span>](tooltip-styles.md)
</dt> </dl>

 

 




