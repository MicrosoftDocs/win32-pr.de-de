---
description: Bei der Videoprozessor-MFT handelt es sich um eine Microsoft Media Foundation Transformation (MFT), die eine colorspace-Konvertierung, eine Videogröße, eine Deinterlacing, eine Frameraten Konvertierung, Drehung, Zuschneiden, räumliche linke und Rechte Ansicht zum Entpacken und Spiegelung ausführt.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: MFT des Video Prozessors (camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369254"
---
# <a name="video-processor-mft"></a><span data-ttu-id="83a00-103">MFT des Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="83a00-103">Video Processor MFT</span></span>

<span data-ttu-id="83a00-104">Bei der Videoprozessor-MFT handelt es sich um eine Microsoft Media Foundation Transformation (MFT), die eine colorspace-Konvertierung, eine Videogröße, eine Deinterlacing, eine Frameraten Konvertierung, Drehung, Zuschneiden, räumliche linke und Rechte Ansicht zum Entpacken und Spiegelung ausführt.</span><span class="sxs-lookup"><span data-stu-id="83a00-104">The video processor MFT is a Microsoft Media Foundation transform (MFT) that performs colorspace conversion, video resizing, deinterlacing, frame rate conversion, rotation, cropping, spatial left and right view unpacking, and mirroring.</span></span>

## <a name="clsid"></a><span data-ttu-id="83a00-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="83a00-105">CLSID</span></span>

<span data-ttu-id="83a00-106">CLSID \_ videoprocess ormft</span><span class="sxs-lookup"><span data-stu-id="83a00-106">CLSID\_VideoProcessorMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="83a00-107">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="83a00-107">Interfaces</span></span>

-   [<span data-ttu-id="83a00-108">**Imfrealtimecliumtex**</span><span class="sxs-lookup"><span data-stu-id="83a00-108">**IMFRealTimeClientEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [<span data-ttu-id="83a00-109">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="83a00-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="83a00-110">**IMF videoprocess Control**</span><span class="sxs-lookup"><span data-stu-id="83a00-110">**IMFVideoProcessorControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a><span data-ttu-id="83a00-111">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="83a00-111">Input Formats</span></span>

-   <span data-ttu-id="83a00-112">**MF-Format \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="83a00-112">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="83a00-113">**MF-Format ( \_ ayuv)**</span><span class="sxs-lookup"><span data-stu-id="83a00-113">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="83a00-114">**MF-Format \_ I420**</span><span class="sxs-lookup"><span data-stu-id="83a00-114">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="83a00-115">**MF-Format ( \_ IYUV)**</span><span class="sxs-lookup"><span data-stu-id="83a00-115">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="83a00-116">**MF-Format \_ NV11**</span><span class="sxs-lookup"><span data-stu-id="83a00-116">**MFVideoFormat\_NV11**</span></span>
-   <span data-ttu-id="83a00-117">**MF-Format \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="83a00-117">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="83a00-118">**MF-Format \_ RGB24**</span><span class="sxs-lookup"><span data-stu-id="83a00-118">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="83a00-119">**MF-Format \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="83a00-119">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="83a00-120">**MF-Format \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="83a00-120">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="83a00-121">**MF-Format \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="83a00-121">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="83a00-122">**MF-Format \_ RGB8**</span><span class="sxs-lookup"><span data-stu-id="83a00-122">**MFVideoFormat\_RGB8**</span></span>
-   <span data-ttu-id="83a00-123">**MF-Format ( \_ UYVY)**</span><span class="sxs-lookup"><span data-stu-id="83a00-123">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="83a00-124">**MF-Format \_ v410**</span><span class="sxs-lookup"><span data-stu-id="83a00-124">**MFVideoFormat\_v410**</span></span>
-   <span data-ttu-id="83a00-125">**MF-Format \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="83a00-125">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="83a00-126">**MF-Format \_ im y41p**</span><span class="sxs-lookup"><span data-stu-id="83a00-126">**MFVideoFormat\_Y41P**</span></span>
-   <span data-ttu-id="83a00-127">**MF-Format \_ Y41T**</span><span class="sxs-lookup"><span data-stu-id="83a00-127">**MFVideoFormat\_Y41T**</span></span>
-   <span data-ttu-id="83a00-128">**MF-Format \_ Y42T**</span><span class="sxs-lookup"><span data-stu-id="83a00-128">**MFVideoFormat\_Y42T**</span></span>
-   <span data-ttu-id="83a00-129">**MF-Format \_ im YUY2**</span><span class="sxs-lookup"><span data-stu-id="83a00-129">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="83a00-130">**MF-Format \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="83a00-130">**MFVideoFormat\_YV12**</span></span>
-   <span data-ttu-id="83a00-131">**Mfvideoformat \_ yvyu**</span><span class="sxs-lookup"><span data-stu-id="83a00-131">**MFVideoFormat\_YVYU**</span></span>

## <a name="output-formats"></a><span data-ttu-id="83a00-132">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="83a00-132">Output Formats</span></span>

-   <span data-ttu-id="83a00-133">**MF-Format \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="83a00-133">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="83a00-134">**MF-Format ( \_ ayuv)**</span><span class="sxs-lookup"><span data-stu-id="83a00-134">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="83a00-135">**MF-Format \_ I420**</span><span class="sxs-lookup"><span data-stu-id="83a00-135">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="83a00-136">**MF-Format ( \_ IYUV)**</span><span class="sxs-lookup"><span data-stu-id="83a00-136">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="83a00-137">**MF-Format \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="83a00-137">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="83a00-138">**MF-Format \_ RGB24**</span><span class="sxs-lookup"><span data-stu-id="83a00-138">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="83a00-139">**MF-Format \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="83a00-139">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="83a00-140">**MF-Format \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="83a00-140">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="83a00-141">**MF-Format \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="83a00-141">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="83a00-142">**MF-Format ( \_ UYVY)**</span><span class="sxs-lookup"><span data-stu-id="83a00-142">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="83a00-143">**MF-Format \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="83a00-143">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="83a00-144">**MF-Format \_ im YUY2**</span><span class="sxs-lookup"><span data-stu-id="83a00-144">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="83a00-145">**MF-Format \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="83a00-145">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="83a00-146">Nicht jede Kombination aus Eingabe-und Ausgabeformaten wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83a00-146">Not every combination of input and output formats is supported.</span></span> <span data-ttu-id="83a00-147">Um zu testen, ob eine Konvertierung unterstützt wird, legen Sie den Eingabetyp fest, und klicken Sie dann auf [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="83a00-147">To test whether a conversion is supported, set the input type and then call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span>

<span data-ttu-id="83a00-148">Weitere Informationen zu diesen Formaten finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="83a00-148">For more information about these formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="83a00-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83a00-149">Remarks</span></span>

<span data-ttu-id="83a00-150">Eine Instanz des Video Prozessors kann auf eine der folgenden Arten erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="83a00-150">An instance of the video processor can be created in one of the following ways:</span></span>

-   <span data-ttu-id="83a00-151">Durch Aufrufen von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="83a00-151">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="83a00-152">Der Videoprozessor ist unter der Kategorie " **MFT \_ Category \_ Video \_ Processor** " registriert.</span><span class="sxs-lookup"><span data-stu-id="83a00-152">The video processor is registered under the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category.</span></span>
-   <span data-ttu-id="83a00-153">Durch Aufrufen der com-Funktion **CoCreateInstance** , die der CLSID- **CLSID \_ videoprocess ormft** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="83a00-153">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_VideoProcessorMFT**.</span></span>

<span data-ttu-id="83a00-154">Die folgenden Hinweise beziehen sich auf die Arbeit mit Quell Rechtecke und Ziel Rechtecke im **Video Prozessor-MFT**.</span><span class="sxs-lookup"><span data-stu-id="83a00-154">The following remarks pertain to working with source rectangles and destination rectangles in the **Video Processor MFT**.</span></span> <span data-ttu-id="83a00-155">Quell-und Ziel Rechtecke werden mit [**IMF videoprocess orcontrol:: setdestinationrechteck**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) und [**setsourcerectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) und mehrmals mit [**IMF mediaengineex:: updatevideostream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="83a00-155">Source and destination rectangles are set with [**IMFVideoProcessorControl::SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) and [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) and some times with [**IMFMediaEngineEx::UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span></span>

-   <span data-ttu-id="83a00-156">Das Quell Rechteck sollte ausgerichtet und gerundet werden, um die Anforderungen des Farb Formats des Frame Abbilds zu erfüllen, der für den Videoprozessor eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="83a00-156">The source rectangle should be aligned and rounded to match the requirements of the color format of the frame inputted to the video processor.</span></span> <span data-ttu-id="83a00-157">Dies ist wichtig, da Formate wie 420 und 422 Anforderungen an die Dimensionen und Offsets haben, die erstellt werden können und auf die zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="83a00-157">This is important because formats like 420 and 422 have requirements about the dimensions and offsets that can be created and accessed.</span></span> <span data-ttu-id="83a00-158">Ein Quell Rechteck von {1, 0, 319, 240} (Links, oben, rechts, unten) wird z. b. auf {2, 0, 320, 240} gerundet, wenn das Eingabeformat auf 420 fest steht.</span><span class="sxs-lookup"><span data-stu-id="83a00-158">For example, a source rectangle of {1, 0, 319, 240} (left, top, right, bottom) will be rounded to {2, 0, 320, 240} when the input format is 420.</span></span>
-   <span data-ttu-id="83a00-159">Sowohl das Ziel-als auch das Quell Rechteck werden immer an die entsprechenden Frames gebunden – das Quell Rechteck zum Quellframe und das Ziel Rechteck zum Zielframe.</span><span class="sxs-lookup"><span data-stu-id="83a00-159">Both the destination and source rectangle will always be clamped to fit inside their respective frames—the source rectangle to the source frame and the destination rectangle to the destination frame.</span></span> <span data-ttu-id="83a00-160">Dies bedeutet, dass negative Werte nicht aussagekräftig sind – Sie werden immer an 0 gebunden.</span><span class="sxs-lookup"><span data-stu-id="83a00-160">This means that negative values are not meaningful—they will be always clamped to 0.</span></span>
-   <span data-ttu-id="83a00-161">Das Quell Rechteck befindet sich im Koordinatensystem des Zielframes abzüglich aller Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="83a00-161">The source rectangle is in the destination frame's coordinate system, minus any destination rectangle.</span></span> <span data-ttu-id="83a00-162">Dies bedeutet, dass Transformationen wie die Drehung im Quell Rechteck "Rückgängig" sind.</span><span class="sxs-lookup"><span data-stu-id="83a00-162">This means that transformations like rotation are "undone" on the source rectangle.</span></span> <span data-ttu-id="83a00-163">Daher müssen Sie nicht wissen, ob das Video gedreht oder 3D entpackt wurde.</span><span class="sxs-lookup"><span data-stu-id="83a00-163">Therefore, you do not need to know if the video was rotated or 3D unpacked.</span></span> <span data-ttu-id="83a00-164">Sie könnten z. b. ein Rechteck oberhalb des videotags zeichnen, die relativen Koordinaten (relativ zum videotag) verwenden, diese normalisieren (Bereich zwischen 0 und 1) und Sie als Quell Rechteck weitergeben, und Sie sollten erwartungsgemäß funktionieren, auch wenn das Video gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="83a00-164">For example, you could draw a rectangle on top of the video tag, take the relative coordinates (relative to the video tag), normalize them (range 0 to 1) and pass them down as the source rectangle and they should work as expected, even if the video is being rotated.</span></span>

<span data-ttu-id="83a00-165">Der Videoprozessor unterstützt eine GPU-beschleunigte Videoverarbeitung mit Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="83a00-165">The video processor supports GPU-accelerated video processing, using Microsoft Direct3D 11.</span></span> <span data-ttu-id="83a00-166">Weitere Informationen finden Sie unter [MF \_ sa \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md).</span><span class="sxs-lookup"><span data-stu-id="83a00-166">For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).</span></span>

### <a name="stereoscopic-video"></a><span data-ttu-id="83a00-167">Stereoskopisches Video</span><span class="sxs-lookup"><span data-stu-id="83a00-167">Stereoscopic Video</span></span>

<span data-ttu-id="83a00-168">Der Videoprozessor unterstützt den Vorgang zum Entpacken der Ansicht auf 3D-Video Frames:</span><span class="sxs-lookup"><span data-stu-id="83a00-168">The video processor supports the view unpacking operation on 3D video frames:</span></span>

<span data-ttu-id="83a00-169">Wenn der Eingabe Rahmen zwei Ansichten enthält, die im gleichen Frame verpackt sind, kann der Videoprozessor die Ansichten in separate Puffer aufteilen oder die Basis Ansicht extrahieren und die zweite Ansicht verwerfen.</span><span class="sxs-lookup"><span data-stu-id="83a00-169">If the input frame contains two views packed in the same frame, the video processor can split the views into separate buffers, or extract the base view and discard the second view.</span></span> <span data-ttu-id="83a00-170">Um das Entpacken von Ansichten zu aktivieren, legen Sie das [MF-Attribut " \_ \_ 3dvideo- \_ Ausgabe aktivieren](mf-enable-3dvideo-output.md) " auf **MF3DVideoOutputType \_ Stereo** oder **MF3DVideoOutputType \_ baseview** fest.</span><span class="sxs-lookup"><span data-stu-id="83a00-170">To enable view unpacking, set the [MF\_ENABLE\_3DVIDEO\_OUTPUT](mf-enable-3dvideo-output.md) attribute to **MF3DVideoOutputType\_Stereo** or **MF3DVideoOutputType\_BaseView**.</span></span>

## <a name="requirements"></a><span data-ttu-id="83a00-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83a00-171">Requirements</span></span>



| <span data-ttu-id="83a00-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83a00-172">Requirement</span></span> | <span data-ttu-id="83a00-173">Wert</span><span class="sxs-lookup"><span data-stu-id="83a00-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a00-174">Header</span><span class="sxs-lookup"><span data-stu-id="83a00-174">Header</span></span><br/> | <dl> <span data-ttu-id="83a00-175"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="83a00-175"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83a00-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83a00-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a00-177">Digitale Signal Prozessoren</span><span class="sxs-lookup"><span data-stu-id="83a00-177">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




