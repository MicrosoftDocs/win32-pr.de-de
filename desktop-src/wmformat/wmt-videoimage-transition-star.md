---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (wmsdkidl. h)
description: Der Stern Übergang zeigt das neue Bild auf einem fünf-Spitzen-Stern innerhalb des Frames.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364689"
---
# <a name="wmt_videoimage_transition_star"></a><span data-ttu-id="6eb4e-104">WMT \_ Videoimage \_ \_ -Übergangs Stern</span><span class="sxs-lookup"><span data-stu-id="6eb4e-104">WMT\_VIDEOIMAGE\_TRANSITION\_STAR</span></span>

<span data-ttu-id="6eb4e-105">Der Stern Übergang zeigt das neue Bild auf einem fünf-Spitzen-Stern innerhalb des Frames.</span><span class="sxs-lookup"><span data-stu-id="6eb4e-105">The star transition reveals the new image in a five-pointed star inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="6eb4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6eb4e-106">Parameters</span></span>

<span data-ttu-id="6eb4e-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6eb4e-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6eb4e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6eb4e-108">Parameter</span></span></th>
<th><span data-ttu-id="6eb4e-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="6eb4e-109">Structure member</span></span></th>
<th><span data-ttu-id="6eb4e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6eb4e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6eb4e-111">X zentrieren</span><span class="sxs-lookup"><span data-stu-id="6eb4e-111">Center X</span></span></td>
<td><span data-ttu-id="6eb4e-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="6eb4e-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="6eb4e-113">X-Koordinate relativ zum Videorahmen der Mitte des Sterns.</span><span class="sxs-lookup"><span data-stu-id="6eb4e-113">X-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eb4e-114">Y zentrieren</span><span class="sxs-lookup"><span data-stu-id="6eb4e-114">Center Y</span></span></td>
<td><span data-ttu-id="6eb4e-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="6eb4e-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="6eb4e-116">Y-Koordinate relativ zum Videorahmen der Mitte des Sterns.</span><span class="sxs-lookup"><span data-stu-id="6eb4e-116">Y-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6eb4e-117">Radius</span><span class="sxs-lookup"><span data-stu-id="6eb4e-117">Radius</span></span></td>
<td><span data-ttu-id="6eb4e-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="6eb4e-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="6eb4e-119">Der RADIUS (in Pixel) des Kreises, der durch die Punkte des Sterns definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6eb4e-119">Radius, in pixels, of the circle defined by the points of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6eb4e-120">Aufbau</span><span class="sxs-lookup"><span data-stu-id="6eb4e-120">Composition</span></span></td>
<td><span data-ttu-id="6eb4e-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="6eb4e-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="6eb4e-122">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="6eb4e-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="6eb4e-123">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="6eb4e-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="6eb4e-124">1: gibt eine umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="6eb4e-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="6eb4e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6eb4e-125">Requirements</span></span>



| <span data-ttu-id="6eb4e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6eb4e-126">Requirement</span></span> | <span data-ttu-id="6eb4e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6eb4e-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb4e-128">Header</span><span class="sxs-lookup"><span data-stu-id="6eb4e-128">Header</span></span><br/> | <dl> <span data-ttu-id="6eb4e-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb4e-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb4e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6eb4e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb4e-131">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="6eb4e-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





