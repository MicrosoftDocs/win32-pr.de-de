---
description: Vorschau von Effekten und Übergängen
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Vorschau von Effekten und Übergängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125078"
---
# <a name="previewing-effects-and-transitions"></a><span data-ttu-id="3323a-103">Vorschau von Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="3323a-103">Previewing Effects and Transitions</span></span>

<span data-ttu-id="3323a-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="3323a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3323a-105">Einige Effekte und Übergänge nehmen zum Rendervorgang relativ lange Zeit in Anspruch.</span><span class="sxs-lookup"><span data-stu-id="3323a-105">Some effects and transitions take a relatively long time to render.</span></span> <span data-ttu-id="3323a-106">Während der Vorschau kann dies dazu führen, dass das Video mit der Audiodatei nicht mehr synchron ist.</span><span class="sxs-lookup"><span data-stu-id="3323a-106">During preview this can cause the video to become choppy or out of sync with the audio.</span></span> <span data-ttu-id="3323a-107">Sie können die Vorschau Geschwindigkeit erhöhen, indem Sie Effekte oder Übergänge deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="3323a-107">You can increase preview speed by disabling effects or transitions:</span></span>

-   <span data-ttu-id="3323a-108">Um alle Effekte zu deaktivieren, nennen Sie [**iamtimeline:: enableeffects**](iamtimeline-enableeffects.md).</span><span class="sxs-lookup"><span data-stu-id="3323a-108">To disable all effects, call [**IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).</span></span>
-   <span data-ttu-id="3323a-109">Um alle Übergänge zu deaktivieren, nennen Sie [**iamtimeline:: enabletransitions**](iamtimeline-enabletransitions.md).</span><span class="sxs-lookup"><span data-stu-id="3323a-109">To disable all transitions, call [**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).</span></span>
-   <span data-ttu-id="3323a-110">Um einen bestimmten Übergang zu deaktivieren, nennen Sie [**iamtimelinetrans:: setcutsonly**](iamtimelinetrans-setcutsonly.md).</span><span class="sxs-lookup"><span data-stu-id="3323a-110">To disable a particular transition, call [**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span></span>

<span data-ttu-id="3323a-111">Wenn Effekte deaktiviert sind, werden Sie während der Vorschau nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="3323a-111">When effects are disabled, they are not rendered during preview.</span></span> <span data-ttu-id="3323a-112">Wenn ein Übergang deaktiviert ist, wird er als Sprung Ausschneide gerendert.</span><span class="sxs-lookup"><span data-stu-id="3323a-112">When a transition is disabled, it is rendered as a jump cut.</span></span> <span data-ttu-id="3323a-113">Der segue zwischen den Spuren tritt immer noch auf, aber der visuelle Effekt wird nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="3323a-113">The segue between tracks still occurs, but the visual effect is not rendered.</span></span>

<span data-ttu-id="3323a-114">Wenn ein Effekt oder Übergang nicht gerendert werden kann, ersetzt die Renderengine einen Standardeffekt oder-Übergang.</span><span class="sxs-lookup"><span data-stu-id="3323a-114">If an effect or transition cannot be rendered, the render engine substitutes a default effect or transition.</span></span> <span data-ttu-id="3323a-115">Aufrufen der [**iamtimeline:: setdefaulteffect**](iamtimeline-setdefaulteffect.md) -Methode zum Festlegen des Standard Effekts und der [**iamtimeline:: setdefaulttransition**](iamtimeline-setdefaulttransition.md) -Methode, um den Standard Übergang festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3323a-115">Call the [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) method to set the default effect, and the [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) method to set the default transition.</span></span> <span data-ttu-id="3323a-116">Wenn Sie keinen Standardwert angeben, oder wenn der von Ihnen angegebene Wert auch einen Fehler verursacht, verwendet des einen eigenen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="3323a-116">If you do not specify a default, or if the one you specify also causes an error, DES uses its own default.</span></span>

> [!Note]  
> <span data-ttu-id="3323a-117">Sie können auch die Vorschau Qualität verbessern, indem Sie den Umfang der Rahmen Pufferung erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3323a-117">You can also improve preview quality by increasing the amount of frame buffering.</span></span> <span data-ttu-id="3323a-118">Weitere Informationen finden Sie unter [**iamtimelinegroup:: setoutputbuffering.**](iamtimelinegroup-setoutputbuffering.md)</span><span class="sxs-lookup"><span data-stu-id="3323a-118">See [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3323a-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3323a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3323a-120">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="3323a-120">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



