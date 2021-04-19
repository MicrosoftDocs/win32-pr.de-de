---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (wmsdkidl. h)
description: Der geteilte Übergang zeigt das neue Bild durch Aufteilen des alten Bilds an. Die Teilung wird entlang einer geraden horizontalen oder vertikalen Linie angezeigt, beginnend innerhalb des Frames.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366061"
---
# <a name="wmt_videoimage_transition_split"></a><span data-ttu-id="a6bd7-105">Teilung des WMT \_ Videoimage- \_ Übergangs \_</span><span class="sxs-lookup"><span data-stu-id="a6bd7-105">WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT</span></span>

<span data-ttu-id="a6bd7-106">Der geteilte Übergang zeigt das neue Bild durch Aufteilen des alten Bilds an.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-106">The split transition reveals the new image by splitting the old image.</span></span> <span data-ttu-id="a6bd7-107">Die Teilung wird entlang einer geraden horizontalen oder vertikalen Linie angezeigt, beginnend innerhalb des Frames.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-107">The split appears along a straight horizontal or vertical line starting inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6bd7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6bd7-108">Parameters</span></span>

<span data-ttu-id="a6bd7-109">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6bd7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6bd7-110">Parameter</span></span></th>
<th><span data-ttu-id="a6bd7-111">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="a6bd7-111">Structure member</span></span></th>
<th><span data-ttu-id="a6bd7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6bd7-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a6bd7-113">X zentrieren</span><span class="sxs-lookup"><span data-stu-id="a6bd7-113">Center X</span></span></td>
<td><span data-ttu-id="a6bd7-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="a6bd7-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="a6bd7-115">X-Koordinate der Ursprungs Zeile der Teilung relativ zum Videorahmen.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-115">X-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6bd7-116">Y zentrieren</span><span class="sxs-lookup"><span data-stu-id="a6bd7-116">Center Y</span></span></td>
<td><span data-ttu-id="a6bd7-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="a6bd7-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="a6bd7-118">Die Y-Koordinate der Ursprungs Zeile der Teilung relativ zum Videorahmen.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-118">Y-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6bd7-119">Entfernung</span><span class="sxs-lookup"><span data-stu-id="a6bd7-119">Distance</span></span></td>
<td><span data-ttu-id="a6bd7-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="a6bd7-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="a6bd7-121">Breite der Aufteilung in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-121">Width of the split in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6bd7-122">Richtung</span><span class="sxs-lookup"><span data-stu-id="a6bd7-122">Direction</span></span></td>
<td><span data-ttu-id="a6bd7-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="a6bd7-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="a6bd7-124">Die Ausrichtung der Aufteilung. Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="a6bd7-124">Orientation of the split.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="a6bd7-125">0-unterteilt entlang einer horizontalen Linie.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-125">0 - Splits along a horizontal line.</span></span></li>
<li><span data-ttu-id="a6bd7-126">1-unterteilt entlang einer vertikalen Linie.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-126">1 - Splits along a vertical line.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6bd7-127">Aufbau</span><span class="sxs-lookup"><span data-stu-id="a6bd7-127">Composition</span></span></td>
<td><span data-ttu-id="a6bd7-128"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="a6bd7-128"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="a6bd7-129">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="a6bd7-129">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="a6bd7-130">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-130">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="a6bd7-131">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="a6bd7-131">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a6bd7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6bd7-132">Requirements</span></span>



| <span data-ttu-id="a6bd7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6bd7-133">Requirement</span></span> | <span data-ttu-id="a6bd7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="a6bd7-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bd7-135">Header</span><span class="sxs-lookup"><span data-stu-id="a6bd7-135">Header</span></span><br/> | <dl> <span data-ttu-id="a6bd7-136"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6bd7-136"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6bd7-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6bd7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6bd7-138">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="a6bd7-138">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





