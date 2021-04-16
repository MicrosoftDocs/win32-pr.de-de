---
description: Gibt die maximale Anzahl von Ltr-Frames (Long Term Reference) an, die von der Anwendung gesteuert werden.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524632"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a><span data-ttu-id="783de-103">Codecapi \_ avencvideoltrbuffercontrol (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="783de-103">CODECAPI\_AVEncVideoLTRBufferControl property</span></span>

<span data-ttu-id="783de-104">Gibt die maximale Anzahl von Ltr-Frames (Long Term Reference) an, die von der Anwendung gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="783de-104">Specifies the maximum number of Long Term Reference (LTR) frames controlled by application.</span></span>

## <a name="data-type"></a><span data-ttu-id="783de-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="783de-105">Data type</span></span>

<span data-ttu-id="783de-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="783de-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="783de-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="783de-107">Property GUID</span></span>

<span data-ttu-id="783de-108">**Codecapi \_ avencvideoltrbuffercontrol**</span><span class="sxs-lookup"><span data-stu-id="783de-108">**CODECAPI\_AVEncVideoLTRBufferControl**</span></span>

## <a name="property-value"></a><span data-ttu-id="783de-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="783de-109">Property value</span></span>

<span data-ttu-id="783de-110">Der Wert dieses Steuer Elements enthält zwei Felder, in denen jedes Feld über 16 Bits verfügt.</span><span class="sxs-lookup"><span data-stu-id="783de-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="783de-111">Wert</span><span class="sxs-lookup"><span data-stu-id="783de-111">Value</span></span></th>
<th><span data-ttu-id="783de-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="783de-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="783de-113"><dt><strong>Die ersten feldbits</strong></dt> <dt>[0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="783de-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="783de-114">Die Anzahl der von der Anwendung kontrollierten Ltr-Frames.</span><span class="sxs-lookup"><span data-stu-id="783de-114">The number of LTR frames controlled by the application.</span></span><br/> <span data-ttu-id="783de-115"><strong>H. 264/AVC-Encoder:</strong></span><span class="sxs-lookup"><span data-stu-id="783de-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="783de-116">Wenn der Wert n und n ungleich 0 (null) ist, muss der Encoder bei jedem IDR-Frame automatisch die Frames nach dem IDR-Frame (und dem IDR-Frame) als Ltr-Frames markieren, solange alle drei der folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="783de-116">Assuming the value is N and N is non-zero value, at each IDR frame the encoder must automatically mark the frames following the IDR frame (and including the IDR frame) as LTR frames as long as all 3 of the following apply:</span></span>
<ul>
<li><span data-ttu-id="783de-117">Der Frame ist nicht bereits so festgelegt, dass er als langfristiger Verweis Rahmen gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="783de-117">The frame is not already set to be marked as a long term reference frame.</span></span></li>
<li><span data-ttu-id="783de-118">Der Frame ist ein basisebenenframe.</span><span class="sxs-lookup"><span data-stu-id="783de-118">The frame is a base layer frame.</span></span> <span data-ttu-id="783de-119">Beispielsweise <strong>temporal_id</strong> -Syntax Element gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="783de-119">For example, syntax element <strong>temporal_id</strong> equal to 0.</span></span></li>
<li><span data-ttu-id="783de-120">Die Anzahl der zurzeit als Ltr markierten Frames ist kleiner als N.</span><span class="sxs-lookup"><span data-stu-id="783de-120">The number of frames currently marked as LTR is less than N.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="783de-121"><dt><strong>Das zweite Feld</strong></dt> <dt>Bits [16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="783de-121"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="783de-122">Der Vertrauensstellungs Modus des Ltr-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="783de-122">The trust mode of LTR control.</span></span><br/> <span data-ttu-id="783de-123"><strong>H. 264/AVC-Encoder:</strong></span><span class="sxs-lookup"><span data-stu-id="783de-123"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="783de-124">1 (Trust until) bedeutet, dass der Encoder einen Ltr-Frame verwenden kann, es sei denn, die APP macht Sie explizit über das <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> -Steuerelement ungültig.</span><span class="sxs-lookup"><span data-stu-id="783de-124">1 (Trust Until) means the encoder may use an LTR frame unless the app explicitly invalidates it through the <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> control.</span></span> <br/> <span data-ttu-id="783de-125">Andere Werte sind ungültig und sind für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="783de-125">Other values are invalid and reserved for future use.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="783de-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="783de-126">Remarks</span></span>

<span data-ttu-id="783de-127">Dies ist eine statische API.</span><span class="sxs-lookup"><span data-stu-id="783de-127">This is a static API.</span></span>

<span data-ttu-id="783de-128">Der Standardwert muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="783de-128">Default value shall be 0</span></span>

## <a name="requirements"></a><span data-ttu-id="783de-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="783de-129">Requirements</span></span>



| <span data-ttu-id="783de-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="783de-130">Requirement</span></span> | <span data-ttu-id="783de-131">Wert</span><span class="sxs-lookup"><span data-stu-id="783de-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="783de-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="783de-132">Minimum supported client</span></span><br/> | <span data-ttu-id="783de-133">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="783de-133">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="783de-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="783de-134">Minimum supported server</span></span><br/> | <span data-ttu-id="783de-135">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="783de-135">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="783de-136">Header</span><span class="sxs-lookup"><span data-stu-id="783de-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="783de-137"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="783de-137"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="783de-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="783de-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783de-139">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="783de-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




