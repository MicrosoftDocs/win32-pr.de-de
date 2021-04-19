---
description: Gibt die Typen der Synchronisierungs Rahmen an, die für einen H. 264-Videostream unterstützt werden.
ms.assetid: A2E548F1-A5FA-4110-AD07-46BE9D7DC4A5
title: MF_MT_H264_SUPPORTED_SYNC_FRAME_TYPES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c328cbdef60750f2df7e9af403d8748c37d53b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355486"
---
# <a name="mf_mt_h264_supported_sync_frame_types-attribute"></a><span data-ttu-id="9b454-103">Das MF \_ MT \_ H264 supported-Attribut für \_ \_ Synchronisierungs \_ Frame \_ Typen</span><span class="sxs-lookup"><span data-stu-id="9b454-103">MF\_MT\_H264\_SUPPORTED\_SYNC\_FRAME\_TYPES attribute</span></span>

<span data-ttu-id="9b454-104">Gibt die Typen der Synchronisierungs Rahmen an, die für einen H. 264-Videostream unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9b454-104">Specifies the types of synchronization frame that are supported for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="9b454-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9b454-105">Data type</span></span>

<span data-ttu-id="9b454-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9b454-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9b454-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="9b454-107">Get/set</span></span>

<span data-ttu-id="9b454-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9b454-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9b454-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9b454-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9b454-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="9b454-110">Applies to</span></span>

[<span data-ttu-id="9b454-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="9b454-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="9b454-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b454-112">Remarks</span></span>

<span data-ttu-id="9b454-113">Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="9b454-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="9b454-114">Der Wert entspricht dem Feld **bmsupportedsyncframetypes** im UVC 1,5 H. 264-Videoformat Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="9b454-114">The value corresponds to the **bmSupportedSyncFrameTypes** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="9b454-115">Dieses Attribut wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b454-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b454-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b454-116">Requirements</span></span>



| <span data-ttu-id="9b454-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b454-117">Requirement</span></span> | <span data-ttu-id="9b454-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9b454-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b454-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b454-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9b454-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9b454-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9b454-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b454-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9b454-122">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9b454-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9b454-123">Header</span><span class="sxs-lookup"><span data-stu-id="9b454-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b454-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b454-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b454-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b454-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b454-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9b454-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9b454-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="9b454-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




