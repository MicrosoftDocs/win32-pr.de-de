---
description: Gibt das MPEG-2-oder H. 264-Profil in einem Video Medientyp an.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: MF_MT_MPEG2_PROFILE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866571"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a><span data-ttu-id="42a36-103">MF- \_ MT- \_ Profil- \_ Profil Attribut</span><span class="sxs-lookup"><span data-stu-id="42a36-103">MF\_MT\_MPEG2\_PROFILE attribute</span></span>

<span data-ttu-id="42a36-104">Gibt das MPEG-2-oder H. 264-Profil in einem Video Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="42a36-104">Specifies the MPEG-2 or H.264 profile in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="42a36-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="42a36-105">Data type</span></span>

<span data-ttu-id="42a36-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="42a36-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="42a36-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42a36-107">Remarks</span></span>

<span data-ttu-id="42a36-108">Bei MPEG-2-Video ist der Wert dieses Attributs ein Member der [**am \_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="42a36-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) enumeration.</span></span>

<span data-ttu-id="42a36-109">Für das H. 264-Video ist der Wert ein Member der [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="42a36-109">For H.264 video, the value is a member of the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span>

<span data-ttu-id="42a36-110">Dieses Attribut entspricht dem **dwprofile** -Member der [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="42a36-110">This attribute corresponds to the **dwProfile** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="42a36-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="42a36-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a36-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42a36-112">Requirements</span></span>



| <span data-ttu-id="42a36-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a36-113">Requirement</span></span> | <span data-ttu-id="42a36-114">Wert</span><span class="sxs-lookup"><span data-stu-id="42a36-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42a36-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42a36-115">Minimum supported client</span></span><br/> | <span data-ttu-id="42a36-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="42a36-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="42a36-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42a36-117">Minimum supported server</span></span><br/> | <span data-ttu-id="42a36-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="42a36-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="42a36-119">Header</span><span class="sxs-lookup"><span data-stu-id="42a36-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a36-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a36-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a36-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42a36-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a36-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="42a36-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="42a36-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="42a36-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="42a36-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="42a36-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="42a36-125">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="42a36-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="42a36-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="42a36-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
