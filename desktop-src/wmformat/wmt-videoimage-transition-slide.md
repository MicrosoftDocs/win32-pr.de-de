---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (wmsdkidl. h)
description: Der Folien Übergang zeigt das neue Bild, indem das alte Bild aus dem Frame versetzt wird.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356463"
---
# <a name="wmt_videoimage_transition_slide"></a><span data-ttu-id="3e84c-104">Folie für WMT \_ Videoimage- \_ Übergang \_</span><span class="sxs-lookup"><span data-stu-id="3e84c-104">WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE</span></span>

<span data-ttu-id="3e84c-105">Der Folien Übergang zeigt das neue Bild, indem das alte Bild aus dem Frame versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="3e84c-105">The slide transition reveals the new image by sliding the old image out of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e84c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e84c-106">Parameters</span></span>

<span data-ttu-id="3e84c-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3e84c-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e84c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e84c-108">Parameter</span></span></th>
<th><span data-ttu-id="3e84c-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="3e84c-109">Structure member</span></span></th>
<th><span data-ttu-id="3e84c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e84c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e84c-111">Entfernung</span><span class="sxs-lookup"><span data-stu-id="3e84c-111">Distance</span></span></td>
<td><span data-ttu-id="3e84c-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="3e84c-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="3e84c-113">Abstand in Pixel, dass das alte Bild aus dem Frame heraus bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="3e84c-113">Distance, in pixels, that the old image slides out of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e84c-114">Richtung</span><span class="sxs-lookup"><span data-stu-id="3e84c-114">Direction</span></span></td>
<td><span data-ttu-id="3e84c-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="3e84c-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="3e84c-116">Die Richtung, in die das alte Bild verschoben wird. Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3e84c-116">Direction in which the old image slides.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="3e84c-117">0-Folie nach rechts verschieben.</span><span class="sxs-lookup"><span data-stu-id="3e84c-117">0 - Slide to the right.</span></span></li>
<li><span data-ttu-id="3e84c-118">1: Folie nach links.</span><span class="sxs-lookup"><span data-stu-id="3e84c-118">1 - Slide to the left.</span></span></li>
<li><span data-ttu-id="3e84c-119">2: Folie nach oben</span><span class="sxs-lookup"><span data-stu-id="3e84c-119">2 - Slide upward.</span></span></li>
<li><span data-ttu-id="3e84c-120">3: nach unten verschieben</span><span class="sxs-lookup"><span data-stu-id="3e84c-120">3 - Slide downward.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e84c-121">Aufbau</span><span class="sxs-lookup"><span data-stu-id="3e84c-121">Composition</span></span></td>
<td><span data-ttu-id="3e84c-122"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="3e84c-122"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="3e84c-123">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="3e84c-123">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="3e84c-124">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="3e84c-124">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="3e84c-125">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="3e84c-125">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3e84c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e84c-126">Requirements</span></span>



| <span data-ttu-id="3e84c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e84c-127">Requirement</span></span> | <span data-ttu-id="3e84c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3e84c-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e84c-129">Header</span><span class="sxs-lookup"><span data-stu-id="3e84c-129">Header</span></span><br/> | <dl> <span data-ttu-id="3e84c-130"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e84c-130"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e84c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e84c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e84c-132">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="3e84c-132">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





