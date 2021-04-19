---
description: Der GOP-Start Zeit Code (Group of Pictures, GOP) für einen MPEG-1-oder MPEG-2-Video Medientyp.
ms.assetid: 8313b83c-5a0a-4aaa-bdc8-58a987c329c7
title: MF_MT_MPEG_START_TIME_CODE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b19a041dbcd791359d704b407445779927d0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360684"
---
# <a name="mf_mt_mpeg_start_time_code-attribute"></a><span data-ttu-id="aa707-103">Code-Attribut für MF \_ MT MPEG- \_ \_ Start \_ Zeit \_</span><span class="sxs-lookup"><span data-stu-id="aa707-103">MF\_MT\_MPEG\_START\_TIME\_CODE attribute</span></span>

<span data-ttu-id="aa707-104">Der GOP-Start Zeit Code (Group of Pictures, GOP) für einen MPEG-1-oder MPEG-2-Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="aa707-104">Group-of-pictures (GOP) start time code, for an MPEG-1 or MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="aa707-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="aa707-105">Data type</span></span>

<span data-ttu-id="aa707-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="aa707-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="aa707-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa707-107">Remarks</span></span>

<span data-ttu-id="aa707-108">Dieses Attribut entspricht dem **dwstarttimecode** -Member der [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) -und [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="aa707-108">This attribute corresponds to the **dwStartTimeCode** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) and [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structures.</span></span>

<span data-ttu-id="aa707-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="aa707-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa707-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa707-110">Requirements</span></span>



| <span data-ttu-id="aa707-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa707-111">Requirement</span></span> | <span data-ttu-id="aa707-112">Wert</span><span class="sxs-lookup"><span data-stu-id="aa707-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa707-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa707-113">Minimum supported client</span></span><br/> | <span data-ttu-id="aa707-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="aa707-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="aa707-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa707-115">Minimum supported server</span></span><br/> | <span data-ttu-id="aa707-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="aa707-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="aa707-117">Header</span><span class="sxs-lookup"><span data-stu-id="aa707-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa707-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa707-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa707-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa707-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa707-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="aa707-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aa707-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="aa707-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="aa707-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="aa707-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="aa707-123">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="aa707-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="aa707-124">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="aa707-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="aa707-125">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="aa707-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 
