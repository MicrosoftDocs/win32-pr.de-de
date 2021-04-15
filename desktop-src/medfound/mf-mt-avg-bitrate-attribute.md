---
description: Ungefähre Datenrate des Videodaten Stroms in Bits pro Sekunde für einen Video Medientyp.
ms.assetid: cf9374a7-3688-4a6c-8339-d68c267c9bed
title: MF_MT_AVG_BITRATE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4497c58abf8587e72dea47d4f8ac222a1b0692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393749"
---
# <a name="mf_mt_avg_bitrate-attribute"></a><span data-ttu-id="273be-103">Attribut "MF- \_ \_ AVG- \_ Bitrate"</span><span class="sxs-lookup"><span data-stu-id="273be-103">MF\_MT\_AVG\_BITRATE attribute</span></span>

<span data-ttu-id="273be-104">Ungefähre Datenrate des Videodaten Stroms in Bits pro Sekunde für einen Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="273be-104">Approximate data rate of the video stream, in bits per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="273be-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="273be-105">Data type</span></span>

<span data-ttu-id="273be-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="273be-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="273be-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="273be-107">Remarks</span></span>

<span data-ttu-id="273be-108">Dieses Attribut entspricht dem **dwbitrate** -Member der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -und [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="273be-108">This attribute corresponds to the **dwBitRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="273be-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="273be-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="273be-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="273be-110">Requirements</span></span>



| <span data-ttu-id="273be-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="273be-111">Requirement</span></span> | <span data-ttu-id="273be-112">Wert</span><span class="sxs-lookup"><span data-stu-id="273be-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="273be-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="273be-113">Minimum supported client</span></span><br/> | <span data-ttu-id="273be-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="273be-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="273be-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="273be-115">Minimum supported server</span></span><br/> | <span data-ttu-id="273be-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="273be-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="273be-117">Header</span><span class="sxs-lookup"><span data-stu-id="273be-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="273be-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="273be-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="273be-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="273be-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273be-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="273be-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="273be-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="273be-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="273be-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="273be-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="273be-123">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="273be-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="273be-124">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="273be-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
