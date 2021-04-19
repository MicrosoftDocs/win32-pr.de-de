---
description: Gibt den Bildtyp an, der von einem Video Encoder ausgegeben wird.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: MFSampleExtension_VideoEncodePictureType-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348487"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a><span data-ttu-id="4b5f4-103">MF Sample Extension- \_ videoencodepicturetype-Attribut</span><span class="sxs-lookup"><span data-stu-id="4b5f4-103">MFSampleExtension\_VideoEncodePictureType attribute</span></span>

<span data-ttu-id="4b5f4-104">Gibt den Bildtyp an, der von einem Video Encoder ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4b5f4-104">Specifies the type of picture that is output by a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="4b5f4-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4b5f4-105">Data type</span></span>

<span data-ttu-id="4b5f4-106">**eAVEncH264PictureType \_ B** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b5f4-106">**eAVEncH264PictureType\_B** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4b5f4-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="4b5f4-107">Get/set</span></span>

<span data-ttu-id="4b5f4-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4b5f4-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4b5f4-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4b5f4-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4b5f4-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="4b5f4-110">Applies to</span></span>

[<span data-ttu-id="4b5f4-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="4b5f4-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="4b5f4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b5f4-112">Remarks</span></span>

<span data-ttu-id="4b5f4-113">Der [**H. 264-Video Encoder**](h-264-video-encoder.md) legt dieses Attribut für die generierten Ausgabe Beispiele fest.</span><span class="sxs-lookup"><span data-stu-id="4b5f4-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span> <span data-ttu-id="4b5f4-114">Der Wert des-Attributs ist ein Member der [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="4b5f4-114">The value of the attribute is a member of the [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b5f4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b5f4-115">Requirements</span></span>



| <span data-ttu-id="4b5f4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b5f4-116">Requirement</span></span> | <span data-ttu-id="4b5f4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4b5f4-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5f4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b5f4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4b5f4-119">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4b5f4-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4b5f4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b5f4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4b5f4-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4b5f4-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="4b5f4-122">Header</span><span class="sxs-lookup"><span data-stu-id="4b5f4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b5f4-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b5f4-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b5f4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b5f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b5f4-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4b5f4-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b5f4-126">**H. 264-Video Encoder**</span><span class="sxs-lookup"><span data-stu-id="4b5f4-126">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="4b5f4-127">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="4b5f4-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b5f4-128">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b5f4-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




