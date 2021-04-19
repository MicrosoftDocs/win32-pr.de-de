---
description: Enthält verschiedene Flags für einen MPEG-2-Video Medientyp.
ms.assetid: 2e1bf3e3-c005-418b-b9fd-1d43c42dad6f
title: MF_MT_MPEG2_FLAGS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ef0a0def9c3e5413ec9b9bf7568fcbe9add851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350118"
---
# <a name="mf_mt_mpeg2_flags-attribute"></a><span data-ttu-id="bb6d8-103">MF \_ MT \_ . \_</span><span class="sxs-lookup"><span data-stu-id="bb6d8-103">MF\_MT\_MPEG2\_FLAGS attribute</span></span>

<span data-ttu-id="bb6d8-104">Enthält verschiedene Flags für einen MPEG-2-Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-104">Contains miscellaneous flags for an MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb6d8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bb6d8-105">Data type</span></span>

<span data-ttu-id="bb6d8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bb6d8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bb6d8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb6d8-107">Remarks</span></span>

<span data-ttu-id="bb6d8-108">Dieses Attribut entspricht dem **dwFlags** -Member der [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-108">This attribute corresponds to the **dwFlags** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="bb6d8-109">Eine Liste gültiger Flags finden Sie in der Dokumentation zu **MPEG2VIDEOINFO**.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-109">For a list of valid flags, see the documentation for **MPEG2VIDEOINFO**.</span></span>

<span data-ttu-id="bb6d8-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6d8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb6d8-111">Requirements</span></span>



| <span data-ttu-id="bb6d8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb6d8-112">Requirement</span></span> | <span data-ttu-id="bb6d8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="bb6d8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6d8-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb6d8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6d8-115">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb6d8-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="bb6d8-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb6d8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6d8-117">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb6d8-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="bb6d8-118">Header</span><span class="sxs-lookup"><span data-stu-id="bb6d8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb6d8-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d8-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb6d8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb6d8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6d8-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="bb6d8-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb6d8-122">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bb6d8-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bb6d8-123">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bb6d8-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="bb6d8-124">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="bb6d8-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="bb6d8-125">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="bb6d8-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
