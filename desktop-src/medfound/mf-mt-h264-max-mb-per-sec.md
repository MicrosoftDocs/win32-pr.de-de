---
description: Gibt die maximale Makroblock-Verarbeitungsrate für einen H. 264-Videostream an.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: MF_MT_H264_MAX_MB_PER_SEC-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347299"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a><span data-ttu-id="6141e-103">Attribut "MF \_ MT \_ H264 \_ Max \_ MB \_ pro \_ Sekunde"</span><span class="sxs-lookup"><span data-stu-id="6141e-103">MF\_MT\_H264\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="6141e-104">Gibt die maximale Makroblock-Verarbeitungsrate für einen H. 264-Videostream an.</span><span class="sxs-lookup"><span data-stu-id="6141e-104">Specifies the maximum macroblock processing rate for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="6141e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6141e-105">Data type</span></span>

<span data-ttu-id="6141e-106">**\[ UInt32 \]** gespeichert als **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="6141e-106">**UINT32\[\]** stored as **UINT8\[\]**</span></span>

## <a name="applies-to"></a><span data-ttu-id="6141e-107">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="6141e-107">Applies to</span></span>

[<span data-ttu-id="6141e-108">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="6141e-108">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="6141e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6141e-109">Remarks</span></span>

<span data-ttu-id="6141e-110">Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="6141e-110">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="6141e-111">Der Wert des-Attributs ist ein Array von UInt32-Werten, die den folgenden Feldern im Videoformat Deskriptor UVC 1,5 H. 264 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6141e-111">The value of the attribute is an array of UINT32 values, which correspond to the following fields in the UVC 1.5 H.264 video format descriptor.</span></span>

| <span data-ttu-id="6141e-112">Array-Element</span><span class="sxs-lookup"><span data-stu-id="6141e-112">Array Element</span></span> | <span data-ttu-id="6141e-113">Deskriptorfeld</span><span class="sxs-lookup"><span data-stu-id="6141e-113">Descriptor Field</span></span>                                           |
|---------------|------------------------------------------------------------|
| <span data-ttu-id="6141e-114">0</span><span class="sxs-lookup"><span data-stu-id="6141e-114">0</span></span>             | <span data-ttu-id="6141e-115">**dwmaxmbperseconeresolutionnoscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-115">**dwMaxMBperSecOneResolutionNoScalability**</span></span>                |
| <span data-ttu-id="6141e-116">1</span><span class="sxs-lookup"><span data-stu-id="6141e-116">1</span></span>             | <span data-ttu-id="6141e-117">**dwmaxmbpersectworesolutionsnoscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span></span>               |
| <span data-ttu-id="6141e-118">2</span><span class="sxs-lookup"><span data-stu-id="6141e-118">2</span></span>             | <span data-ttu-id="6141e-119">**dwmaxmbpersecthreeresolutionsnoscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span></span>             |
| <span data-ttu-id="6141e-120">3</span><span class="sxs-lookup"><span data-stu-id="6141e-120">3</span></span>             | <span data-ttu-id="6141e-121">**dwmaxmbpersecfourresolutionsnoscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-121">**dwMaxMBperSecFourResolutionsNoScalability**</span></span>              |
| <span data-ttu-id="6141e-122">4</span><span class="sxs-lookup"><span data-stu-id="6141e-122">4</span></span>             | <span data-ttu-id="6141e-123">**dwmaxmbperseconeresolutiontemporalscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span></span>          |
| <span data-ttu-id="6141e-124">5</span><span class="sxs-lookup"><span data-stu-id="6141e-124">5</span></span>             | <span data-ttu-id="6141e-125">**dwmaxmbpersectworesolutionstemporalscalablility**</span><span class="sxs-lookup"><span data-stu-id="6141e-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span></span>        |
| <span data-ttu-id="6141e-126">6</span><span class="sxs-lookup"><span data-stu-id="6141e-126">6</span></span>             | <span data-ttu-id="6141e-127">**dwmaxmbpersecthreeresolutionstemporalscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span></span>       |
| <span data-ttu-id="6141e-128">7</span><span class="sxs-lookup"><span data-stu-id="6141e-128">7</span></span>             | <span data-ttu-id="6141e-129">**dwmaxmbpersecfourresolutionstemportscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span></span>        |
| <span data-ttu-id="6141e-130">8</span><span class="sxs-lookup"><span data-stu-id="6141e-130">8</span></span>             | <span data-ttu-id="6141e-131">**dwmaxmbperseconeresolutiontemporalqualityscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span></span>   |
| <span data-ttu-id="6141e-132">9</span><span class="sxs-lookup"><span data-stu-id="6141e-132">9</span></span>             | <span data-ttu-id="6141e-133">**dwmaxmbpersectworesolutionstemporalqualityscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span></span>  |
| <span data-ttu-id="6141e-134">10</span><span class="sxs-lookup"><span data-stu-id="6141e-134">10</span></span>            | <span data-ttu-id="6141e-135">**dwmaxmbpersecthreeresolutionstemporalqualityscalablity**</span><span class="sxs-lookup"><span data-stu-id="6141e-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span></span> |
| <span data-ttu-id="6141e-136">11</span><span class="sxs-lookup"><span data-stu-id="6141e-136">11</span></span>            | <span data-ttu-id="6141e-137">**dwmaxmbpersecfourresolutionstemporalqualityscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span></span> |
| <span data-ttu-id="6141e-138">12</span><span class="sxs-lookup"><span data-stu-id="6141e-138">12</span></span>            | <span data-ttu-id="6141e-139">**dwmaxmbperseconeresolutionfullscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-139">**dwMaxMBperSecOneResolutionFullScalability**</span></span>              |
| <span data-ttu-id="6141e-140">13</span><span class="sxs-lookup"><span data-stu-id="6141e-140">13</span></span>            | <span data-ttu-id="6141e-141">**dwmaxmbpersectworesolutionsfullscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span></span>             |
| <span data-ttu-id="6141e-142">14</span><span class="sxs-lookup"><span data-stu-id="6141e-142">14</span></span>            | <span data-ttu-id="6141e-143">**dwmaxmbpersecthreeresolutionsfullscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span></span>           |
| <span data-ttu-id="6141e-144">15</span><span class="sxs-lookup"><span data-stu-id="6141e-144">15</span></span>            | <span data-ttu-id="6141e-145">**dwmaxmbpersecfourresolutionsfullscalability**</span><span class="sxs-lookup"><span data-stu-id="6141e-145">**dwMaxMBperSecFourResolutionsFullScalability**</span></span>            |



 

<span data-ttu-id="6141e-146">Dieses Attribut wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6141e-146">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6141e-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6141e-147">Requirements</span></span>



| <span data-ttu-id="6141e-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6141e-148">Requirement</span></span> | <span data-ttu-id="6141e-149">Wert</span><span class="sxs-lookup"><span data-stu-id="6141e-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6141e-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6141e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6141e-151">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6141e-151">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6141e-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6141e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6141e-153">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6141e-153">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6141e-154">Header</span><span class="sxs-lookup"><span data-stu-id="6141e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6141e-155"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6141e-155"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6141e-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6141e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6141e-157">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6141e-157">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6141e-158">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="6141e-158">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




