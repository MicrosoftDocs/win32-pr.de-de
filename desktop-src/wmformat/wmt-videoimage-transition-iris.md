---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (wmsdkidl. h)
description: Der Iris-Übergang zeigt das neue Bild entlang einer x-Achse und einer y-Achse an. Der visuelle Effekt dieses Übergangs besteht darin, dass das neue Bild in einem erweiternden quer Sprung zu allen Seiten des Frames angezeigt wird.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372141"
---
# <a name="wmt_videoimage_transition_iris"></a><span data-ttu-id="5192c-105">WMT \_ Videoimage- \_ Übergangs \_ IRIS</span><span class="sxs-lookup"><span data-stu-id="5192c-105">WMT\_VIDEOIMAGE\_TRANSITION\_IRIS</span></span>

<span data-ttu-id="5192c-106">Der Iris-Übergang zeigt das neue Bild entlang einer x-Achse und einer y-Achse an.</span><span class="sxs-lookup"><span data-stu-id="5192c-106">The iris transition reveals the new image along an x-axis and a y-axis.</span></span> <span data-ttu-id="5192c-107">Der visuelle Effekt dieses Übergangs besteht darin, dass das neue Bild in einem erweiternden quer Sprung zu allen Seiten des Frames angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5192c-107">The visual effect of this transition is that the new image appears in a widening cross reaching to all sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="5192c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5192c-108">Parameters</span></span>

<span data-ttu-id="5192c-109">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="5192c-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5192c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5192c-110">Parameter</span></span></th>
<th><span data-ttu-id="5192c-111">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="5192c-111">Structure member</span></span></th>
<th><span data-ttu-id="5192c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5192c-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5192c-113">X zentrieren</span><span class="sxs-lookup"><span data-stu-id="5192c-113">Center X</span></span></td>
<td><span data-ttu-id="5192c-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="5192c-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="5192c-115">X-Koordinate relativ zum Videorahmen der Mitte des IRIS-Effekts.</span><span class="sxs-lookup"><span data-stu-id="5192c-115">X-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5192c-116">Y zentrieren</span><span class="sxs-lookup"><span data-stu-id="5192c-116">Center Y</span></span></td>
<td><span data-ttu-id="5192c-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="5192c-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="5192c-118">Y-Koordinate relativ zum Videorahmen der Mitte des Schwert Effekts.</span><span class="sxs-lookup"><span data-stu-id="5192c-118">Y-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5192c-119">Breite</span><span class="sxs-lookup"><span data-stu-id="5192c-119">Width</span></span></td>
<td><span data-ttu-id="5192c-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="5192c-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="5192c-121">Breite der vertikalen Linie, die das neue Bild offenbart, in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5192c-121">Width of the vertical line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5192c-122">Höhe</span><span class="sxs-lookup"><span data-stu-id="5192c-122">Height</span></span></td>
<td><span data-ttu-id="5192c-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="5192c-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="5192c-124">Höhe der horizontalen Linie, die das neue Bild aufzeigt, in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5192c-124">Height of the horizontal line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5192c-125">Aufbau</span><span class="sxs-lookup"><span data-stu-id="5192c-125">Composition</span></span></td>
<td><span data-ttu-id="5192c-126"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="5192c-126"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="5192c-127">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="5192c-127">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="5192c-128">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="5192c-128">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="5192c-129">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="5192c-129">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="5192c-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5192c-130">Requirements</span></span>



| <span data-ttu-id="5192c-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5192c-131">Requirement</span></span> | <span data-ttu-id="5192c-132">Wert</span><span class="sxs-lookup"><span data-stu-id="5192c-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5192c-133">Header</span><span class="sxs-lookup"><span data-stu-id="5192c-133">Header</span></span><br/> | <dl> <span data-ttu-id="5192c-134"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5192c-134"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5192c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5192c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5192c-136">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="5192c-136">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





