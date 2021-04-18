---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (wmsdkidl. h)
description: Der Diagonale Übergang zeigt das neue Bild entlang einer diagonalen Linie, die in einer Ecke des Frames steht.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358297"
---
# <a name="wmt_videoimage_transition_diagonal"></a><span data-ttu-id="adf2b-104">Übergang von WMT \_ Videoimage \_ \_ Diagonal</span><span class="sxs-lookup"><span data-stu-id="adf2b-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL</span></span>

<span data-ttu-id="adf2b-105">Der Diagonale Übergang zeigt das neue Bild entlang einer diagonalen Linie, die in einer Ecke des Frames steht.</span><span class="sxs-lookup"><span data-stu-id="adf2b-105">The diagonal transition reveals the new image along a diagonal line originating in one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="adf2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="adf2b-106">Parameters</span></span>

<span data-ttu-id="adf2b-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="adf2b-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adf2b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="adf2b-108">Parameter</span></span></th>
<th><span data-ttu-id="adf2b-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="adf2b-109">Structure member</span></span></th>
<th><span data-ttu-id="adf2b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adf2b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adf2b-111">Breite</span><span class="sxs-lookup"><span data-stu-id="adf2b-111">Width</span></span></td>
<td><span data-ttu-id="adf2b-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="adf2b-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="adf2b-113">Breite des diagonalen Abschnitts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="adf2b-113">Width of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf2b-114">Höhe</span><span class="sxs-lookup"><span data-stu-id="adf2b-114">Height</span></span></td>
<td><span data-ttu-id="adf2b-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="adf2b-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="adf2b-116">Höhe des diagonalen Abschnitts in Pixel.</span><span class="sxs-lookup"><span data-stu-id="adf2b-116">Height of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf2b-117">Richtung</span><span class="sxs-lookup"><span data-stu-id="adf2b-117">Direction</span></span></td>
<td><span data-ttu-id="adf2b-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="adf2b-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="adf2b-119">Bestimmt die Ecke, aus der der Übergang stammt. Legen Sie einen der folgenden Wert fest:</span><span class="sxs-lookup"><span data-stu-id="adf2b-119">Determines the corner from which the transition originates.Set to one of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="adf2b-120">0 (oben rechts)</span><span class="sxs-lookup"><span data-stu-id="adf2b-120">0 - Upper right</span></span></li>
<li><span data-ttu-id="adf2b-121">1-obere linke Seite</span><span class="sxs-lookup"><span data-stu-id="adf2b-121">1 - Upper left</span></span></li>
<li><span data-ttu-id="adf2b-122">2-unten rechts</span><span class="sxs-lookup"><span data-stu-id="adf2b-122">2 - Lower right</span></span></li>
<li><span data-ttu-id="adf2b-123">3-unten links</span><span class="sxs-lookup"><span data-stu-id="adf2b-123">3 - Lower left</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf2b-124">Aufbau</span><span class="sxs-lookup"><span data-stu-id="adf2b-124">Composition</span></span></td>
<td><span data-ttu-id="adf2b-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="adf2b-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="adf2b-126">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="adf2b-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="adf2b-127">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="adf2b-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="adf2b-128">1: gibt eine umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="adf2b-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="adf2b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adf2b-129">Requirements</span></span>



| <span data-ttu-id="adf2b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adf2b-130">Requirement</span></span> | <span data-ttu-id="adf2b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="adf2b-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adf2b-132">Header</span><span class="sxs-lookup"><span data-stu-id="adf2b-132">Header</span></span><br/> | <dl> <span data-ttu-id="adf2b-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf2b-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf2b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adf2b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf2b-135">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="adf2b-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





