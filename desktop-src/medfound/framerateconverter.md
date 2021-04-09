---
description: Ändert die Framerate eines Videodaten Stroms.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Frame Rate Konverter DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749232"
---
# <a name="frame-rate-converter-dsp"></a><span data-ttu-id="af18a-103">Frame Rate Konverter DSP</span><span class="sxs-lookup"><span data-stu-id="af18a-103">Frame Rate Converter DSP</span></span>

<span data-ttu-id="af18a-104">Ändert die Framerate eines Videodaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="af18a-104">Changes the frame rate of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="af18a-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="af18a-105">CLSID</span></span>

<span data-ttu-id="af18a-106">CLSID \_ cframerateconvertdmo</span><span class="sxs-lookup"><span data-stu-id="af18a-106">CLSID\_CFrameRateConvertDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="af18a-107">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="af18a-107">Interfaces</span></span>

-   <span data-ttu-id="af18a-108">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="af18a-108">**IMediaObject**</span></span>
-   <span data-ttu-id="af18a-109">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="af18a-109">**IMFTransform**</span></span>
-   <span data-ttu-id="af18a-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="af18a-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="af18a-111">Formate</span><span class="sxs-lookup"><span data-stu-id="af18a-111">Formats</span></span>

-   <span data-ttu-id="af18a-112">ARGB 32</span><span class="sxs-lookup"><span data-stu-id="af18a-112">ARGB 32</span></span>
-   <span data-ttu-id="af18a-113">RGB 24</span><span class="sxs-lookup"><span data-stu-id="af18a-113">RGB 24</span></span>
-   <span data-ttu-id="af18a-114">RGB 32</span><span class="sxs-lookup"><span data-stu-id="af18a-114">RGB 32</span></span>
-   <span data-ttu-id="af18a-115">RGB 555</span><span class="sxs-lookup"><span data-stu-id="af18a-115">RGB 555</span></span>
-   <span data-ttu-id="af18a-116">RGB 565</span><span class="sxs-lookup"><span data-stu-id="af18a-116">RGB 565</span></span>
-   <span data-ttu-id="af18a-117">Ayuv</span><span class="sxs-lookup"><span data-stu-id="af18a-117">AYUV</span></span>
-   <span data-ttu-id="af18a-118">IYUV</span><span class="sxs-lookup"><span data-stu-id="af18a-118">IYUV</span></span>
-   <span data-ttu-id="af18a-119">UYVY</span><span class="sxs-lookup"><span data-stu-id="af18a-119">UYVY</span></span>
-   <span data-ttu-id="af18a-120">Y211</span><span class="sxs-lookup"><span data-stu-id="af18a-120">Y211</span></span>
-   <span data-ttu-id="af18a-121">Y411</span><span class="sxs-lookup"><span data-stu-id="af18a-121">Y411</span></span>
-   <span data-ttu-id="af18a-122">Im y41p</span><span class="sxs-lookup"><span data-stu-id="af18a-122">Y41P</span></span>
-   <span data-ttu-id="af18a-123">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="af18a-123">YUY2</span></span>
-   <span data-ttu-id="af18a-124">Yuyv</span><span class="sxs-lookup"><span data-stu-id="af18a-124">YUYV</span></span>
-   <span data-ttu-id="af18a-125">YV12</span><span class="sxs-lookup"><span data-stu-id="af18a-125">YV12</span></span>
-   <span data-ttu-id="af18a-126">Im yvyu</span><span class="sxs-lookup"><span data-stu-id="af18a-126">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="af18a-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af18a-127">Properties</span></span>

-   [<span data-ttu-id="af18a-128">mfpkey, \_ \_ inputframerate</span><span class="sxs-lookup"><span data-stu-id="af18a-128">MFPKEY\_CONV\_INPUTFRAMERATE</span></span>](mfpkey-conv-inputframerate.md)
-   [<span data-ttu-id="af18a-129">mfpkey-" \_ \_ outputframerate"</span><span class="sxs-lookup"><span data-stu-id="af18a-129">MFPKEY\_CONV\_OUTPUTFRAMERATE</span></span>](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a><span data-ttu-id="af18a-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af18a-130">Remarks</span></span>

<span data-ttu-id="af18a-131">Dieser DSP ändert die Framerate, indem Frames wiederholt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="af18a-131">This DSP changes the frame rate by repeating or dropping frames.</span></span>

<span data-ttu-id="af18a-132">Standardmäßig ruft der DSP die Frameraten aus den Medientypen ab.</span><span class="sxs-lookup"><span data-stu-id="af18a-132">By default, the DSP gets the frame rates from the media types.</span></span> <span data-ttu-id="af18a-133">Optional können Sie die Frameraten angeben, indem Sie die Eigenschaften "mfpkey", " \_ \_ inputframerate" und "mfpkey" für " \_ \_ outputframerate" festlegen.</span><span class="sxs-lookup"><span data-stu-id="af18a-133">Optionally, you can specify the frame rates by setting the MFPKEY\_CONV\_INPUTFRAMERATE and MFPKEY\_CONV\_OUTPUTFRAMERATE properties.</span></span> <span data-ttu-id="af18a-134">Diese Werte überschreiben die im Medientyp angegebene Framerate.</span><span class="sxs-lookup"><span data-stu-id="af18a-134">These values override the frame rate given in the media type.</span></span> <span data-ttu-id="af18a-135">Wenn Sie diesen DSP jedoch innerhalb der Media Foundation Pipeline verwenden, sollten Sie diese Eigenschaften nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="af18a-135">However, if you are using this DSP within the Media Foundation pipeline, you should not set these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="af18a-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af18a-136">Requirements</span></span>



| <span data-ttu-id="af18a-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af18a-137">Requirement</span></span> | <span data-ttu-id="af18a-138">Wert</span><span class="sxs-lookup"><span data-stu-id="af18a-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af18a-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af18a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="af18a-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af18a-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="af18a-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af18a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="af18a-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af18a-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af18a-143">Header</span><span class="sxs-lookup"><span data-stu-id="af18a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="af18a-144"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af18a-144"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="af18a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="af18a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af18a-146"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af18a-146"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af18a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af18a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af18a-148">Digitale Signal Prozessoren</span><span class="sxs-lookup"><span data-stu-id="af18a-148">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




