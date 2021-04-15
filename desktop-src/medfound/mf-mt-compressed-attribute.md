---
description: Gibt für einen Medientyp an, ob die Mediendaten komprimiert sind.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: MF_MT_COMPRESSED-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528238"
---
# <a name="mf_mt_compressed-attribute"></a><span data-ttu-id="ac4f8-103">\_Komprimiertes MF MT- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="ac4f8-103">MF\_MT\_COMPRESSED attribute</span></span>

<span data-ttu-id="ac4f8-104">Gibt für einen Medientyp an, ob die Mediendaten komprimiert sind.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-104">Specifies for a media type whether the media data is compressed.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac4f8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ac4f8-105">Data type</span></span>

<span data-ttu-id="ac4f8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ac4f8-106">**UINT32**</span></span>

<span data-ttu-id="ac4f8-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac4f8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac4f8-108">Remarks</span></span>

<span data-ttu-id="ac4f8-109">Wenn dieses Attribut **true** ist, ist der Medientyp ein komprimiertes Format.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-109">If this attribute is **TRUE**, the media type is a compressed format.</span></span> <span data-ttu-id="ac4f8-110">Andernfalls ist entweder der Medientyp unkomprimiert, oder der Komprimierungstyp ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-110">Otherwise, either the media type is uncompressed or the compression type is not known.</span></span>

<span data-ttu-id="ac4f8-111">Es ist nicht garantiert, dass dieses Attribut für alle komprimierten Formate auf **true** festgelegt ist, sodass Anwendungen in der Regel nicht dieses Attribut verlassen sollten.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-111">This attribute is not guaranteed to be set to **TRUE** for all compressed formats, so applications should generally not rely this attribute.</span></span> <span data-ttu-id="ac4f8-112">Die zuverlässigste Möglichkeit, um zu bestimmen, ob ein Format komprimiert ist, besteht darin, eine Liste bekannter Formate beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-112">The most reliable way to determine whether a format is compressed is to maintain a list of known formats.</span></span> <span data-ttu-id="ac4f8-113">Wenn eine Anwendung ein Format nicht erkennt, wie im [**MF \_ MT- \_ SubType**](mf-mt-subtype-attribute.md) -Attribut angegeben, sollte Sie nichts über die Komprimierung des Formats annehmen.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-113">If an application does not recognize a format, as specified in the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute, it should not assume anything about the compression of the format.</span></span>

<span data-ttu-id="ac4f8-114">Um zu ermitteln, ob ein Format die Temporale Komprimierung verwendet (was bedeutet, dass einige Beispiele als Delta aus früheren Beispielen berechnet werden), überprüfen Sie das " [**MF \_ MT \_ All \_ Samples \_ Independent**](mf-mt-all-samples-independent-attribute.md) "-Attribut.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-114">To determine whether a format uses temporal compression (meaning that some samples are computed as deltas from earlier samples), check the [**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) attribute.</span></span>

<span data-ttu-id="ac4f8-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac4f8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac4f8-116">Requirements</span></span>



| <span data-ttu-id="ac4f8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac4f8-117">Requirement</span></span> | <span data-ttu-id="ac4f8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ac4f8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4f8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac4f8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac4f8-120">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ac4f8-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ac4f8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac4f8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac4f8-122">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ac4f8-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ac4f8-123">Header</span><span class="sxs-lookup"><span data-stu-id="ac4f8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac4f8-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac4f8-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac4f8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac4f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4f8-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ac4f8-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac4f8-127">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ac4f8-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ac4f8-128">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ac4f8-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ac4f8-129">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="ac4f8-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ac4f8-130">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="ac4f8-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




