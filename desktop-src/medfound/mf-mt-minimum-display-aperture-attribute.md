---
description: Definiert die Anzeige Öffnung, bei der es sich um den Bereich eines Video Rahmens handelt, der gültige Bilddaten enthält.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: MF_MT_MINIMUM_DISPLAY_APERTURE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348198"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a><span data-ttu-id="49ba2-103">Das MF \_ MT- \_ Minimal Anzeige-Aperture- \_ \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="49ba2-103">MF\_MT\_MINIMUM\_DISPLAY\_APERTURE attribute</span></span>

<span data-ttu-id="49ba2-104">Definiert die Anzeige Öffnung, bei der es sich um den Bereich eines Video Rahmens handelt, der gültige Bilddaten enthält.</span><span class="sxs-lookup"><span data-stu-id="49ba2-104">Defines the display aperture, which is the region of a video frame that contains valid image data.</span></span>

## <a name="data-type"></a><span data-ttu-id="49ba2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="49ba2-105">Data type</span></span>

<span data-ttu-id="49ba2-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="49ba2-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="49ba2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49ba2-107">Remarks</span></span>

<span data-ttu-id="49ba2-108">Der Attribut Wert ist eine [**MF Video Area**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="49ba2-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="49ba2-109">Die minimale Anzeige Öffnung ist der Bereich, der den gültigen Teil des Signals enthält.</span><span class="sxs-lookup"><span data-stu-id="49ba2-109">The minimum display aperture is the region that contains the valid portion of the signal.</span></span> <span data-ttu-id="49ba2-110">Die Pixel außerhalb der Öffnung enthalten ungültige Daten und sollten nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="49ba2-110">The pixels outside the aperture contain invalid data and should not be displayed.</span></span>

<span data-ttu-id="49ba2-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="49ba2-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ba2-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49ba2-112">Requirements</span></span>



| <span data-ttu-id="49ba2-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49ba2-113">Requirement</span></span> | <span data-ttu-id="49ba2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="49ba2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="49ba2-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49ba2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="49ba2-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="49ba2-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="49ba2-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49ba2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="49ba2-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="49ba2-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="49ba2-119">Header</span><span class="sxs-lookup"><span data-stu-id="49ba2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ba2-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="49ba2-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49ba2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49ba2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ba2-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="49ba2-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="49ba2-123">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="49ba2-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="49ba2-124">Bildseiten Verhältnis</span><span class="sxs-lookup"><span data-stu-id="49ba2-124">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="49ba2-125">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="49ba2-125">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="49ba2-126">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="49ba2-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="49ba2-127">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="49ba2-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="49ba2-128">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="49ba2-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="49ba2-129">**\_geometrische Monte-MT- \_ \_ Öffnung**</span><span class="sxs-lookup"><span data-stu-id="49ba2-129">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="49ba2-130">**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**</span><span class="sxs-lookup"><span data-stu-id="49ba2-130">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




