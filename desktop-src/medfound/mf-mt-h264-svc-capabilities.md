---
description: Gibt die SVC-Funktionen eines H. 264-Videodaten Stroms an.
ms.assetid: B727D9D2-6126-41F8-A27A-743640FE3AE4
title: MF_MT_H264_SVC_CAPABILITIES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35a39b5f1727af8399d9d0c56c93d2d9d1486c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751936"
---
# <a name="mf_mt_h264_svc_capabilities-attribute"></a><span data-ttu-id="fbda2-103">Das MF \_ MT \_ H264 \_ svc-Funktionen- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="fbda2-103">MF\_MT\_H264\_SVC\_CAPABILITIES attribute</span></span>

<span data-ttu-id="fbda2-104">Gibt die SVC-Funktionen eines H. 264-Videodaten Stroms an.</span><span class="sxs-lookup"><span data-stu-id="fbda2-104">Specifies the SVC capabilities of an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="fbda2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fbda2-105">Data type</span></span>

<span data-ttu-id="fbda2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fbda2-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="fbda2-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="fbda2-107">Get/set</span></span>

<span data-ttu-id="fbda2-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="fbda2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="fbda2-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="fbda2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="fbda2-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="fbda2-110">Applies to</span></span>

[<span data-ttu-id="fbda2-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="fbda2-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="fbda2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbda2-112">Remarks</span></span>

<span data-ttu-id="fbda2-113">Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="fbda2-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="fbda2-114">Der Wert entspricht dem **bmsvccapabili-** Feld im Video Frame Deskriptor UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="fbda2-114">The value corresponds to the **bmSVCCapabilities** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="fbda2-115">Dieses Attribut wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbda2-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbda2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbda2-116">Requirements</span></span>



| <span data-ttu-id="fbda2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbda2-117">Requirement</span></span> | <span data-ttu-id="fbda2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fbda2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fbda2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbda2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fbda2-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fbda2-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="fbda2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbda2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fbda2-122">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fbda2-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fbda2-123">Header</span><span class="sxs-lookup"><span data-stu-id="fbda2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbda2-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbda2-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbda2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbda2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbda2-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="fbda2-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fbda2-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="fbda2-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




