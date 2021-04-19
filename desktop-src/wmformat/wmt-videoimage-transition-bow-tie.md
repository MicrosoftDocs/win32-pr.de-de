---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (wmsdkidl. h)
description: Der Bogen Binder Übergang zeigt das neue Bild in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Rahmens an.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355881"
---
# <a name="wmt_videoimage_transition_bow_tie"></a><span data-ttu-id="cd59b-104">WMT \_ Videoimage- \_ Übergangs \_ Bogen \_ Tie</span><span class="sxs-lookup"><span data-stu-id="cd59b-104">WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE</span></span>

<span data-ttu-id="cd59b-105">Der Bogen Binder Übergang zeigt das neue Bild in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Rahmens an.</span><span class="sxs-lookup"><span data-stu-id="cd59b-105">The bow tie transition reveals the new image in a set of triangles on opposite sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd59b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd59b-106">Parameters</span></span>

<span data-ttu-id="cd59b-107">In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="cd59b-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd59b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd59b-108">Parameter</span></span></th>
<th><span data-ttu-id="cd59b-109">Strukturmember</span><span class="sxs-lookup"><span data-stu-id="cd59b-109">Structure member</span></span></th>
<th><span data-ttu-id="cd59b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd59b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd59b-111">Breite</span><span class="sxs-lookup"><span data-stu-id="cd59b-111">Width</span></span></td>
<td><span data-ttu-id="cd59b-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="cd59b-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="cd59b-113">Breite jeder dreieckigen Seite des Bogen links.</span><span class="sxs-lookup"><span data-stu-id="cd59b-113">Width of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd59b-114">Höhe</span><span class="sxs-lookup"><span data-stu-id="cd59b-114">Height</span></span></td>
<td><span data-ttu-id="cd59b-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="cd59b-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="cd59b-116">Die Höhe jeder dreieckigen Seite des Bogen-links.</span><span class="sxs-lookup"><span data-stu-id="cd59b-116">Height of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd59b-117">Richtung</span><span class="sxs-lookup"><span data-stu-id="cd59b-117">Direction</span></span></td>
<td><span data-ttu-id="cd59b-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="cd59b-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="cd59b-119">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cd59b-119">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="cd59b-120">0-gibt den horizontalen bogeneiendeeffekt an, in dem die Dreiecke von der rechten und linken Seite des Frames eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cd59b-120">0 - Specifies horizontal bow tie effect, in which the triangles enter from the right and left sides of the frame.</span></span></li>
<li><span data-ttu-id="cd59b-121">1: gibt den vertikalen Bogen Binder Effekt an, in dem die Dreiecke vom oberen und unteren Rand des Frames eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cd59b-121">1 - Specifies vertical bow tie effect, in which the triangles enter from the top and bottom of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd59b-122">Aufbau</span><span class="sxs-lookup"><span data-stu-id="cd59b-122">Composition</span></span></td>
<td><span data-ttu-id="cd59b-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="cd59b-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="cd59b-124">Legen Sie einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="cd59b-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="cd59b-125">0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="cd59b-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="cd59b-126">1: gibt eine umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild ist der Vordergrund.</span><span class="sxs-lookup"><span data-stu-id="cd59b-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="cd59b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd59b-127">Requirements</span></span>



| <span data-ttu-id="cd59b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd59b-128">Requirement</span></span> | <span data-ttu-id="cd59b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="cd59b-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd59b-130">Header</span><span class="sxs-lookup"><span data-stu-id="cd59b-130">Header</span></span><br/> | <dl> <span data-ttu-id="cd59b-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd59b-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd59b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd59b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd59b-133">**Video Bild Übergänge**</span><span class="sxs-lookup"><span data-stu-id="cd59b-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





