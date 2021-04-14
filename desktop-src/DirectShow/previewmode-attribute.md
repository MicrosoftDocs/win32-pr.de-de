---
description: Das PreviewMode-Attribut gibt den Vorschaumodus für die Gruppe an. Wenn der Wert true ist, können Frames während der Vorschau gelöscht werden. Andernfalls werden während der Vorschau keine Frames gelöscht. Der Standardwert ist TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: PreviewMode-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392601"
---
# <a name="previewmode-attribute"></a><span data-ttu-id="53363-106">PreviewMode-Attribut</span><span class="sxs-lookup"><span data-stu-id="53363-106">previewmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="53363-107">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="53363-107">\[Deprecated.</span></span> <span data-ttu-id="53363-108">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="53363-108">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53363-109">Das- `previewmode` Attribut gibt den Vorschaumodus für die Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="53363-109">The `previewmode` attribute specifies the preview mode for the group.</span></span> <span data-ttu-id="53363-110">Wenn der Wert **true** ist, können Frames während der Vorschau gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="53363-110">If the value is **TRUE**, frames might be dropped during preview.</span></span> <span data-ttu-id="53363-111">Andernfalls werden während der Vorschau keine Frames gelöscht.</span><span class="sxs-lookup"><span data-stu-id="53363-111">Otherwise, no frames are dropped during preview.</span></span> <span data-ttu-id="53363-112">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="53363-112">The default value is **TRUE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="53363-113">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="53363-113">Possible Values</span></span>

<span data-ttu-id="53363-114">Die folgenden Werte sind als true definiert: y, y, t, t, 1.</span><span class="sxs-lookup"><span data-stu-id="53363-114">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="53363-115">Die folgenden Werte sind als false definiert: n, n, f, f, 0 (null).</span><span class="sxs-lookup"><span data-stu-id="53363-115">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="53363-116">Gilt für</span><span class="sxs-lookup"><span data-stu-id="53363-116">Applies To</span></span>

[<span data-ttu-id="53363-117">**Kreis**</span><span class="sxs-lookup"><span data-stu-id="53363-117">**group**</span></span>](group-element.md)

## <a name="remarks"></a><span data-ttu-id="53363-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53363-118">Remarks</span></span>

<span data-ttu-id="53363-119">In der Standardeinstellung werden Frames beim Anzeigen der Vorschau von langsamen Effekten oder Übergängen gelöscht, damit das Video mit der Audiodatei synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="53363-119">Under the default setting, frames are dropped while previewing slow effects or transitions, to keep the video synchronized with the audio.</span></span> <span data-ttu-id="53363-120">Das Video könnte als Ergebnis aussehen.</span><span class="sxs-lookup"><span data-stu-id="53363-120">The video might look choppy as a result.</span></span> <span data-ttu-id="53363-121">Wenn dieses Attribut auf " **false** " festgelegt wird, wird jedes Frame während der Vorschau angezeigt, was dazu führen kann, dass das Video nicht mehr mit dem Audioformat synchronisiert wird</span><span class="sxs-lookup"><span data-stu-id="53363-121">Setting this attribute to **FALSE** forces every frame to render during preview, possibly resulting in the video becoming out of sync with the audio.</span></span> <span data-ttu-id="53363-122">Rahmen werden beim Schreiben in eine Datei nie gelöscht.</span><span class="sxs-lookup"><span data-stu-id="53363-122">Frames are never dropped when writing to a file.</span></span>

## <a name="see-also"></a><span data-ttu-id="53363-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53363-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53363-124">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="53363-124">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="53363-125">**Iamtimelinegroup:: SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="53363-125">**IAMTimelineGroup::SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



