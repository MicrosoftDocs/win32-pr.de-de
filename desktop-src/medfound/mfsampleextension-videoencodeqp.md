---
description: Gibt den Quantisierungsparameter (QP) an, der zum Codieren eines Video Beispiels verwendet wurde.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: MFSampleExtension_VideoEncodeQP-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721f5df00ff24b307daed2ccbcbf61a04b129db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354622"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a><span data-ttu-id="f2843-103">MF Sample Extension- \_ videoencodeqp-Attribut</span><span class="sxs-lookup"><span data-stu-id="f2843-103">MFSampleExtension\_VideoEncodeQP attribute</span></span>

<span data-ttu-id="f2843-104">Gibt den Quantisierungsparameter (QP) an, der zum Codieren eines Video Beispiels verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2843-104">Specifies the quantization parameter (QP) that was used to encode a video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="f2843-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f2843-105">Data type</span></span>

<span data-ttu-id="f2843-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f2843-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="f2843-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="f2843-107">Get/set</span></span>

<span data-ttu-id="f2843-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="f2843-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="f2843-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="f2843-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f2843-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="f2843-110">Applies to</span></span>

[<span data-ttu-id="f2843-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="f2843-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="f2843-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2843-112">Remarks</span></span>

<span data-ttu-id="f2843-113">Der [**H. 264-Video Encoder**](h-264-video-encoder.md) legt dieses Attribut für die generierten Ausgabe Beispiele fest.</span><span class="sxs-lookup"><span data-stu-id="f2843-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2843-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2843-114">Requirements</span></span>



| <span data-ttu-id="f2843-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2843-115">Requirement</span></span> | <span data-ttu-id="f2843-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f2843-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2843-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2843-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2843-118">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f2843-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f2843-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2843-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2843-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f2843-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="f2843-121">Header</span><span class="sxs-lookup"><span data-stu-id="f2843-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2843-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2843-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2843-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2843-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2843-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f2843-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2843-125">**H. 264-Video Encoder**</span><span class="sxs-lookup"><span data-stu-id="f2843-125">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="f2843-126">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="f2843-126">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2843-127">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2843-127">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




