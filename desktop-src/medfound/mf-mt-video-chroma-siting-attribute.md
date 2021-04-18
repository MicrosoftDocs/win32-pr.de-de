---
description: Beschreibt, wie Chroma für einen YCbCr-Video Medientyp getestet wurde.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: MF_MT_VIDEO_CHROMA_SITING-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347656"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a><span data-ttu-id="17041-103">MF \_ MT- \_ Video- \_ Chroma- \_ siting-Attribut</span><span class="sxs-lookup"><span data-stu-id="17041-103">MF\_MT\_VIDEO\_CHROMA\_SITING attribute</span></span>

<span data-ttu-id="17041-104">Beschreibt, wie Chroma für den Video Medientyp "y' cb' CR '" abgefragt wurde.</span><span class="sxs-lookup"><span data-stu-id="17041-104">Describes how chroma was sampled for a Y'Cb'Cr' video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="17041-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="17041-105">Data type</span></span>

<span data-ttu-id="17041-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="17041-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="17041-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17041-107">Remarks</span></span>

<span data-ttu-id="17041-108">Der Wert dieses Attributs ist ein bitweises **or** von Flags aus der [**MF videochromasubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="17041-108">The value of this attribute is a bitwise **OR** of flags from the [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) enumeration.</span></span>

<span data-ttu-id="17041-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="17041-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="17041-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17041-110">Requirements</span></span>



| <span data-ttu-id="17041-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17041-111">Requirement</span></span> | <span data-ttu-id="17041-112">Wert</span><span class="sxs-lookup"><span data-stu-id="17041-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17041-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17041-113">Minimum supported client</span></span><br/> | <span data-ttu-id="17041-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="17041-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="17041-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17041-115">Minimum supported server</span></span><br/> | <span data-ttu-id="17041-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="17041-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="17041-117">Header</span><span class="sxs-lookup"><span data-stu-id="17041-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="17041-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="17041-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17041-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17041-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17041-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="17041-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="17041-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="17041-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="17041-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="17041-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="17041-123">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="17041-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="17041-124">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="17041-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="17041-125">Erweiterte Farbinformationen</span><span class="sxs-lookup"><span data-stu-id="17041-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




