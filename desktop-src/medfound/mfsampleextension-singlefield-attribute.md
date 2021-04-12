---
description: Gibt an, ob ein Video Beispiel ein einzelnes Feld oder zwei verschachtelte Felder enthält. Dieses Attribut gilt für Medien Beispiele.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: MFSampleExtension_SingleField-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527926"
---
# <a name="mfsampleextension_singlefield-attribute"></a><span data-ttu-id="3f16f-104">MF Sample Extension- \_ Singlefield-Attribut</span><span class="sxs-lookup"><span data-stu-id="3f16f-104">MFSampleExtension\_SingleField attribute</span></span>

<span data-ttu-id="3f16f-105">Gibt an, ob ein Video Beispiel ein einzelnes Feld oder zwei verschachtelte Felder enthält.</span><span class="sxs-lookup"><span data-stu-id="3f16f-105">Specifies whether a video sample contains a single field or two interleaved fields.</span></span> <span data-ttu-id="3f16f-106">Dieses Attribut gilt für Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="3f16f-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="3f16f-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3f16f-107">Data type</span></span>

<span data-ttu-id="3f16f-108">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f16f-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3f16f-109">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="3f16f-109">Get/set</span></span>

<span data-ttu-id="3f16f-110">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3f16f-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3f16f-111">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3f16f-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3f16f-112">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="3f16f-112">Applies to</span></span>

[<span data-ttu-id="3f16f-113">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="3f16f-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="3f16f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f16f-114">Remarks</span></span>

<span data-ttu-id="3f16f-115">Wenn der Wert **true** ist, enthält das Beispiel ein Feld.</span><span class="sxs-lookup"><span data-stu-id="3f16f-115">If the value is **TRUE**, the sample contains one field.</span></span> <span data-ttu-id="3f16f-116">Wenn der Wert **false** ist oder das-Attribut nicht festgelegt ist, enthält das Beispiel einen kompletten Frame.</span><span class="sxs-lookup"><span data-stu-id="3f16f-116">If the value is **FALSE** or the attribute is not set, the sample contains a complete frame.</span></span> <span data-ttu-id="3f16f-117">(Zwei Felder, wenn Zeilen Sprung oder ein progressiver Rahmen).</span><span class="sxs-lookup"><span data-stu-id="3f16f-117">(Two fields if interlaced, or a progressive frame.)</span></span>

<span data-ttu-id="3f16f-118">Wenn es sich bei dem Medientyp um progressive Frames oder verschachtelte Felder handelt, muss dieses Attribut auf " **false** " oder "unset" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="3f16f-118">If the media type is progressive frames or interleaved fields, this attribute must be **FALSE** or left unset.</span></span>

<span data-ttu-id="3f16f-119">Wenn der Medientyp ein einzelnes Feld ist, muss dieses Attribut " **true**" lauten.</span><span class="sxs-lookup"><span data-stu-id="3f16f-119">If the media type is single field, this attribute must be **TRUE**.</span></span> <span data-ttu-id="3f16f-120">Legen Sie das Attribut " [**mfsampleextension \_ bottomfieldfirst**](mfsampleextension-bottomfieldfirst-attribute.md) " für das Beispiel fest, um anzugeben, ob es sich um das obere Feld oder das untere Feld handelt.</span><span class="sxs-lookup"><span data-stu-id="3f16f-120">Set the [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute on the sample to indicate whether it is the upper field or the lower field.</span></span>

<span data-ttu-id="3f16f-121">Zurzeit unterstützt der erweiterte Videorenderer (EVR) keine Inhalte, die zwischen Zeilen Sprung Frames und einzelnen Feldern wechseln.</span><span class="sxs-lookup"><span data-stu-id="3f16f-121">Currently the enhanced video renderer (EVR) does not support content that switches between interlaced frames and single fields.</span></span>

<span data-ttu-id="3f16f-122">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="3f16f-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f16f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f16f-123">Requirements</span></span>



| <span data-ttu-id="3f16f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f16f-124">Requirement</span></span> | <span data-ttu-id="3f16f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3f16f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f16f-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f16f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f16f-127">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="3f16f-127">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="3f16f-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f16f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f16f-129">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="3f16f-129">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3f16f-130">Header</span><span class="sxs-lookup"><span data-stu-id="3f16f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f16f-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f16f-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f16f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f16f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f16f-133">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3f16f-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3f16f-134">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="3f16f-134">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="3f16f-135">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f16f-135">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="3f16f-136">Video-Interlacing</span><span class="sxs-lookup"><span data-stu-id="3f16f-136">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




