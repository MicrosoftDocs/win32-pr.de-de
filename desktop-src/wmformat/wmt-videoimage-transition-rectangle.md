---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (wmsdkidl. h)
description: Der Rechteck Übergang zeigt das neue Bild in einem Rechteck innerhalb des Rahmens an.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356021"
---
# <a name="wmt_videoimage_transition_rectangle"></a><span data-ttu-id="67aa9-104">WMT \_ Videoimage- \_ Übergangs \_ Rechteck</span><span class="sxs-lookup"><span data-stu-id="67aa9-104">WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE</span></span>

<span data-ttu-id="67aa9-105">Der Rechteck Übergang zeigt das neue Bild in einem Rechteck innerhalb des Rahmens an.</span><span class="sxs-lookup"><span data-stu-id="67aa9-105">The rectangle transition reveals the new image in a rectangle within the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="67aa9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67aa9-106">Parameters</span></span>

<span data-ttu-id="67aa9-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="67aa9-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67aa9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="67aa9-108">Parameter</span></span></th>
<th><span data-ttu-id="67aa9-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="67aa9-109">Structure member</span></span></th>
<th><span data-ttu-id="67aa9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67aa9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67aa9-111">X zentrieren</span><span class="sxs-lookup"><span data-stu-id="67aa9-111">Center X</span></span></td>
<td><span data-ttu-id="67aa9-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="67aa9-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="67aa9-113">X-Koordinate relativ zum Videorahmen der Mitte des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="67aa9-113">X-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67aa9-114">Y zentrieren</span><span class="sxs-lookup"><span data-stu-id="67aa9-114">Center Y</span></span></td>
<td><span data-ttu-id="67aa9-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="67aa9-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="67aa9-116">Y-Koordinate relativ zum Videorahmen der Mitte des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="67aa9-116">Y-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67aa9-117">Breite</span><span class="sxs-lookup"><span data-stu-id="67aa9-117">Width</span></span></td>
<td><span data-ttu-id="67aa9-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="67aa9-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="67aa9-119">Breite des Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="67aa9-119">Width of the rectangle in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67aa9-120">Höhe</span><span class="sxs-lookup"><span data-stu-id="67aa9-120">Height</span></span></td>
<td><span data-ttu-id="67aa9-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="67aa9-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="67aa9-122">Höhe des Rechtecks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="67aa9-122">Height of the rectangle in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67aa9-123">Aufbau</span><span class="sxs-lookup"><span data-stu-id="67aa9-123">Composition</span></span></td>
<td><span data-ttu-id="67aa9-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="67aa9-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="67aa9-125">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="67aa9-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="67aa9-126">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="67aa9-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="67aa9-127">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="67aa9-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="67aa9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67aa9-128">Requirements</span></span>



| <span data-ttu-id="67aa9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67aa9-129">Requirement</span></span> | <span data-ttu-id="67aa9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="67aa9-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67aa9-131">Header</span><span class="sxs-lookup"><span data-stu-id="67aa9-131">Header</span></span><br/> | <dl> <span data-ttu-id="67aa9-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="67aa9-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67aa9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67aa9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67aa9-134">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="67aa9-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





