---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (wmsdkidl. h)
description: Der radübergang zeigt das neue Bild durch Drehen von vier Zeilen um einen gemeinsamen Pivotpunkt, wie z. b. die Spokes eines Rades.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369310"
---
# <a name="wmt_videoimage_transition_wheel"></a><span data-ttu-id="9b0a1-104">WMT \_ Videoimage- \_ Übergangs \_ Rad</span><span class="sxs-lookup"><span data-stu-id="9b0a1-104">WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL</span></span>

<span data-ttu-id="9b0a1-105">Der radübergang zeigt das neue Bild durch Drehen von vier Zeilen um einen gemeinsamen Pivotpunkt, wie z. b. die Spokes eines Rades.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-105">The wheel transition reveals the new image by rotating four lines around a common pivot point, like the spokes of a wheel.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b0a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b0a1-106">Parameters</span></span>

<span data-ttu-id="9b0a1-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b0a1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b0a1-108">Parameter</span></span></th>
<th><span data-ttu-id="9b0a1-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="9b0a1-109">Structure member</span></span></th>
<th><span data-ttu-id="9b0a1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b0a1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b0a1-111">X zentrieren</span><span class="sxs-lookup"><span data-stu-id="9b0a1-111">Center X</span></span></td>
<td><span data-ttu-id="9b0a1-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="9b0a1-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="9b0a1-113">X-Koordinate relativ zum Videorahmen der Mitte des radeffekts.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-113">X-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b0a1-114">Y zentrieren</span><span class="sxs-lookup"><span data-stu-id="9b0a1-114">Center Y</span></span></td>
<td><span data-ttu-id="9b0a1-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="9b0a1-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="9b0a1-116">Y-Koordinate relativ zum Videorahmen der Mitte des radeffekts.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-116">Y-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b0a1-117">Angle</span><span class="sxs-lookup"><span data-stu-id="9b0a1-117">Angle</span></span></td>
<td><span data-ttu-id="9b0a1-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="9b0a1-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="9b0a1-119">Der Drehwinkel für die Spokes des radeffekts in Grad.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-119">Angle of rotation, in degrees, of the spokes of the wheel effect.</span></span> <span data-ttu-id="9b0a1-120">Der Wert 0,0 gibt das alte Bild an, ohne dass ein neues Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-120">A value of 0.0 indicates the old image without any of the new image revealed.</span></span> <span data-ttu-id="9b0a1-121">Der Wert 90,0 gibt an, dass das neue Bild vollständig offengelegt ist. Die Verschiebung von 0,0 zu 90,0 wird als Drehung im Uhrzeigersinn der Spokes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-121">A value of 90.0 indicates the new image fully revealed.Movement from 0.0 to 90.0 appears as clockwise rotation of the spokes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b0a1-122">Aufbau</span><span class="sxs-lookup"><span data-stu-id="9b0a1-122">Composition</span></span></td>
<td><span data-ttu-id="9b0a1-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="9b0a1-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="9b0a1-124">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="9b0a1-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="9b0a1-125">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="9b0a1-126">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="9b0a1-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9b0a1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b0a1-127">Requirements</span></span>



| <span data-ttu-id="9b0a1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b0a1-128">Requirement</span></span> | <span data-ttu-id="9b0a1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9b0a1-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0a1-130">Header</span><span class="sxs-lookup"><span data-stu-id="9b0a1-130">Header</span></span><br/> | <dl> <span data-ttu-id="9b0a1-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b0a1-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b0a1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b0a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b0a1-133">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="9b0a1-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





