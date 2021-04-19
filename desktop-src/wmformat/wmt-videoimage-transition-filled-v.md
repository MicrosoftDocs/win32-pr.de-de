---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (wmsdkidl. h)
description: Der erfüllte V-Übergang zeigt das neue Bild in einem Dreieck an, das von einer Seite des Frames stammt.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353825"
---
# <a name="wmt_videoimage_transition_filled_v"></a><span data-ttu-id="87cc6-104">WMT \_ Videoimage- \_ Übergang mit \_ ausgefülltem \_ V</span><span class="sxs-lookup"><span data-stu-id="87cc6-104">WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V</span></span>

<span data-ttu-id="87cc6-105">Der erfüllte V-Übergang zeigt das neue Bild in einem Dreieck an, das von einer Seite des Frames stammt.</span><span class="sxs-lookup"><span data-stu-id="87cc6-105">The filled V transition reveals the new image in a triangle originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="87cc6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87cc6-106">Parameters</span></span>

<span data-ttu-id="87cc6-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="87cc6-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87cc6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="87cc6-108">Parameter</span></span></th>
<th><span data-ttu-id="87cc6-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="87cc6-109">Structure member</span></span></th>
<th><span data-ttu-id="87cc6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87cc6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87cc6-111">Breite</span><span class="sxs-lookup"><span data-stu-id="87cc6-111">Width</span></span></td>
<td><span data-ttu-id="87cc6-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="87cc6-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="87cc6-113">Breite des gefüllten V in Pixel.</span><span class="sxs-lookup"><span data-stu-id="87cc6-113">Width of the filled V in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87cc6-114">Höhe</span><span class="sxs-lookup"><span data-stu-id="87cc6-114">Height</span></span></td>
<td><span data-ttu-id="87cc6-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="87cc6-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="87cc6-116">Höhe des gefüllten V in Pixel.</span><span class="sxs-lookup"><span data-stu-id="87cc6-116">Height of the filled V in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87cc6-117">Richtung</span><span class="sxs-lookup"><span data-stu-id="87cc6-117">Direction</span></span></td>
<td><span data-ttu-id="87cc6-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="87cc6-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="87cc6-119">Die Richtung, aus der das gefüllte V stammt. Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="87cc6-119">Direction from which the filled V originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="87cc6-120">0-gibt von der linken Seite des Frames aus.</span><span class="sxs-lookup"><span data-stu-id="87cc6-120">0 - Enters from the left side of the frame.</span></span></li>
<li><span data-ttu-id="87cc6-121">1: gibt von der rechten Seite des Frames aus.</span><span class="sxs-lookup"><span data-stu-id="87cc6-121">1 - Enters from the right side of the frame.</span></span></li>
<li><span data-ttu-id="87cc6-122">2: gibt vom unteren Rand des Frames aus.</span><span class="sxs-lookup"><span data-stu-id="87cc6-122">2 - Enters from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="87cc6-123">3: geht vom oberen Rand des Frames aus.</span><span class="sxs-lookup"><span data-stu-id="87cc6-123">3 - Enters from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87cc6-124">Aufbau</span><span class="sxs-lookup"><span data-stu-id="87cc6-124">Composition</span></span></td>
<td><span data-ttu-id="87cc6-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="87cc6-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="87cc6-126">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="87cc6-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="87cc6-127">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="87cc6-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="87cc6-128">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="87cc6-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="87cc6-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87cc6-129">Requirements</span></span>



| <span data-ttu-id="87cc6-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87cc6-130">Requirement</span></span> | <span data-ttu-id="87cc6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="87cc6-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87cc6-132">Header</span><span class="sxs-lookup"><span data-stu-id="87cc6-132">Header</span></span><br/> | <dl> <span data-ttu-id="87cc6-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87cc6-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87cc6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87cc6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cc6-135">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="87cc6-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





