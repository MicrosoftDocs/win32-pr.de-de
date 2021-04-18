---
title: WMT_VIDEOIMAGE_TRANSITION_CIRCLE (wmsdkidl. h)
description: Der Kreis Übergang zeigt das neue Bild in einem Kreis.
ms.assetid: ba3bcf46-1254-4aad-a958-0f9ddb2f40dc
keywords:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf3a8eff2ca5a5069fa01c4e61bc0735808fd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364556"
---
# <a name="wmt_videoimage_transition_circle"></a><span data-ttu-id="7f6d2-104">WMT \_ Videoimage- \_ Übergangs \_ Kreis</span><span class="sxs-lookup"><span data-stu-id="7f6d2-104">WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE</span></span>

<span data-ttu-id="7f6d2-105">Der Kreis Übergang zeigt das neue Bild in einem Kreis.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-105">The circle transition reveals the new image in a circle.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f6d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f6d2-106">Parameters</span></span>

<span data-ttu-id="7f6d2-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f6d2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f6d2-108">Parameter</span></span></th>
<th><span data-ttu-id="7f6d2-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="7f6d2-109">Structure member</span></span></th>
<th><span data-ttu-id="7f6d2-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f6d2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f6d2-111">X zentrieren</span><span class="sxs-lookup"><span data-stu-id="7f6d2-111">Center X</span></span></td>
<td><span data-ttu-id="7f6d2-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="7f6d2-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="7f6d2-113">X-Koordinate relativ zum Videorahmen der Mitte des Kreises.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-113">X-coordinate, relative to the video frame, of the center of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f6d2-114">Y zentrieren</span><span class="sxs-lookup"><span data-stu-id="7f6d2-114">Center Y</span></span></td>
<td><span data-ttu-id="7f6d2-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="7f6d2-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="7f6d2-116">Y-Koordinate relativ zum Videorahmen der Mitte des Kreises.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-116">Y-coordinate, relative to the video frame, of center of the circle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f6d2-117">Radius</span><span class="sxs-lookup"><span data-stu-id="7f6d2-117">Radius</span></span></td>
<td><span data-ttu-id="7f6d2-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="7f6d2-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="7f6d2-119">RADIUS (in Pixel) des Kreises.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-119">Radius, in pixels, of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f6d2-120">Aufbau</span><span class="sxs-lookup"><span data-stu-id="7f6d2-120">Composition</span></span></td>
<td><span data-ttu-id="7f6d2-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="7f6d2-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="7f6d2-122">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="7f6d2-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="7f6d2-123">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="7f6d2-124">1: gibt eine umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="7f6d2-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f6d2-125">Requirements</span></span>



| <span data-ttu-id="7f6d2-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f6d2-126">Requirement</span></span> | <span data-ttu-id="7f6d2-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7f6d2-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6d2-128">Header</span><span class="sxs-lookup"><span data-stu-id="7f6d2-128">Header</span></span><br/> | <dl> <span data-ttu-id="7f6d2-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f6d2-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f6d2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f6d2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6d2-131">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="7f6d2-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





