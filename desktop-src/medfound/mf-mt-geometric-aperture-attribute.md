---
description: Definiert die geometrische Öffnung für einen Video Medientyp.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: MF_MT_GEOMETRIC_APERTURE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959286"
---
# <a name="mf_mt_geometric_aperture-attribute"></a><span data-ttu-id="05572-103">\_ \_ Geometrische Aperture- \_ Attribut für MF MT</span><span class="sxs-lookup"><span data-stu-id="05572-103">MF\_MT\_GEOMETRIC\_APERTURE attribute</span></span>

<span data-ttu-id="05572-104">Definiert die geometrische Öffnung für einen Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="05572-104">Defines the geometric aperture for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="05572-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="05572-105">Data type</span></span>

<span data-ttu-id="05572-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="05572-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="05572-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05572-107">Remarks</span></span>

<span data-ttu-id="05572-108">Der Wert dieses Attributs ist eine [**MF Video Area**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="05572-108">The value of this attribute is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="05572-109">Das Bildseiten Verhältnis wird relativ zur geometrischen Öffnung berechnet, wobei die folgende Formel verwendet wird: Bildseiten Verhältnis = (geometrische Aperture Width/geometrische Aperture Height) × Pixel Seitenverhältnis.</span><span class="sxs-lookup"><span data-stu-id="05572-109">The picture aspect ratio is calculated relative to the geometric aperture, using the following formula: Picture aspect ratio = (geometric aperture width / geometric aperture height) × pixel aspect ratio.</span></span>

<span data-ttu-id="05572-110">Wenn dieses Attribut nicht festgelegt ist, wird davon ausgegangen, dass es sich bei der geometrischen Öffnung um den gesamten Videorahmen handelt.</span><span class="sxs-lookup"><span data-stu-id="05572-110">If this attribute is not set, the geometric aperture is assumed to be the entire video frame.</span></span> <span data-ttu-id="05572-111">Dieses Attribut sollte nur festgelegt werden, wenn der Medientyp einen Videostandard mit einem definierten aktiven Bereich beschreibt.</span><span class="sxs-lookup"><span data-stu-id="05572-111">You should set this attribute only when the media type describes a video standard with a defined active area.</span></span>

<span data-ttu-id="05572-112">In NTSC TV lautet der Videorahmen beispielsweise 720 × 480 mit einem aktiven Bereich von 704 × 480 und einem Seitenverhältnis von 10:11 Pixel.</span><span class="sxs-lookup"><span data-stu-id="05572-112">For example, in NTSC television the video frame is 720 × 480 with an active area of 704 × 480 and a 10:11 pixel aspect ratio.</span></span> <span data-ttu-id="05572-113">Das resultierende Bild hat ein Seitenverhältnis von (704/480) × (10/11) = 4:3.</span><span class="sxs-lookup"><span data-stu-id="05572-113">The resulting picture has an aspect ratio of (704/480) × (10/11) = 4:3.</span></span>

> [!Note]  
> <span data-ttu-id="05572-114">Der Standard Presenter für den [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) zeigt die geometrische Öffnung des Videos, falls angegeben.</span><span class="sxs-lookup"><span data-stu-id="05572-114">The default presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) shows the geometric aperture of the video, if specified.</span></span>

 

<span data-ttu-id="05572-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="05572-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="05572-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05572-116">Examples</span></span>


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a><span data-ttu-id="05572-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05572-117">Requirements</span></span>



| <span data-ttu-id="05572-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05572-118">Requirement</span></span> | <span data-ttu-id="05572-119">Wert</span><span class="sxs-lookup"><span data-stu-id="05572-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05572-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05572-120">Minimum supported client</span></span><br/> | <span data-ttu-id="05572-121">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="05572-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="05572-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05572-122">Minimum supported server</span></span><br/> | <span data-ttu-id="05572-123">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="05572-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="05572-124">Header</span><span class="sxs-lookup"><span data-stu-id="05572-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="05572-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="05572-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05572-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05572-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05572-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="05572-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="05572-128">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="05572-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="05572-129">Bildseiten Verhältnis</span><span class="sxs-lookup"><span data-stu-id="05572-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="05572-130">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="05572-130">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="05572-131">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="05572-131">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="05572-132">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="05572-132">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="05572-133">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="05572-133">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="05572-134">**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**</span><span class="sxs-lookup"><span data-stu-id="05572-134">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="05572-135">**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**</span><span class="sxs-lookup"><span data-stu-id="05572-135">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




