---
description: Enthält den MPEG-1-oder MPEG-2-Sequenz Header für einen Video Medientyp.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: MF_MT_MPEG_SEQUENCE_HEADER-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350349"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a><span data-ttu-id="54c49-103">MF- \_ MT- \_ MPEG- \_ Sequenz \_ Header Attribut</span><span class="sxs-lookup"><span data-stu-id="54c49-103">MF\_MT\_MPEG\_SEQUENCE\_HEADER attribute</span></span>

<span data-ttu-id="54c49-104">Enthält den MPEG-1-oder MPEG-2-Sequenz Header für einen Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="54c49-104">Contains the MPEG-1 or MPEG-2 sequence header for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="54c49-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="54c49-105">Data type</span></span>

<span data-ttu-id="54c49-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="54c49-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="54c49-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54c49-107">Remarks</span></span>

<span data-ttu-id="54c49-108">Dieses Attribut entspricht dem **dwsequenceheader** -Member der [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur oder dem **bsequenceheader** -Member der [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="54c49-108">This attribute corresponds to the **dwSequenceHeader** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure, or the **bSequenceHeader** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) structure.</span></span>

<span data-ttu-id="54c49-109">Im H264-und H265-Video enthält das BLOB verketteten [nal-Einheiten](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) im Anhang B-Format sowie die zugehörigen Start Codes.</span><span class="sxs-lookup"><span data-stu-id="54c49-109">For h264 and h265 video, the blob contains concatenated [NAL units](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) in Annex B format, along with their start codes.</span></span> <span data-ttu-id="54c49-110">Speziell für H264 Video sind Sie SPS & PPS-nal-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="54c49-110">Specifically, for h264 video they are SPS & PPS NAL units.</span></span> <span data-ttu-id="54c49-111">Für H265 sind Sie VPS, SPS & PPS.</span><span class="sxs-lookup"><span data-stu-id="54c49-111">For h265 they are VPS, SPS & PPS.</span></span>

<span data-ttu-id="54c49-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="54c49-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="54c49-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54c49-113">Requirements</span></span>



| <span data-ttu-id="54c49-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54c49-114">Requirement</span></span> | <span data-ttu-id="54c49-115">Wert</span><span class="sxs-lookup"><span data-stu-id="54c49-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54c49-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54c49-116">Minimum supported client</span></span><br/> | <span data-ttu-id="54c49-117">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="54c49-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="54c49-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54c49-118">Minimum supported server</span></span><br/> | <span data-ttu-id="54c49-119">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="54c49-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="54c49-120">Header</span><span class="sxs-lookup"><span data-stu-id="54c49-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="54c49-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="54c49-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54c49-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54c49-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54c49-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="54c49-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="54c49-124">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="54c49-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="54c49-125">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="54c49-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="54c49-126">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="54c49-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="54c49-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="54c49-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
