---
description: Definiert die schwenken-/Scan-Aperture. Dies ist der 4&\# 215; 3 Bereich von Video, der im Pan/Scan-Modus angezeigt werden soll.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: MF_MT_PAN_SCAN_APERTURE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348238"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a><span data-ttu-id="c5bd8-103">Das MF \_ MT \_ Pan-Scan-Aperture- \_ \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="c5bd8-103">MF\_MT\_PAN\_SCAN\_APERTURE attribute</span></span>

<span data-ttu-id="c5bd8-104">Definiert die schwenken-/Scan-Aperture. Dies ist der 4 × 3-Bereich des Videos, der im Pan/Scan-Modus angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5bd8-104">Defines the pan/scan aperture, which is the 4×3 region of video that should be displayed in pan/scan mode.</span></span>

## <a name="data-type"></a><span data-ttu-id="c5bd8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c5bd8-105">Data type</span></span>

<span data-ttu-id="c5bd8-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="c5bd8-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="c5bd8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5bd8-107">Remarks</span></span>

<span data-ttu-id="c5bd8-108">Der Attribut Wert ist eine [**MF Video Area**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c5bd8-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="c5bd8-109">Dieses Attribut wird verwendet, um ein Grafik Video zu einem 4:3-Seitenverhältnis zu schneiden.</span><span class="sxs-lookup"><span data-stu-id="c5bd8-109">This attribute is used to crop widescreen video to a 4:3 aspect ratio.</span></span> <span data-ttu-id="c5bd8-110">Die Pan/Scan-Öffnung wird nur im Pan/Scan-Modus verwendet, der aktiviert wird, indem das [**MF \_ MT \_ Pan \_ Scan \_ aktivierte**](mf-mt-pan-scan-enabled-attribute.md) Attribut auf " **true**" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c5bd8-110">The pan/scan aperture is used only in pan/scan mode, which is enabled by setting the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="c5bd8-111">Wenn der Pan/Scan-Modus nicht aktiviert ist, verwenden Sie die Anzeige Öffnung, die durch das Attribut " [**MF \_ MT \_ minimal \_ Display \_ Aperture**](mf-mt-minimum-display-aperture-attribute.md) " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5bd8-111">If pan/scan mode is not enabled, use the display aperture, specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="c5bd8-112">Wenn dieses Attribut nicht festgelegt ist, wird angenommen, dass es sich bei der Pan/Scan-Öffnung um den gesamten Videorahmen handelt.</span><span class="sxs-lookup"><span data-stu-id="c5bd8-112">If this attribute is not set, the pan/scan aperture is assumed to be the entire video frame.</span></span>

<span data-ttu-id="c5bd8-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c5bd8-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5bd8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5bd8-114">Requirements</span></span>



| <span data-ttu-id="c5bd8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5bd8-115">Requirement</span></span> | <span data-ttu-id="c5bd8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c5bd8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bd8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5bd8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5bd8-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c5bd8-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c5bd8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5bd8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5bd8-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c5bd8-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c5bd8-121">Header</span><span class="sxs-lookup"><span data-stu-id="c5bd8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5bd8-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5bd8-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5bd8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5bd8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bd8-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c5bd8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c5bd8-125">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="c5bd8-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="c5bd8-126">Bildseiten Verhältnis</span><span class="sxs-lookup"><span data-stu-id="c5bd8-126">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="c5bd8-127">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="c5bd8-127">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="c5bd8-128">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="c5bd8-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="c5bd8-129">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="c5bd8-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="c5bd8-130">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="c5bd8-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c5bd8-131">**\_geometrische Monte-MT- \_ \_ Öffnung**</span><span class="sxs-lookup"><span data-stu-id="c5bd8-131">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="c5bd8-132">**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**</span><span class="sxs-lookup"><span data-stu-id="c5bd8-132">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="c5bd8-133">**MF- \_ MT- \_ Schwenken- \_ Scan \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="c5bd8-133">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




