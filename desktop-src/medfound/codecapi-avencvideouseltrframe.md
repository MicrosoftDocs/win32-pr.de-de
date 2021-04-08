---
description: Gibt an, dass der aktuelle Frame mit einem oder mehreren Ltr-Frames codiert wird.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749353"
---
# <a name="codecapi_avencvideouseltrframe-property"></a><span data-ttu-id="48aae-103">Codecapi \_ avencvideouseltrframe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="48aae-103">CODECAPI\_AVEncVideoUseLTRFrame property</span></span>

<span data-ttu-id="48aae-104">Gibt an, dass der aktuelle Frame mit einem oder mehreren Ltr-Frames codiert wird.</span><span class="sxs-lookup"><span data-stu-id="48aae-104">Specifies that the current frame is encoded using one or multiple LTR frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="48aae-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="48aae-105">Data type</span></span>

<span data-ttu-id="48aae-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="48aae-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="48aae-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="48aae-107">Property GUID</span></span>

<span data-ttu-id="48aae-108">**Codecapi \_ avencvideouseltrframe**</span><span class="sxs-lookup"><span data-stu-id="48aae-108">**CODECAPI\_AVEncVideoUseLTRFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="48aae-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="48aae-109">Property value</span></span>

<span data-ttu-id="48aae-110">Der Wert dieses Steuer Elements enthält zwei Felder, in denen jedes Feld über 16 Bits verfügt.</span><span class="sxs-lookup"><span data-stu-id="48aae-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48aae-111">Wert</span><span class="sxs-lookup"><span data-stu-id="48aae-111">Value</span></span></th>
<th><span data-ttu-id="48aae-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="48aae-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="48aae-113"><dt><strong>Die ersten feldbits</strong></dt> <dt>[0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="48aae-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="48aae-114">Gibt an, welche Ltr-Frames zum Codieren des aktuellen Frames zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="48aae-114">Indicates which LTR frame(s) are allowed for encoding the current frame.</span></span> <br/> <span data-ttu-id="48aae-115"><strong>H. 264/AVC-Encoder:</strong></span><span class="sxs-lookup"><span data-stu-id="48aae-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="48aae-116">Dies ist eine Bitmap, die angibt, welche Ltr-Frames als Verweis für diesen Frame verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="48aae-116">This is a bitmap that indicates which LTR frames can be used as a reference for this frame.</span></span> <span data-ttu-id="48aae-117">Das unwichtigste Bit entspricht dem Ltr-Index 0, das zweite unwichtigste Bit entspricht dem Ltr-Index 1 usw.</span><span class="sxs-lookup"><span data-stu-id="48aae-117">The least significant bit corresponds to LTR index 0, the second least significant bit corresponds to LTR index 1, etc.</span></span><br/> <span data-ttu-id="48aae-118">Dieser Wert darf nicht 0 sein.</span><span class="sxs-lookup"><span data-stu-id="48aae-118">This value shall not be 0.</span></span><br/> <span data-ttu-id="48aae-119">Der höchste Index, der durch diesen Wert angegeben wird, darf nicht größer als die maximale Anzahl von Ltr-Frames sein, die in der <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> -Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="48aae-119">The highest index specified by this value shall not be greater than the maximum number of LTR frames specified in the <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> property less one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="48aae-120"><dt><strong>Das zweite Feld</strong></dt> <dt>Bits [16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="48aae-120"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="48aae-121">Flag, das angibt, ob für das Codieren von nachfolgenden Frames zusätzliche Einschränkungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="48aae-121">Flag that indicates whether additional limitations are required for encoding subsequent frames.</span></span> <br/> <span data-ttu-id="48aae-122"><strong>H. 264/AVC-Encoder:</strong></span><span class="sxs-lookup"><span data-stu-id="48aae-122"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="48aae-123">1 ist der einzige gültige Wert für dieses Feld.</span><span class="sxs-lookup"><span data-stu-id="48aae-123">1 is on the only valid value for this field.</span></span> <span data-ttu-id="48aae-124">Alle anderen Werte sind ungültig und sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="48aae-124">All other values are invalid and reserved for future use.</span></span><br/> <span data-ttu-id="48aae-125">Wenn das Flag 1 ist, muss der Encoder nachfolgende Frames in der Codierungs Reihenfolge codieren, die den folgenden Einschränkungen unterliegen:</span><span class="sxs-lookup"><span data-stu-id="48aae-125">When the flag is 1, the encoder shall encode subsequent frames in encoding order subject to the following constraints:</span></span><br/>
<ul>
<li><span data-ttu-id="48aae-126">Es dürfen keine kurzfristigen Verweis Rahmen in der Codierungs Reihenfolge verwendet werden, die älter als der aktuelle Frame oder in der Codierungs Reihenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="48aae-126">It shall not use short term reference frames in encoding order older than the current frame or future encoding in encoding order.</span></span></li>
<li><span data-ttu-id="48aae-127">Es dürfen keine Ltr-Frames verwendet werden, die nicht vom letzten CODECAPI_AVEncVideoUseLTRFrame Steuerelement beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="48aae-127">It shall not use LTR frames not described by the most recent CODECAPI_AVEncVideoUseLTRFrame control.</span></span></li>
<li><span data-ttu-id="48aae-128">Es können Ltr-Frames verwendet werden, die nach dem aktuellen Frame aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="48aae-128">It may use LTR frames updated after the current frame.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="48aae-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48aae-129">Remarks</span></span>

<span data-ttu-id="48aae-130">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="48aae-130">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="48aae-131">Diese Eigenschaft sollte nicht aufgerufen werden, wenn ein ausstehender Aufruf zur Verwendung eines Ltr-Frames mithilfe der codecapi- \_ Eigenschaft "avencvideouseltrframe" ausgegeben wurde und der Encoder noch keinen Frame generiert hat, der die Ltr verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="48aae-131">This property should not be called if a pending call to use an LTR frame has been issued using the CODECAPI\_AVEncVideoUseLTRFrame property and the encoder has not yet generated a frame that has used the LTR.</span></span> <span data-ttu-id="48aae-132">Anders ausgedrückt: der Encoder sollte codecapi- \_ krecvideouseltrframe-Anforderungen nicht in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="48aae-132">In other words, the encoder should not queue up CODECAPI\_AVEncVideoUseLTRFrame requests.</span></span>

<span data-ttu-id="48aae-133">Wenn eine codecapi-Regel " \_ avencvideouseltrframe" übermittelt wird, während eine andere codecapi-Datei " \_ avencvideouseltrframe" noch aussteht, sollte die ältere Anforderung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="48aae-133">If a CODECAPI\_AVEncVideoUseLTRFrame request is submitted while another CODECAPI\_AVEncVideoUseLTRFrame request is still pending, then the older request should be dropped.</span></span>

<span data-ttu-id="48aae-134">Das Aufrufen von codecapi \_ avencvideouseltrframe auf einem nicht-Basisschicht Rahmen ist gültig und sollte auf den nicht-Basisschicht Rahmen angewendet werden, ohne dass ein basisebenenframe verzögert wird.</span><span class="sxs-lookup"><span data-stu-id="48aae-134">Calling CODECAPI\_AVEncVideoUseLTRFrame on a non-base layer frame is valid and shall apply to the non-base layer frame, without delay to a base layer frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="48aae-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48aae-135">Requirements</span></span>



| <span data-ttu-id="48aae-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48aae-136">Requirement</span></span> | <span data-ttu-id="48aae-137">Wert</span><span class="sxs-lookup"><span data-stu-id="48aae-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48aae-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48aae-138">Minimum supported client</span></span><br/> | <span data-ttu-id="48aae-139">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="48aae-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="48aae-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48aae-140">Minimum supported server</span></span><br/> | <span data-ttu-id="48aae-141">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="48aae-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="48aae-142">Header</span><span class="sxs-lookup"><span data-stu-id="48aae-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="48aae-143"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="48aae-143"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48aae-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48aae-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48aae-145">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="48aae-145">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




