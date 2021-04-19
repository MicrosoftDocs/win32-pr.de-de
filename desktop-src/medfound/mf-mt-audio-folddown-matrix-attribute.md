---
description: Gibt an, wie ein Audiodecoder Multichannel-Audiodaten in Stereoausgabe umwandeln soll. Dieser Prozess wird auch als "fold-down" bezeichnet.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: MF_MT_AUDIO_FOLDDOWN_MATRIX-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347054"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a><span data-ttu-id="26965-104">Attribut "MF \_ MT \_ - \_ audiofolddown- \_ Matrix"</span><span class="sxs-lookup"><span data-stu-id="26965-104">MF\_MT\_AUDIO\_FOLDDOWN\_MATRIX attribute</span></span>

<span data-ttu-id="26965-105">Gibt an, wie ein Audiodecoder Multichannel-Audiodaten in Stereoausgabe umwandeln soll.</span><span class="sxs-lookup"><span data-stu-id="26965-105">Specifies how an audio decoder should transform multichannel audio to stereo output.</span></span> <span data-ttu-id="26965-106">Dieser Prozess wird auch als " *Fold-Down*" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="26965-106">This process is also called *fold-down*.</span></span>

## <a name="data-type"></a><span data-ttu-id="26965-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="26965-107">Data type</span></span>

<span data-ttu-id="26965-108">Bytearray</span><span class="sxs-lookup"><span data-stu-id="26965-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="26965-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26965-109">Remarks</span></span>

<span data-ttu-id="26965-110">Dieses Attribut gilt für audiomedientypen.</span><span class="sxs-lookup"><span data-stu-id="26965-110">This attribute applies to audio media types.</span></span>

<span data-ttu-id="26965-111">Der Wert dieses Attributs ist eine [**mffolddown- \_ Matrix**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) Struktur.</span><span class="sxs-lookup"><span data-stu-id="26965-111">The value of this attribute is an [**MFFOLDDOWN\_MATRIX**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) structure.</span></span>

<span data-ttu-id="26965-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="26965-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="26965-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26965-113">Requirements</span></span>



| <span data-ttu-id="26965-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26965-114">Requirement</span></span> | <span data-ttu-id="26965-115">Wert</span><span class="sxs-lookup"><span data-stu-id="26965-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26965-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26965-116">Minimum supported client</span></span><br/> | <span data-ttu-id="26965-117">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="26965-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="26965-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26965-118">Minimum supported server</span></span><br/> | <span data-ttu-id="26965-119">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="26965-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="26965-120">Header</span><span class="sxs-lookup"><span data-stu-id="26965-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="26965-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="26965-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26965-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26965-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26965-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="26965-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26965-124">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="26965-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="26965-125">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="26965-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="26965-126">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="26965-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="26965-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="26965-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




