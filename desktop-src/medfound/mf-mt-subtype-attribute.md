---
description: Untertyp-GUID für einen Medientyp.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: MF_MT_SUBTYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042337"
---
# <a name="mf_mt_subtype-attribute"></a><span data-ttu-id="c2037-103">MF \_ - \_ Untertypen Attribut</span><span class="sxs-lookup"><span data-stu-id="c2037-103">MF\_MT\_SUBTYPE attribute</span></span>

<span data-ttu-id="c2037-104">Untertyp-GUID für einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="c2037-104">Subtype GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2037-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c2037-105">Data type</span></span>

<span data-ttu-id="c2037-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="c2037-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="c2037-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2037-107">Remarks</span></span>

<span data-ttu-id="c2037-108">Der Untertyp-GUID definiert einen bestimmten Medien Formattyp innerhalb eines Haupt Typs.</span><span class="sxs-lookup"><span data-stu-id="c2037-108">The subtype GUID defines a specific media format type within a major type.</span></span> <span data-ttu-id="c2037-109">In Videos enthalten die Untertypen z. b. RGB-24, RGB-32, UYVY, ayuv usw.</span><span class="sxs-lookup"><span data-stu-id="c2037-109">For example, within video, the subtypes include RGB-24, RGB-32, UYVY, AYUV, and so forth.</span></span> <span data-ttu-id="c2037-110">In Audiodaten enthalten die Untertypen PCM-Audiodaten, Windows Media Audio 9 usw.</span><span class="sxs-lookup"><span data-stu-id="c2037-110">Within audio, the subtypes include PCM audio, Windows Media Audio 9, and so forth.</span></span>

<span data-ttu-id="c2037-111">Mögliche Werte finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c2037-111">For possible values, see the following topics:</span></span>

-   [<span data-ttu-id="c2037-112">Audiountertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="c2037-112">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
-   [<span data-ttu-id="c2037-113">Video Untertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="c2037-113">Video Subtype GUIDs</span></span>](video-subtype-guids.md)

<span data-ttu-id="c2037-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c2037-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2037-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2037-115">Requirements</span></span>



| <span data-ttu-id="c2037-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2037-116">Requirement</span></span> | <span data-ttu-id="c2037-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c2037-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2037-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2037-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c2037-119">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c2037-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c2037-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2037-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c2037-121">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c2037-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c2037-122">Header</span><span class="sxs-lookup"><span data-stu-id="c2037-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2037-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2037-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2037-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2037-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2037-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c2037-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2037-126">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="c2037-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="c2037-127">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="c2037-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="c2037-128">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="c2037-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c2037-129">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="c2037-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




