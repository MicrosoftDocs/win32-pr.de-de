---
description: Die minimale Framerate, die von einem Video Erfassungsgerät in Frames pro Sekunde unterstützt wird.
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: MF_MT_FRAME_RATE_RANGE_MIN-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9692927242eea7ec65b86572db455e610e30c711
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867547"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a><span data-ttu-id="4b3c1-103">"MF MT"- \_ \_ Frame \_ Raten \_ Bereich \_ Min-Attribut</span><span class="sxs-lookup"><span data-stu-id="4b3c1-103">MF\_MT\_FRAME\_RATE\_RANGE\_MIN attribute</span></span>

<span data-ttu-id="4b3c1-104">Die minimale Framerate, die von einem Video Erfassungsgerät in Frames pro Sekunde unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-104">The minimum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="4b3c1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4b3c1-105">Data type</span></span>

<span data-ttu-id="4b3c1-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4b3c1-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="4b3c1-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="4b3c1-107">Get/set</span></span>

<span data-ttu-id="4b3c1-108">Um dieses Attribut abzurufen, nennen Sie [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="4b3c1-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="4b3c1-109">Um dieses Attribut festzulegen, nennen Sie [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="4b3c1-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b3c1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b3c1-110">Remarks</span></span>

<span data-ttu-id="4b3c1-111">Die Framerate wird als Verhältnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="4b3c1-112">Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="4b3c1-113">Wenn die Framerate z. b. 30 Frames pro Sekunde (fps) ist, ist das Verhältnis 30/1.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="4b3c1-114">Wenn das Erfassungsgerät eine minimale Framerate meldet, legt die Medienquelle dieses Attribut auf den Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-114">If the capture device reports a minimum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="4b3c1-115">Die maximale Framerate ist im [Bereich "MF \_ MT- \_ Rahmen \_ Raten Bereich ( \_ \_ Max](mf-mt-frame-rate-range-max.md) )" angegeben.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-115">The maximum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) attribute.</span></span> <span data-ttu-id="4b3c1-116">Es ist nicht garantiert, dass das Gerät jedes Inkrement in diesem Bereich unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="4b3c1-117">Zum Festlegen der Framerate des Geräts ändern Sie zunächst den Wert des " [**MF MT"- \_ \_ Frame \_ Raten**](mf-mt-frame-rate-attribute.md) Attributs für den Medientyp.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="4b3c1-118">Legen Sie dann den Medientyp für die Medienquelle fest.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="4b3c1-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4b3c1-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b3c1-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b3c1-120">Requirements</span></span>



| <span data-ttu-id="4b3c1-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b3c1-121">Requirement</span></span> | <span data-ttu-id="4b3c1-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4b3c1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3c1-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b3c1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b3c1-124">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4b3c1-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4b3c1-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b3c1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b3c1-126">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4b3c1-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4b3c1-127">Header</span><span class="sxs-lookup"><span data-stu-id="4b3c1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b3c1-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b3c1-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b3c1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b3c1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3c1-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4b3c1-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b3c1-131">Festlegen der Frame Rate für die Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="4b3c1-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="4b3c1-132">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="4b3c1-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b3c1-133">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="4b3c1-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4b3c1-134">maximal zulässige Anzahl von MF- \_ MT- \_ Frame \_ Raten \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b3c1-134">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 




