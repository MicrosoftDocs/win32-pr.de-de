---
description: Gibt die unterstützten Verwendungs Modi für einen H. 264-Videostream an.
ms.assetid: EEAE0B57-9731-4032-80A3-6A1AD11214EC
title: MF_MT_H264_SUPPORTED_USAGES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d1803c532e005c9fca8fca2fcd5cf211214989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350459"
---
# <a name="mf_mt_h264_supported_usages-attribute"></a><span data-ttu-id="6d61c-103">Das MF \_ MT \_ H264 supported-Attribut " \_ \_ Verwendungen"</span><span class="sxs-lookup"><span data-stu-id="6d61c-103">MF\_MT\_H264\_SUPPORTED\_USAGES attribute</span></span>

<span data-ttu-id="6d61c-104">Gibt die unterstützten Verwendungs Modi für einen H. 264-Videostream an.</span><span class="sxs-lookup"><span data-stu-id="6d61c-104">Specifies the supported usage modes for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="6d61c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6d61c-105">Data type</span></span>

<span data-ttu-id="6d61c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6d61c-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6d61c-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="6d61c-107">Get/set</span></span>

<span data-ttu-id="6d61c-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6d61c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6d61c-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6d61c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6d61c-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="6d61c-110">Applies to</span></span>

[<span data-ttu-id="6d61c-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="6d61c-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="6d61c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d61c-112">Remarks</span></span>

<span data-ttu-id="6d61c-113">Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="6d61c-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="6d61c-114">Der Wert entspricht dem Feld **bmsupportedumps** im UVC 1,5 H. 264-Video Frame Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="6d61c-114">The value corresponds to the **bmSupportedUsages** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="6d61c-115">Dieses Attribut wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d61c-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d61c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d61c-116">Requirements</span></span>



| <span data-ttu-id="6d61c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d61c-117">Requirement</span></span> | <span data-ttu-id="6d61c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6d61c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d61c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d61c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d61c-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6d61c-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6d61c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d61c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d61c-122">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6d61c-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6d61c-123">Header</span><span class="sxs-lookup"><span data-stu-id="6d61c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d61c-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d61c-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d61c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d61c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d61c-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6d61c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d61c-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="6d61c-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




