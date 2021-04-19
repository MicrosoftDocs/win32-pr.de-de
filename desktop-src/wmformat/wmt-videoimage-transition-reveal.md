---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (wmsdkidl. h)
description: Der übereinungs Übergang zeigt das neue Bild entlang einer geraden Linie an, die von einer Seite des Frames stammt.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365602"
---
# <a name="wmt_videoimage_transition_reveal"></a><span data-ttu-id="b2e93-104">WMT \_ Videoimage- \_ Übergang \_ offenlegen</span><span class="sxs-lookup"><span data-stu-id="b2e93-104">WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL</span></span>

<span data-ttu-id="b2e93-105">Der übereinungs Übergang zeigt das neue Bild entlang einer geraden Linie an, die von einer Seite des Frames stammt.</span><span class="sxs-lookup"><span data-stu-id="b2e93-105">The reveal transition reveals the new image along a straight line originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2e93-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e93-106">Parameters</span></span>

<span data-ttu-id="b2e93-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b2e93-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2e93-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2e93-108">Parameter</span></span></th>
<th><span data-ttu-id="b2e93-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="b2e93-109">Structure member</span></span></th>
<th><span data-ttu-id="b2e93-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2e93-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2e93-111">Entfernung</span><span class="sxs-lookup"><span data-stu-id="b2e93-111">Distance</span></span></td>
<td><span data-ttu-id="b2e93-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="b2e93-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="b2e93-113">Der Umfang des neuen Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="b2e93-113">Amount of the new image revealed, in pixels.</span></span> <span data-ttu-id="b2e93-114">Dieser Wert ist relativ zur Ursprungsseite des Frames.</span><span class="sxs-lookup"><span data-stu-id="b2e93-114">This value is relative to the originating side of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2e93-115">Richtung</span><span class="sxs-lookup"><span data-stu-id="b2e93-115">Direction</span></span></td>
<td><span data-ttu-id="b2e93-116"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="b2e93-116"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="b2e93-117">Die Richtung der Offenlegung. Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b2e93-117">Direction of the revealing.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="b2e93-118">0-offenlegen rechts; von der linken Seite des Frames ausgehen.</span><span class="sxs-lookup"><span data-stu-id="b2e93-118">0 - Reveal to the right; originate from the left side of the frame.</span></span></li>
<li><span data-ttu-id="b2e93-119">1-offen Links anzeigen; von der rechten Seite des Frames ausgehen.</span><span class="sxs-lookup"><span data-stu-id="b2e93-119">1 - Reveal to the left; originate from the right side of the frame.</span></span></li>
<li><span data-ttu-id="b2e93-120">2-nach oben anzeigen vom unteren Rand des Frames ausgehen.</span><span class="sxs-lookup"><span data-stu-id="b2e93-120">2 - Reveal upward; originate from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="b2e93-121">3: nach unten anzeigen vom oberen Rand des Frames ausgehen.</span><span class="sxs-lookup"><span data-stu-id="b2e93-121">3 - Reveal downward; originate from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2e93-122">Aufbau</span><span class="sxs-lookup"><span data-stu-id="b2e93-122">Composition</span></span></td>
<td><span data-ttu-id="b2e93-123"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="b2e93-123"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="b2e93-124">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b2e93-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="b2e93-125">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="b2e93-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="b2e93-126">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="b2e93-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b2e93-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2e93-127">Requirements</span></span>



| <span data-ttu-id="b2e93-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2e93-128">Requirement</span></span> | <span data-ttu-id="b2e93-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b2e93-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e93-130">Header</span><span class="sxs-lookup"><span data-stu-id="b2e93-130">Header</span></span><br/> | <dl> <span data-ttu-id="b2e93-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e93-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e93-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2e93-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e93-133">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="b2e93-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





