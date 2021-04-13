---
description: Konvertiert einen Videostream zwischen Farbformaten.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Farb Konverter DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484107"
---
# <a name="color-converter-dsp"></a><span data-ttu-id="24813-103">Farb Konverter-DSP</span><span class="sxs-lookup"><span data-stu-id="24813-103">Color Converter DSP</span></span>

<span data-ttu-id="24813-104">Konvertiert einen Videostream zwischen Farbformaten.</span><span class="sxs-lookup"><span data-stu-id="24813-104">Converts a video stream between color formats.</span></span>

## <a name="clsid"></a><span data-ttu-id="24813-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="24813-105">CLSID</span></span>

<span data-ttu-id="24813-106">CLSID \_ ccolorconvertdmo</span><span class="sxs-lookup"><span data-stu-id="24813-106">CLSID\_CColorConvertDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="24813-107">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="24813-107">Interfaces</span></span>

-   [<span data-ttu-id="24813-108">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="24813-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="24813-109">**Imfrealtimeclient**</span><span class="sxs-lookup"><span data-stu-id="24813-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="24813-110">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="24813-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="24813-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="24813-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="24813-112">Iwmcolor-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24813-112">IWMColorConvProps</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a><span data-ttu-id="24813-113">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="24813-113">Input Formats</span></span>

-   <span data-ttu-id="24813-114">RGB 24</span><span class="sxs-lookup"><span data-stu-id="24813-114">RGB 24</span></span>
-   <span data-ttu-id="24813-115">RGB 32</span><span class="sxs-lookup"><span data-stu-id="24813-115">RGB 32</span></span>
-   <span data-ttu-id="24813-116">RGB 555</span><span class="sxs-lookup"><span data-stu-id="24813-116">RGB 555</span></span>
-   <span data-ttu-id="24813-117">RGB 565</span><span class="sxs-lookup"><span data-stu-id="24813-117">RGB 565</span></span>
-   <span data-ttu-id="24813-118">RGB 8</span><span class="sxs-lookup"><span data-stu-id="24813-118">RGB 8</span></span>
-   <span data-ttu-id="24813-119">Ayuv</span><span class="sxs-lookup"><span data-stu-id="24813-119">AYUV</span></span>
-   <span data-ttu-id="24813-120">I420</span><span class="sxs-lookup"><span data-stu-id="24813-120">I420</span></span>
-   <span data-ttu-id="24813-121">IYUV</span><span class="sxs-lookup"><span data-stu-id="24813-121">IYUV</span></span>
-   <span data-ttu-id="24813-122">NV11</span><span class="sxs-lookup"><span data-stu-id="24813-122">NV11</span></span>
-   <span data-ttu-id="24813-123">NV12</span><span class="sxs-lookup"><span data-stu-id="24813-123">NV12</span></span>
-   <span data-ttu-id="24813-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="24813-124">UYVY</span></span>
-   <span data-ttu-id="24813-125">V216</span><span class="sxs-lookup"><span data-stu-id="24813-125">V216</span></span>
-   <span data-ttu-id="24813-126">V410</span><span class="sxs-lookup"><span data-stu-id="24813-126">V410</span></span>
-   <span data-ttu-id="24813-127">Im y41p</span><span class="sxs-lookup"><span data-stu-id="24813-127">Y41P</span></span>
-   <span data-ttu-id="24813-128">Y41T</span><span class="sxs-lookup"><span data-stu-id="24813-128">Y41T</span></span>
-   <span data-ttu-id="24813-129">Y42T</span><span class="sxs-lookup"><span data-stu-id="24813-129">Y42T</span></span>
-   <span data-ttu-id="24813-130">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="24813-130">YUY2</span></span>
-   <span data-ttu-id="24813-131">YV12</span><span class="sxs-lookup"><span data-stu-id="24813-131">YV12</span></span>
-   <span data-ttu-id="24813-132">YVU9</span><span class="sxs-lookup"><span data-stu-id="24813-132">YVU9</span></span>
-   <span data-ttu-id="24813-133">Im yvyu</span><span class="sxs-lookup"><span data-stu-id="24813-133">YVYU</span></span>

## <a name="output-formats"></a><span data-ttu-id="24813-134">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="24813-134">Output Formats</span></span>

-   <span data-ttu-id="24813-135">RGB 24</span><span class="sxs-lookup"><span data-stu-id="24813-135">RGB 24</span></span>
-   <span data-ttu-id="24813-136">RGB 32</span><span class="sxs-lookup"><span data-stu-id="24813-136">RGB 32</span></span>
-   <span data-ttu-id="24813-137">RGB 555</span><span class="sxs-lookup"><span data-stu-id="24813-137">RGB 555</span></span>
-   <span data-ttu-id="24813-138">RGB 565</span><span class="sxs-lookup"><span data-stu-id="24813-138">RGB 565</span></span>
-   <span data-ttu-id="24813-139">RGB 8</span><span class="sxs-lookup"><span data-stu-id="24813-139">RGB 8</span></span>
-   <span data-ttu-id="24813-140">Ayuv</span><span class="sxs-lookup"><span data-stu-id="24813-140">AYUV</span></span>
-   <span data-ttu-id="24813-141">I420</span><span class="sxs-lookup"><span data-stu-id="24813-141">I420</span></span>
-   <span data-ttu-id="24813-142">IYUV</span><span class="sxs-lookup"><span data-stu-id="24813-142">IYUV</span></span>
-   <span data-ttu-id="24813-143">NV11</span><span class="sxs-lookup"><span data-stu-id="24813-143">NV11</span></span>
-   <span data-ttu-id="24813-144">NV12</span><span class="sxs-lookup"><span data-stu-id="24813-144">NV12</span></span>
-   <span data-ttu-id="24813-145">UYVY</span><span class="sxs-lookup"><span data-stu-id="24813-145">UYVY</span></span>
-   <span data-ttu-id="24813-146">V216</span><span class="sxs-lookup"><span data-stu-id="24813-146">V216</span></span>
-   <span data-ttu-id="24813-147">V410</span><span class="sxs-lookup"><span data-stu-id="24813-147">V410</span></span>
-   <span data-ttu-id="24813-148">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="24813-148">YUY2</span></span>
-   <span data-ttu-id="24813-149">YV12</span><span class="sxs-lookup"><span data-stu-id="24813-149">YV12</span></span>
-   <span data-ttu-id="24813-150">Im yvyu</span><span class="sxs-lookup"><span data-stu-id="24813-150">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="24813-151">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24813-151">Properties</span></span>

-   [<span data-ttu-id="24813-152">mfpkey \_ Color-v \_ srcleft</span><span class="sxs-lookup"><span data-stu-id="24813-152">MFPKEY\_COLORCONV\_SRCLEFT</span></span>](mfpkey-colorconv-srcleft.md)
-   [<span data-ttu-id="24813-153">mfpkey \_ Color-v \_ srctop</span><span class="sxs-lookup"><span data-stu-id="24813-153">MFPKEY\_COLORCONV\_SRCTOP</span></span>](mfpkey-colorconv-srctop.md)
-   [<span data-ttu-id="24813-154">mfpkey \_ Color-v \_ dstleft</span><span class="sxs-lookup"><span data-stu-id="24813-154">MFPKEY\_COLORCONV\_DSTLEFT</span></span>](mfpkey-colorconv-dstleft.md)
-   [<span data-ttu-id="24813-155">mfpkey \_ Color-v \_ dsttop</span><span class="sxs-lookup"><span data-stu-id="24813-155">MFPKEY\_COLORCONV\_DSTTOP</span></span>](mfpkey-colorconv-dsttop.md)
-   [<span data-ttu-id="24813-156">Breite von mfpkey \_ Color-v \_</span><span class="sxs-lookup"><span data-stu-id="24813-156">MFPKEY\_COLORCONV\_WIDTH</span></span>](mfpkey-colorconv-width.md)
-   [<span data-ttu-id="24813-157">mfpkey \_ Color-v- \_ Höhe</span><span class="sxs-lookup"><span data-stu-id="24813-157">MFPKEY\_COLORCONV\_HEIGHT</span></span>](mfpkey-colorconv-height.md)
-   [<span data-ttu-id="24813-158">mfpkey \_ Color-v- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="24813-158">MFPKEY\_COLORCONV\_MODE</span></span>](mfpkey-colorconv-mode.md)

## <a name="remarks"></a><span data-ttu-id="24813-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24813-159">Remarks</span></span>

<span data-ttu-id="24813-160">Der Farb Konverter DSP ist als COM-Objekt implementiert, das als directxmedia-Objekt (DMO) oder Media Foundation Transformation (MFT) fungieren kann.</span><span class="sxs-lookup"><span data-stu-id="24813-160">The Color Converter DSP is implemented as a COM object that can act as a DirectXMedia Object (DMO) or a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="24813-161">Das-Objekt verfügt über einen einzelnen Klassen Bezeichner (CLSID), unabhängig davon, ob er als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="24813-161">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="24813-162">Informationen dazu, wann ein DSP als DMO oder MFT fungiert, finden Sie unter [digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="24813-162">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="24813-163">Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein DSP als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="24813-163">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="24813-164">Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein DSP als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="24813-164">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="24813-165">Informationen zu den GUIDs, die Medien Untertypen darstellen, finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="24813-165">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="24813-166">Standardmäßig kopiert dieser DSP das gesamte Quell Abbild in den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="24813-166">By default, this DSP copies the entire source image to the output buffer.</span></span> <span data-ttu-id="24813-167">Optional können Sie Quell-und Ziel Rechtecke angeben.</span><span class="sxs-lookup"><span data-stu-id="24813-167">Optionally, you can specify source and destination rectangles.</span></span> <span data-ttu-id="24813-168">Der DSP kopiert den Teil des Quell Bilds, der durch das Quell Rechteck definiert ist, und schreibt ihn in das Ziel Rechteck im Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="24813-168">The DSP copies the portion of the source image defined by source rectangle, and writes it into the destination rectangle on the output buffer.</span></span> <span data-ttu-id="24813-169">Der DSP führt keine Skalierung aus. die Quell-und Ziel Rechtecke müssen dieselbe Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="24813-169">The DSP does not perform any scaling; the source and destination rectangles must be the same size.</span></span> <span data-ttu-id="24813-170">Die Quell-und Ziel Rechtecke dürfen die Grenzen des Video Rahmens nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="24813-170">The source and destination rectangles cannot exceed the boundaries of the video frame.</span></span>

<span data-ttu-id="24813-171">Alle Eigenschaften außer dem [**mfpkey \_ Color-v- \_ Modus**](mfpkey-colorconv-mode.md) müssen in einer Gruppe festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="24813-171">All of the properties except [**MFPKEY\_COLORCONV\_MODE**](mfpkey-colorconv-mode.md) must be set in a group.</span></span> <span data-ttu-id="24813-172">Wenn Sie eine dieser Eigenschaften festlegen, müssen Sie alle anderen festlegen.</span><span class="sxs-lookup"><span data-stu-id="24813-172">If you set any of these properties, you must set all of the others.</span></span> <span data-ttu-id="24813-173">Andernfalls sind die Quell-und Ziel Rechtecke möglicherweise ungültig. in diesem Fall geben sowohl die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode als auch die [**imediaobject::P rocess Output**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) -Methode **E \_ invalidArg** zurück.</span><span class="sxs-lookup"><span data-stu-id="24813-173">Otherwise, the source and destination rectangles might be invalid, in which case both the [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) and [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) methods will return **E\_INVALIDARG**.</span></span>

<span data-ttu-id="24813-174">Der Farb Konverter unterstützt nicht jede Kombination aus Eingabeformat und Ausgabeformat.</span><span class="sxs-lookup"><span data-stu-id="24813-174">The color converter does not support every combination of input format and output format.</span></span> <span data-ttu-id="24813-175">Normalerweise sollten Sie das Medienformat festlegen, das Sie wissen, entweder Eingabe oder Ausgabe, und dann die verfügbaren Formate im umgekehrten Stream auflisten.</span><span class="sxs-lookup"><span data-stu-id="24813-175">Usually, you should set the media format that you know, either input or output, and then enumerate the available formats on the opposite stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="24813-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24813-176">Requirements</span></span>



| <span data-ttu-id="24813-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24813-177">Requirement</span></span> | <span data-ttu-id="24813-178">Wert</span><span class="sxs-lookup"><span data-stu-id="24813-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24813-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24813-179">Minimum supported client</span></span><br/> | <span data-ttu-id="24813-180">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24813-180">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="24813-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24813-181">Minimum supported server</span></span><br/> | <span data-ttu-id="24813-182">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24813-182">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24813-183">Header</span><span class="sxs-lookup"><span data-stu-id="24813-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="24813-184"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="24813-184"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="24813-185">DLL</span><span class="sxs-lookup"><span data-stu-id="24813-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24813-186"><dt>Colorcnv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24813-186"><dt>Colorcnv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24813-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24813-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24813-188">Digitale Signal Prozessoren</span><span class="sxs-lookup"><span data-stu-id="24813-188">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
