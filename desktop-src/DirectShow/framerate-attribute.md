---
description: Das Framerate-Attribut gibt ein Framerate in Frames pro Sekunde an.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Framerate-Attribut (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957904"
---
# <a name="framerate-attribute-directshow"></a><span data-ttu-id="d2da1-103">Framerate-Attribut (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d2da1-103">framerate Attribute (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="d2da1-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="d2da1-104">\[Deprecated.</span></span> <span data-ttu-id="d2da1-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d2da1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d2da1-106">Das- `framerate` Attribut gibt einen Framerate in Frames pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="d2da1-106">The `framerate` attribute specifies a framerate, in frames per second.</span></span>

## <a name="possible-values"></a><span data-ttu-id="d2da1-107">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d2da1-107">Possible Values</span></span>

<span data-ttu-id="d2da1-108">Gleitkommawert.</span><span class="sxs-lookup"><span data-stu-id="d2da1-108">Floating-point value.</span></span> <span data-ttu-id="d2da1-109">Der Wert muss die führende Null vor der Dezimalstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="d2da1-109">The value must include the leading zero before the decimal place.</span></span> <span data-ttu-id="d2da1-110">Beispielsweise 0,3, nicht. 3.</span><span class="sxs-lookup"><span data-stu-id="d2da1-110">For example, 0.3, not .3.</span></span> <span data-ttu-id="d2da1-111">Verwenden Sie nicht mehr als sieben Dezimalziffern.</span><span class="sxs-lookup"><span data-stu-id="d2da1-111">Do not use more than seven decimal digits.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d2da1-112">Gilt für</span><span class="sxs-lookup"><span data-stu-id="d2da1-112">Applies To</span></span>

<span data-ttu-id="d2da1-113">[**Clip**](clip-element.md), [**Gruppe**](group-element.md), [**Zeitachse**](timeline-element.md)</span><span class="sxs-lookup"><span data-stu-id="d2da1-113">[**clip**](clip-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md)</span></span>

## <a name="remarks"></a><span data-ttu-id="d2da1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2da1-114">Remarks</span></span>

<span data-ttu-id="d2da1-115">Für das **Clip** -Element gibt dieses Attribut die Standardbildrate der Quelle an.</span><span class="sxs-lookup"><span data-stu-id="d2da1-115">For the **clip** element, this attribute specifies the default frame rate of the source.</span></span> <span data-ttu-id="d2da1-116">Geben Sie das-Attribut für weiterhin Bilder und DIB-Sequenzen an.</span><span class="sxs-lookup"><span data-stu-id="d2da1-116">Specify the attribute for still images andDIB sequences.</span></span> <span data-ttu-id="d2da1-117">Legen Sie für ein Image den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="d2da1-117">For a still image, set the value to zero.</span></span> <span data-ttu-id="d2da1-118">Verwenden Sie für eine DIB-Sequenz einen Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d2da1-118">For a DIB sequence, use a nonzero value.</span></span> <span data-ttu-id="d2da1-119">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d2da1-119">The default value is zero.</span></span>

<span data-ttu-id="d2da1-120">Für das **Group** -Element gibt dieses Attribut die Ausgabe Frame Rate für die Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="d2da1-120">For the **group** element, this attribute specifies the output frame rate for the group.</span></span>

<span data-ttu-id="d2da1-121">Für das **Timeline** -Element gibt dieses Attribut die Standardbildrate für alle Gruppen an.</span><span class="sxs-lookup"><span data-stu-id="d2da1-121">For the **timeline** element, this attribute specifies the default frame rate for all groups.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2da1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2da1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2da1-123">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="d2da1-123">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2da1-124">**Iamtimelinesrc:: setdefaultfps**</span><span class="sxs-lookup"><span data-stu-id="d2da1-124">**IAMTimelineSrc::SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[<span data-ttu-id="d2da1-125">**Iamtimelinegroup:: setoutputfps**</span><span class="sxs-lookup"><span data-stu-id="d2da1-125">**IAMTimelineGroup::SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[<span data-ttu-id="d2da1-126">**Iamtimeline:: setdefaultfps**</span><span class="sxs-lookup"><span data-stu-id="d2da1-126">**IAMTimeline::SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



