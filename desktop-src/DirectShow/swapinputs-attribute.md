---
description: Das swapinputs-Attribut gibt an, ob Übergangs Eingaben ausgetauscht werden sollen. Wenn der Wert true ist, werden die Eingaben ausgetauscht. Der Standardwert ist FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Attribut "Swap-Eingaben"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349068"
---
# <a name="swapinputs-attribute"></a><span data-ttu-id="325cc-105">Attribut "Swap-Eingaben"</span><span class="sxs-lookup"><span data-stu-id="325cc-105">swapinputs Attribute</span></span>

> [!Note]  
> <span data-ttu-id="325cc-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="325cc-106">\[Deprecated.</span></span> <span data-ttu-id="325cc-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="325cc-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="325cc-108">Das- `swapinputs` Attribut gibt an, ob Übergangs Eingaben ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="325cc-108">The `swapinputs` attribute specifies whether to swap transition inputs.</span></span> <span data-ttu-id="325cc-109">Wenn der Wert **true** ist, werden die Eingaben ausgetauscht.</span><span class="sxs-lookup"><span data-stu-id="325cc-109">If the value is **TRUE**, the inputs are swapped.</span></span> <span data-ttu-id="325cc-110">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="325cc-110">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="325cc-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="325cc-111">Possible Values</span></span>

<span data-ttu-id="325cc-112">Die folgenden Werte sind als true definiert: y, y, t, t, 1.</span><span class="sxs-lookup"><span data-stu-id="325cc-112">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="325cc-113">Die folgenden Werte sind als false definiert: n, n, f, f, 0 (null).</span><span class="sxs-lookup"><span data-stu-id="325cc-113">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="325cc-114">Gilt für</span><span class="sxs-lookup"><span data-stu-id="325cc-114">Applies To</span></span>

[<span data-ttu-id="325cc-115">**Übergang**</span><span class="sxs-lookup"><span data-stu-id="325cc-115">**transition**</span></span>](transition-element.md)

## <a name="remarks"></a><span data-ttu-id="325cc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="325cc-116">Remarks</span></span>

<span data-ttu-id="325cc-117">Standardmäßig verläuft ein Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zur Ebene, auf der sich der Übergang befindet.</span><span class="sxs-lookup"><span data-stu-id="325cc-117">By default, a transition proceeds from the composite of all lower-priority layers to the layer on which the transition resides.</span></span> <span data-ttu-id="325cc-118">Wenn das- `swapinputs` Attribut 1 ist, wird diese Richtung umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="325cc-118">If the `swapinputs` attribute is 1, this direction is reversed.</span></span> <span data-ttu-id="325cc-119">Weitere Informationen zum von des verwendeten Ebenenmodell finden Sie [im Zeitachsen Modell](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="325cc-119">For more information about the layering model used by DES, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="325cc-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="325cc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325cc-121">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="325cc-121">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="325cc-122">**Iamtimelinetrans::-wapinputs**</span><span class="sxs-lookup"><span data-stu-id="325cc-122">**IAMTimelineTrans::SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



