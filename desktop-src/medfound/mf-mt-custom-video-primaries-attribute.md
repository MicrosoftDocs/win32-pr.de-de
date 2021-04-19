---
description: Gibt benutzerdefinierte Farb-Primärwerte für einen Video Medientyp an.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: MF_MT_CUSTOM_VIDEO_PRIMARIES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349689"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a><span data-ttu-id="9610e-103">\_ \_ Benutzerdefiniertes MF MT- \_ \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="9610e-103">MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="9610e-104">Gibt benutzerdefinierte Farb-Primärwerte für einen Video Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="9610e-104">Specifies custom color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="9610e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9610e-105">Data type</span></span>

<span data-ttu-id="9610e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9610e-106">**UINT32**</span></span>

<span data-ttu-id="9610e-107">Bytearray</span><span class="sxs-lookup"><span data-stu-id="9610e-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="9610e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9610e-108">Remarks</span></span>

<span data-ttu-id="9610e-109">Bei den Attributdaten handelt es sich um eine [**\_ benutzerdefinierte MT- \_ Video \_ primär**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) Struktur</span><span class="sxs-lookup"><span data-stu-id="9610e-109">The attribute data is an [**MT\_CUSTOM\_VIDEO\_PRIMARIES**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) structure.</span></span>

<span data-ttu-id="9610e-110">Dieses Attribut gibt die tatsächliche Farb Menge des Inhalts oder einer Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="9610e-110">This attribute specifies the actual color volume of content or a display.</span></span> <span data-ttu-id="9610e-111">CEA-861,3/SMPTE St. 2086 Color Volume-Debuginformationen werden von Decodern in diesem Attribut gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9610e-111">CEA-861.3 / SMPTE ST.2086 color volume mastering information is stored in this attribute by decoders.</span></span> <span data-ttu-id="9610e-112">Beachten Sie, dass dieses Attribut das [**MF \_ MT- \_ Video- \_ Primary**](mf-mt-video-primaries-attribute.md)-Attribut nicht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9610e-112">Note that this attribute does not replace the [**MF\_MT\_VIDEO\_PRIMARIES**](mf-mt-video-primaries-attribute.md)attribute.</span></span> <span data-ttu-id="9610e-113">Dieses Attribut beschreibt einen Hinweis zum Farbvolumen des Inhalts, während die **MF- \_ MT-Video- \_ \_ primär** Punkte die Farb Replikate beschreiben, in denen der Inhalt tatsächlich codiert ist (z. b. die Bedeutung von 1,0 in den R/g/B-Kanälen einer Gleit Komma Darstellung).</span><span class="sxs-lookup"><span data-stu-id="9610e-113">This attribute describes a hint about the color volume of the content, whereas **MF\_MT\_VIDEO\_PRIMARIES** describes the color primaries in which the content is actually coded (e.g: the meaning of 1.0 in the R/G/B channels of a floating point representation).</span></span>

<span data-ttu-id="9610e-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9610e-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9610e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9610e-115">Requirements</span></span>



| <span data-ttu-id="9610e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9610e-116">Requirement</span></span> | <span data-ttu-id="9610e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9610e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9610e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9610e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9610e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9610e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9610e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9610e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9610e-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9610e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9610e-122">Header</span><span class="sxs-lookup"><span data-stu-id="9610e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9610e-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9610e-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9610e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9610e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9610e-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9610e-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9610e-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="9610e-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="9610e-127">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="9610e-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="9610e-128">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="9610e-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="9610e-129">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="9610e-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




