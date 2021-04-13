---
description: Gibt die MPEG-2-oder H. 264-Ebene in einem Video Medientyp an.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: MF_MT_MPEG2_LEVEL-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111c4b30befb1d4b25a688d25f46f02bcef21541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216884"
---
# <a name="mf_mt_mpeg2_level-attribute"></a><span data-ttu-id="1e9ee-103">MF-MT-Attribut auf der \_ \_ \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="1e9ee-103">MF\_MT\_MPEG2\_LEVEL attribute</span></span>

<span data-ttu-id="1e9ee-104">Gibt die MPEG-2-oder H. 264-Ebene in einem Video Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-104">Specifies the MPEG-2 or H.264 level in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e9ee-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1e9ee-105">Data type</span></span>

<span data-ttu-id="1e9ee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1e9ee-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1e9ee-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e9ee-107">Remarks</span></span>

<span data-ttu-id="1e9ee-108">Bei MPEG-2-Video ist der Wert dieses Attributs ein Member der [**am \_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) enumeration.</span></span>

<span data-ttu-id="1e9ee-109">Für das H. 264-Video ist der Wert ein Member der [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-109">For H.264 video, the value is a member of the [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) enumeration.</span></span>

<span data-ttu-id="1e9ee-110">Dieses Attribut entspricht dem **dwlevel** -Member der [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-110">This attribute corresponds to the **dwLevel** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="1e9ee-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="1e9ee-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9ee-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e9ee-112">Requirements</span></span>



| <span data-ttu-id="1e9ee-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e9ee-113">Requirement</span></span> | <span data-ttu-id="1e9ee-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1e9ee-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9ee-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e9ee-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1e9ee-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1e9ee-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1e9ee-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e9ee-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1e9ee-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1e9ee-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1e9ee-119">Header</span><span class="sxs-lookup"><span data-stu-id="1e9ee-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e9ee-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e9ee-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e9ee-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e9ee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9ee-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="1e9ee-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e9ee-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1e9ee-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1e9ee-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1e9ee-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1e9ee-125">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="1e9ee-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1e9ee-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="1e9ee-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
