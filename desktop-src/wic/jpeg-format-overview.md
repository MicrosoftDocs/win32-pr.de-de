---
description: Dieses Thema enthält Informationen zum nativen JPEG-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Übersicht über das JPEG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444191"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="a1f6f-103">Übersicht über das JPEG-Format</span><span class="sxs-lookup"><span data-stu-id="a1f6f-103">JPEG Format Overview</span></span>

<span data-ttu-id="a1f6f-104">Dieses Thema enthält Informationen zum nativen JPEG-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="a1f6f-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="a1f6f-105">Codec Identity</span></span>

<span data-ttu-id="a1f6f-106">Die folgende Tabelle enthält Informationen zur Codecidentifikation.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="a1f6f-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="a1f6f-107">Component</span></span>            | <span data-ttu-id="a1f6f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1f6f-108">Description</span></span>                             |
|------------------------|-----------------------------------------|
| <span data-ttu-id="a1f6f-109">Formale Namen</span><span class="sxs-lookup"><span data-stu-id="a1f6f-109">Formal Name(s)</span></span>         | <span data-ttu-id="a1f6f-110">JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-110">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="a1f6f-111">Dateinamenerweiterungen</span><span class="sxs-lookup"><span data-stu-id="a1f6f-111">File Name Extension(s)</span></span> | <span data-ttu-id="a1f6f-112">jpe, jpeg, jpg</span><span class="sxs-lookup"><span data-stu-id="a1f6f-112">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="a1f6f-113">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-113">MIME type</span></span>              | <span data-ttu-id="a1f6f-114">image/jpeg, image/jpe, image/jpg</span><span class="sxs-lookup"><span data-stu-id="a1f6f-114">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="a1f6f-115">Spezifikationsunterstützung</span><span class="sxs-lookup"><span data-stu-id="a1f6f-115">Specification Support</span></span>  | <span data-ttu-id="a1f6f-116">JFIF-Spezifikation 1.02</span><span class="sxs-lookup"><span data-stu-id="a1f6f-116">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="a1f6f-117">In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen JPEG-Codeckomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-117">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="a1f6f-118">Komponente</span><span class="sxs-lookup"><span data-stu-id="a1f6f-118">Component</span></span>        | <span data-ttu-id="a1f6f-119">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="a1f6f-119">Friendly Name</span></span>             | <span data-ttu-id="a1f6f-120">GUID</span><span class="sxs-lookup"><span data-stu-id="a1f6f-120">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="a1f6f-121">Containerformat</span><span class="sxs-lookup"><span data-stu-id="a1f6f-121">Container Format</span></span> | <span data-ttu-id="a1f6f-122">GUID \_ ContainerFormatJpeg</span><span class="sxs-lookup"><span data-stu-id="a1f6f-122">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="a1f6f-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="a1f6f-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="a1f6f-124">Decoder</span><span class="sxs-lookup"><span data-stu-id="a1f6f-124">Decoder</span></span>          | <span data-ttu-id="a1f6f-125">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="a1f6f-125">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="a1f6f-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="a1f6f-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="a1f6f-127">Encoder</span><span class="sxs-lookup"><span data-stu-id="a1f6f-127">Encoder</span></span>          | <span data-ttu-id="a1f6f-128">CLSID \_ WICJpegEncoder</span><span class="sxs-lookup"><span data-stu-id="a1f6f-128">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="a1f6f-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="a1f6f-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="a1f6f-130">Codierung</span><span class="sxs-lookup"><span data-stu-id="a1f6f-130">Encoding</span></span>

<span data-ttu-id="a1f6f-131">Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a1f6f-132">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="a1f6f-133">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="a1f6f-133">Encoder Options</span></span>

<span data-ttu-id="a1f6f-134">WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="a1f6f-135">Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="a1f6f-136">Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (obwohl sie nicht unbedingt unterstützt werden) oder codecspezifische Optionen, die vom Bildformatcodec entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="a1f6f-137">Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a1f6f-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="a1f6f-138">Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="a1f6f-139">Der JPEG-Codec verwendet grundlegende WIC-Optionen.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-139">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="a1f6f-140">In der folgenden Tabelle sind die WIC-Encoderoptionen aufgeführt, die vom nativen JPEG-Codec unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-140">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="a1f6f-141">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="a1f6f-141">Property Name</span></span>                                        | <span data-ttu-id="a1f6f-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a1f6f-142">VARTYPE</span></span>           | <span data-ttu-id="a1f6f-143">Wertbereich</span><span class="sxs-lookup"><span data-stu-id="a1f6f-143">Value Range</span></span>                                                                       | <span data-ttu-id="a1f6f-144">Standardwert</span><span class="sxs-lookup"><span data-stu-id="a1f6f-144">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="a1f6f-145">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="a1f6f-145">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="a1f6f-146">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="a1f6f-146">VT\_R4</span></span>            | <span data-ttu-id="a1f6f-147">0 - 1.0</span><span class="sxs-lookup"><span data-stu-id="a1f6f-147">0 - 1.0</span></span>                                                                           | <span data-ttu-id="a1f6f-148">0.9</span><span class="sxs-lookup"><span data-stu-id="a1f6f-148">0.9</span></span>                                                                            |
| [<span data-ttu-id="a1f6f-149">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="a1f6f-149">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="a1f6f-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="a1f6f-150">VT\_UI1</span></span>           | [<span data-ttu-id="a1f6f-151">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="a1f6f-151">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="a1f6f-152">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="a1f6f-152">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="a1f6f-153">Sättigung</span><span class="sxs-lookup"><span data-stu-id="a1f6f-153">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="a1f6f-154">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="a1f6f-154">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="a1f6f-155">64 Einträge (DCT)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-155">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="a1f6f-156">Standard-Leuchtdichtetabelle.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-156">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="a1f6f-157">Chrominance</span><span class="sxs-lookup"><span data-stu-id="a1f6f-157">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="a1f6f-158">VT \_ UI4/VT \_ ARRAY</span><span class="sxs-lookup"><span data-stu-id="a1f6f-158">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="a1f6f-159">64 Einträge (DCT)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-159">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="a1f6f-160">Standard-Chromeinancetabelle.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-160">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="a1f6f-161">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="a1f6f-161">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="a1f6f-162">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="a1f6f-162">VT\_UI1</span></span>           | [<span data-ttu-id="a1f6f-163">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="a1f6f-163">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="a1f6f-164">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="a1f6f-164">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="a1f6f-165">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="a1f6f-165">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="a1f6f-166">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="a1f6f-166">VT\_BOOL</span></span>          | <span data-ttu-id="a1f6f-167">**TRUE** / **FALSE**</span><span class="sxs-lookup"><span data-stu-id="a1f6f-167">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="a1f6f-168">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a1f6f-168">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="a1f6f-169">Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-169">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="a1f6f-170">ImageQuality-Option</span><span class="sxs-lookup"><span data-stu-id="a1f6f-170">ImageQuality Option</span></span>

<span data-ttu-id="a1f6f-171">Gibt die gewünschte Bildgenauigkeit an.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-171">Specifies the desired image fidelity.</span></span> <span data-ttu-id="a1f6f-172">0,0 gibt die niedrigste mögliche Genauigkeit und 1,0 die höchste Genauigkeit an.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-172">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="a1f6f-173">Der Standardwert ist 0,9.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-173">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="a1f6f-174">BitmapTransform-Option</span><span class="sxs-lookup"><span data-stu-id="a1f6f-174">BitmapTransform Option</span></span>

<span data-ttu-id="a1f6f-175">Gibt an, wie das Bild während der Bilddecodierung transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-175">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="a1f6f-176">Diese Option muss auf einen der [**WICBitmapTransformOptions-Enumerationswerte**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-176">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="a1f6f-177">Der Standardwert ist [**WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-177">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="a1f6f-178">Luminance-Option</span><span class="sxs-lookup"><span data-stu-id="a1f6f-178">Luminance Option</span></span>

<span data-ttu-id="a1f6f-179">Gibt die Graustufen-Helligkeitsebenentabelle an, die für die Codierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-179">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="a1f6f-180">Chromeinance-Option</span><span class="sxs-lookup"><span data-stu-id="a1f6f-180">Chrominance Option</span></span>

<span data-ttu-id="a1f6f-181">Gibt die Chromeinancetabelle an, die für die Codierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-181">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="a1f6f-182">JpegYCrCbSubsampling-Option</span><span class="sxs-lookup"><span data-stu-id="a1f6f-182">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="a1f6f-183">Gibt das Untersamplingverhältnis an, das für die YCrCb-Codierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-183">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="a1f6f-184">Der Standardwert ist [**WICJpegYCrCbSubsampling420.**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-184">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="a1f6f-185">SuppressApp0-Option</span><span class="sxs-lookup"><span data-stu-id="a1f6f-185">SuppressApp0 Option</span></span>

<span data-ttu-id="a1f6f-186">Gibt an, ob das Schreiben von App0-Metadaten beim Codieren der Bilddaten unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-186">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="a1f6f-187">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-187">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="a1f6f-188">Decodierung</span><span class="sxs-lookup"><span data-stu-id="a1f6f-188">Decoding</span></span>

<span data-ttu-id="a1f6f-189">Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-189">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="a1f6f-190">Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-190">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="a1f6f-191">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-191">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="a1f6f-192">Der native JPEG-Codec unterstützt auch [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) bei der Framedecodierung und fügt freigeschaltete Optionen zum Decodieren eines Bilddatenstroms hinzu.</span><span class="sxs-lookup"><span data-stu-id="a1f6f-192">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="a1f6f-193">Weitere Informationen zu diesen erweiterten Optionen finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="a1f6f-193">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
