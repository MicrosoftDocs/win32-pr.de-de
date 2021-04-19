---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (wmsdkidl. h)
description: Der einfügen-Übergang zeigt das neue Bild in einem Rechteck an, das aus einer Ecke des Frames stammt.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354113"
---
# <a name="wmt_videoimage_transition_inset"></a><span data-ttu-id="28ba0-104">WMT \_ Videoimage- \_ Übergangs \_ inmenge</span><span class="sxs-lookup"><span data-stu-id="28ba0-104">WMT\_VIDEOIMAGE\_TRANSITION\_INSET</span></span>

<span data-ttu-id="28ba0-105">Der einfügen-Übergang zeigt das neue Bild in einem Rechteck an, das aus einer Ecke des Frames stammt.</span><span class="sxs-lookup"><span data-stu-id="28ba0-105">The inset transition reveals the new image in a rectangle originating from one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="28ba0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28ba0-106">Parameters</span></span>

<span data-ttu-id="28ba0-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="28ba0-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28ba0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="28ba0-108">Parameter</span></span></th>
<th><span data-ttu-id="28ba0-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="28ba0-109">Structure member</span></span></th>
<th><span data-ttu-id="28ba0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28ba0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28ba0-111">Breite</span><span class="sxs-lookup"><span data-stu-id="28ba0-111">Width</span></span></td>
<td><span data-ttu-id="28ba0-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="28ba0-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="28ba0-113">Breite des insets in Pixel.</span><span class="sxs-lookup"><span data-stu-id="28ba0-113">Width of the inset in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28ba0-114">Höhe</span><span class="sxs-lookup"><span data-stu-id="28ba0-114">Height</span></span></td>
<td><span data-ttu-id="28ba0-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="28ba0-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="28ba0-116">Die Höhe des insets in Pixel.</span><span class="sxs-lookup"><span data-stu-id="28ba0-116">Height of the inset in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28ba0-117">Richtung</span><span class="sxs-lookup"><span data-stu-id="28ba0-117">Direction</span></span></td>
<td><span data-ttu-id="28ba0-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="28ba0-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="28ba0-119">Ecke, von der die inmenge stammt. Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="28ba0-119">Corner from which the inset originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="28ba0-120">0-unten links</span><span class="sxs-lookup"><span data-stu-id="28ba0-120">0 - Lower left</span></span></li>
<li><span data-ttu-id="28ba0-121">1-untere rechte Seite</span><span class="sxs-lookup"><span data-stu-id="28ba0-121">1 - Lower right</span></span></li>
<li><span data-ttu-id="28ba0-122">2-obere linke Seite</span><span class="sxs-lookup"><span data-stu-id="28ba0-122">2 - Upper left</span></span></li>
<li><span data-ttu-id="28ba0-123">3-obere rechte</span><span class="sxs-lookup"><span data-stu-id="28ba0-123">3 - Upper right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28ba0-124">Aufbau</span><span class="sxs-lookup"><span data-stu-id="28ba0-124">Composition</span></span></td>
<td><span data-ttu-id="28ba0-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="28ba0-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="28ba0-126">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="28ba0-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="28ba0-127">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="28ba0-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="28ba0-128">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="28ba0-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="28ba0-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28ba0-129">Requirements</span></span>



| <span data-ttu-id="28ba0-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28ba0-130">Requirement</span></span> | <span data-ttu-id="28ba0-131">Wert</span><span class="sxs-lookup"><span data-stu-id="28ba0-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28ba0-132">Header</span><span class="sxs-lookup"><span data-stu-id="28ba0-132">Header</span></span><br/> | <dl> <span data-ttu-id="28ba0-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ba0-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ba0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28ba0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ba0-135">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="28ba0-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





