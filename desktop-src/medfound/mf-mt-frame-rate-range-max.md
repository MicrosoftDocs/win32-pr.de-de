---
description: Die maximale Framerate, die von einem Video Erfassungsgerät in Frames pro Sekunde unterstützt wird.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: MF_MT_FRAME_RATE_RANGE_MAX-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959287"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a><span data-ttu-id="4a645-103">Maximal zulässige Größe des MF \_ MT- \_ Frame \_ Raten \_ Bereichs \_</span><span class="sxs-lookup"><span data-stu-id="4a645-103">MF\_MT\_FRAME\_RATE\_RANGE\_MAX attribute</span></span>

<span data-ttu-id="4a645-104">Die maximale Framerate, die von einem Video Erfassungsgerät in Frames pro Sekunde unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4a645-104">The maximum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a645-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4a645-105">Data type</span></span>

<span data-ttu-id="4a645-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4a645-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="4a645-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="4a645-107">Get/set</span></span>

<span data-ttu-id="4a645-108">Um dieses Attribut abzurufen, nennen Sie [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="4a645-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="4a645-109">Um dieses Attribut festzulegen, nennen Sie [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="4a645-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a645-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a645-110">Remarks</span></span>

<span data-ttu-id="4a645-111">Die Framerate wird als Verhältnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="4a645-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="4a645-112">Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner.</span><span class="sxs-lookup"><span data-stu-id="4a645-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="4a645-113">Wenn die Framerate z. b. 30 Frames pro Sekunde (fps) ist, ist das Verhältnis 30/1.</span><span class="sxs-lookup"><span data-stu-id="4a645-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="4a645-114">Wenn das Erfassungsgerät eine maximale Framerate meldet, legt die Medienquelle dieses Attribut auf den Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="4a645-114">If the capture device reports a maximum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="4a645-115">Die minimale Framerate wird im " [MF \_ MT"- \_ Rahmen \_ Raten \_ Bereich " \_ Min](mf-mt-frame-rate-range-min.md) "-Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="4a645-115">The minimum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attribute.</span></span> <span data-ttu-id="4a645-116">Es ist nicht garantiert, dass das Gerät jedes Inkrement in diesem Bereich unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4a645-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="4a645-117">Zum Festlegen der Framerate des Geräts ändern Sie zunächst den Wert des " [**MF MT"- \_ \_ Frame \_ Raten**](mf-mt-frame-rate-attribute.md) Attributs für den Medientyp.</span><span class="sxs-lookup"><span data-stu-id="4a645-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="4a645-118">Legen Sie dann den Medientyp für die Medienquelle fest.</span><span class="sxs-lookup"><span data-stu-id="4a645-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="4a645-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4a645-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a645-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a645-120">Requirements</span></span>



| <span data-ttu-id="4a645-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a645-121">Requirement</span></span> | <span data-ttu-id="4a645-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4a645-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a645-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a645-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4a645-124">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4a645-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4a645-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a645-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4a645-126">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4a645-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4a645-127">Header</span><span class="sxs-lookup"><span data-stu-id="4a645-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a645-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a645-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a645-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a645-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a645-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4a645-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a645-131">Festlegen der Frame Rate für die Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="4a645-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="4a645-132">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="4a645-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a645-133">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="4a645-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4a645-134">Bereich für die Anzahl von MF \_ MT- \_ Frame \_ Raten \_ \_</span><span class="sxs-lookup"><span data-stu-id="4a645-134">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




