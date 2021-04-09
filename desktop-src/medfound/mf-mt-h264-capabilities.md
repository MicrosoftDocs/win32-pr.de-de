---
description: Gibt die Funktionen-Flags für einen H. 264-Videostream an.
ms.assetid: 59EF18D6-6063-4EF3-BBFB-51A966CFF09E
title: MF_MT_H264_CAPABILITIES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67f796e09d4b57667a3d8f7c7c0fa888eba7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868552"
---
# <a name="mf_mt_h264_capabilities-attribute"></a><span data-ttu-id="9b718-103">MF \_ MT \_ H264- \_ Funktionen-Attribut</span><span class="sxs-lookup"><span data-stu-id="9b718-103">MF\_MT\_H264\_CAPABILITIES attribute</span></span>

<span data-ttu-id="9b718-104">Gibt die Funktionen-Flags für einen H. 264-Videostream an.</span><span class="sxs-lookup"><span data-stu-id="9b718-104">Specifies the capabilities flags for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="9b718-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9b718-105">Data type</span></span>

<span data-ttu-id="9b718-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9b718-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9b718-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="9b718-107">Get/set</span></span>

<span data-ttu-id="9b718-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9b718-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9b718-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9b718-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9b718-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="9b718-110">Applies to</span></span>

[<span data-ttu-id="9b718-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="9b718-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="9b718-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b718-112">Remarks</span></span>

<span data-ttu-id="9b718-113">Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="9b718-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="9b718-114">Der Wert entspricht dem Feld **bmfunktionen** im Video Frame Deskriptor UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="9b718-114">The value corresponds to the **bmCapabilities** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="9b718-115">Dieses Attribut wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b718-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b718-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b718-116">Requirements</span></span>



| <span data-ttu-id="9b718-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b718-117">Requirement</span></span> | <span data-ttu-id="9b718-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9b718-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b718-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b718-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9b718-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9b718-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9b718-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b718-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9b718-122">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9b718-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9b718-123">Header</span><span class="sxs-lookup"><span data-stu-id="9b718-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b718-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b718-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b718-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b718-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b718-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9b718-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9b718-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="9b718-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




