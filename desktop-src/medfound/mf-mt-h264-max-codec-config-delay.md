---
description: Die maximale Anzahl von Frames, die der H. 264-Encoder benötigt, um auf einen Befehl zu antworten.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: MF_MT_H264_MAX_CODEC_CONFIG_DELAY-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362413"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a><span data-ttu-id="d55cb-103">"MF \_ MT \_ H264 \_ Max \_ Codec \_ config Delay \_ "-Attribut</span><span class="sxs-lookup"><span data-stu-id="d55cb-103">MF\_MT\_H264\_MAX\_CODEC\_CONFIG\_DELAY attribute</span></span>

<span data-ttu-id="d55cb-104">Die maximale Anzahl von Frames, die der H. 264-Encoder benötigt, um auf einen Befehl zu antworten.</span><span class="sxs-lookup"><span data-stu-id="d55cb-104">The maximum number of frames the H.264 encoder takes to respond to a command.</span></span>

## <a name="data-type"></a><span data-ttu-id="d55cb-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d55cb-105">Data type</span></span>

<span data-ttu-id="d55cb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d55cb-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d55cb-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="d55cb-107">Get/set</span></span>

<span data-ttu-id="d55cb-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d55cb-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d55cb-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d55cb-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d55cb-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="d55cb-110">Applies to</span></span>

[<span data-ttu-id="d55cb-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="d55cb-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="d55cb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d55cb-112">Remarks</span></span>

<span data-ttu-id="d55cb-113">Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="d55cb-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="d55cb-114">Der Wert entspricht dem Feld **bmaxcodecconfigdelay** im Videoformat Deskriptor UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="d55cb-114">The value corresponds to the **bMaxCodecConfigDelay** field in the UVC 1.2 H.264 video format descriptor.</span></span>

<span data-ttu-id="d55cb-115">Dieses Attribut wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="d55cb-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d55cb-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d55cb-116">Requirements</span></span>



| <span data-ttu-id="d55cb-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d55cb-117">Requirement</span></span> | <span data-ttu-id="d55cb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d55cb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d55cb-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d55cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d55cb-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d55cb-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d55cb-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d55cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d55cb-122">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d55cb-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d55cb-123">Header</span><span class="sxs-lookup"><span data-stu-id="d55cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d55cb-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d55cb-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d55cb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d55cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55cb-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d55cb-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d55cb-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="d55cb-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




