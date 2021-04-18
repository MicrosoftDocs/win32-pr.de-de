---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (wmsdkidl. h)
description: Der Seiten rollenübergang transformiert das alte Bild mit einem Seitenumbruch Effekt und zeigt das neue Bild unterhalb an.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364836"
---
# <a name="wmt_videoimage_transition_page_roll"></a><span data-ttu-id="08c8b-104">WMT \_ Videoimage- \_ Übergangs \_ Seite \_ (Rollup)</span><span class="sxs-lookup"><span data-stu-id="08c8b-104">WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL</span></span>

<span data-ttu-id="08c8b-105">Der Seiten rollenübergang transformiert das alte Bild mit einem Seitenumbruch Effekt und zeigt das neue Bild unterhalb an.</span><span class="sxs-lookup"><span data-stu-id="08c8b-105">The page roll transition transforms the old image with a page-flipping effect, revealing the new image underneath.</span></span>

## <a name="parameters"></a><span data-ttu-id="08c8b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08c8b-106">Parameters</span></span>

<span data-ttu-id="08c8b-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="08c8b-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08c8b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08c8b-108">Parameter</span></span></th>
<th><span data-ttu-id="08c8b-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="08c8b-109">Structure member</span></span></th>
<th><span data-ttu-id="08c8b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08c8b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08c8b-111">Radius</span><span class="sxs-lookup"><span data-stu-id="08c8b-111">Radius</span></span></td>
<td><span data-ttu-id="08c8b-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="08c8b-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="08c8b-113">Der Radius des Rollbacks im Seiten Roll Effekt.</span><span class="sxs-lookup"><span data-stu-id="08c8b-113">Radius of the roll in the page roll effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08c8b-114">Entfernung</span><span class="sxs-lookup"><span data-stu-id="08c8b-114">Distance</span></span></td>
<td><span data-ttu-id="08c8b-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="08c8b-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="08c8b-116">Die Menge des neuen Bilds, das durch den Seiten rollffekt in Pixel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="08c8b-116">Amount of the new image that is revealed by the page roll effect, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08c8b-117">Richtung</span><span class="sxs-lookup"><span data-stu-id="08c8b-117">Direction</span></span></td>
<td><span data-ttu-id="08c8b-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="08c8b-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="08c8b-119">Die Ecke oder Seite des Video Rahmens, von der die Seiten Ausführung ausgeht. Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="08c8b-119">Corner or side of the video frame, from which the page roll originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="08c8b-120">0-linke Seite</span><span class="sxs-lookup"><span data-stu-id="08c8b-120">0 - Left side</span></span></li>
<li><span data-ttu-id="08c8b-121">1-Rechte Seite</span><span class="sxs-lookup"><span data-stu-id="08c8b-121">1 - Right side</span></span></li>
<li><span data-ttu-id="08c8b-122">2-unten</span><span class="sxs-lookup"><span data-stu-id="08c8b-122">2 - Bottom</span></span></li>
<li><span data-ttu-id="08c8b-123">3-oben</span><span class="sxs-lookup"><span data-stu-id="08c8b-123">3 - Top</span></span></li>
<li><span data-ttu-id="08c8b-124">4-untere linke Ecke</span><span class="sxs-lookup"><span data-stu-id="08c8b-124">4 - Bottom left corner</span></span></li>
<li><span data-ttu-id="08c8b-125">5-untere rechte Ecke</span><span class="sxs-lookup"><span data-stu-id="08c8b-125">5 - Bottom right corner</span></span></li>
<li><span data-ttu-id="08c8b-126">6-obere linke Ecke</span><span class="sxs-lookup"><span data-stu-id="08c8b-126">6 - Upper left corner</span></span></li>
<li><span data-ttu-id="08c8b-127">7-obere rechte Ecke</span><span class="sxs-lookup"><span data-stu-id="08c8b-127">7 - Upper right corner</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08c8b-128">Aufbau</span><span class="sxs-lookup"><span data-stu-id="08c8b-128">Composition</span></span></td>
<td><span data-ttu-id="08c8b-129"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="08c8b-129"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="08c8b-130">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="08c8b-130">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="08c8b-131">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="08c8b-131">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="08c8b-132">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="08c8b-132">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="08c8b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08c8b-133">Requirements</span></span>



| <span data-ttu-id="08c8b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08c8b-134">Requirement</span></span> | <span data-ttu-id="08c8b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="08c8b-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08c8b-136">Header</span><span class="sxs-lookup"><span data-stu-id="08c8b-136">Header</span></span><br/> | <dl> <span data-ttu-id="08c8b-137"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08c8b-137"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c8b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08c8b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c8b-139">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="08c8b-139">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





