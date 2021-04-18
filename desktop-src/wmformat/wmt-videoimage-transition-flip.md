---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (wmsdkidl. h)
description: Der Flip-Übergang dreht das alte Bild auf einer y-Achse durch die Mitte des Frames. Das neue Bild wird als Rückseite des alten Bilds angezeigt.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358802"
---
# <a name="wmt_videoimage_transition_flip"></a><span data-ttu-id="b9cba-105">WMT \_ Videoimage- \_ Übergang \_ kippen</span><span class="sxs-lookup"><span data-stu-id="b9cba-105">WMT\_VIDEOIMAGE\_TRANSITION\_FLIP</span></span>

<span data-ttu-id="b9cba-106">Der Flip-Übergang dreht das alte Bild auf einer y-Achse durch die Mitte des Frames.</span><span class="sxs-lookup"><span data-stu-id="b9cba-106">The flip transition rotates the old image on a y-axis through the center of the frame.</span></span> <span data-ttu-id="b9cba-107">Das neue Bild wird als Rückseite des alten Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b9cba-107">The new image is revealed as the back of the old image.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9cba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9cba-108">Parameters</span></span>

<span data-ttu-id="b9cba-109">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b9cba-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9cba-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9cba-110">Parameter</span></span></th>
<th><span data-ttu-id="b9cba-111">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="b9cba-111">Structure member</span></span></th>
<th><span data-ttu-id="b9cba-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9cba-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9cba-113">Angle</span><span class="sxs-lookup"><span data-stu-id="b9cba-113">Angle</span></span></td>
<td><span data-ttu-id="b9cba-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="b9cba-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="b9cba-115">Drehwinkel zwischen 0,0 und 180,0 Grad.</span><span class="sxs-lookup"><span data-stu-id="b9cba-115">Angle of the rotation, from 0.0 to 180.0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9cba-116">Aufbau</span><span class="sxs-lookup"><span data-stu-id="b9cba-116">Composition</span></span></td>
<td><span data-ttu-id="b9cba-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="b9cba-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="b9cba-118">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="b9cba-118">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="b9cba-119">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="b9cba-119">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="b9cba-120">1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="b9cba-120">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b9cba-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9cba-121">Remarks</span></span>

<span data-ttu-id="b9cba-122">Sie können die Auswirkung dieses Übergangs visualisieren, als ob beide Bilder physische Foto-und Back-to-Back-Listen darstellen.</span><span class="sxs-lookup"><span data-stu-id="b9cba-122">You can visualize the effect of this transition as if both images were physical photographs glued together back-to-back.</span></span> <span data-ttu-id="b9cba-123">Der Übergang hat denselben Effekt wie das halten zweier solcher Fotos in der Mitte des unteren Rands und Rotieren der Fotos um 180 Grad.</span><span class="sxs-lookup"><span data-stu-id="b9cba-123">The transition has the same effect as holding two such photographs at the center of the bottom edge and rotating them 180 degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9cba-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9cba-124">Requirements</span></span>



| <span data-ttu-id="b9cba-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9cba-125">Requirement</span></span> | <span data-ttu-id="b9cba-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b9cba-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b9cba-127">Header</span><span class="sxs-lookup"><span data-stu-id="b9cba-127">Header</span></span><br/> | <dl> <span data-ttu-id="b9cba-128"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9cba-128"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9cba-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9cba-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9cba-130">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="b9cba-130">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





