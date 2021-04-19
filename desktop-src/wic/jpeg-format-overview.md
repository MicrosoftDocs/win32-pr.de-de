---
description: Dieses Thema enthält Informationen über den nativen JPEG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Übersicht über JPEG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349868"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="e7958-103">Übersicht über JPEG-Format</span><span class="sxs-lookup"><span data-stu-id="e7958-103">JPEG Format Overview</span></span>

<span data-ttu-id="e7958-104">Dieses Thema enthält Informationen über den nativen JPEG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e7958-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="e7958-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="e7958-105">Codec Identity</span></span>

<span data-ttu-id="e7958-106">In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e7958-106">The following table provides codec identification information.</span></span>



|                        |                                         |
|------------------------|-----------------------------------------|
| <span data-ttu-id="e7958-107">Formaler Name (n)</span><span class="sxs-lookup"><span data-stu-id="e7958-107">Formal Name(s)</span></span>         | <span data-ttu-id="e7958-108">JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="e7958-108">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="e7958-109">Dateinamenerweiterung (en)</span><span class="sxs-lookup"><span data-stu-id="e7958-109">File Name Extension(s)</span></span> | <span data-ttu-id="e7958-110">jpe, JPEG, JPG</span><span class="sxs-lookup"><span data-stu-id="e7958-110">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="e7958-111">MIME-Typ (MIME type)</span><span class="sxs-lookup"><span data-stu-id="e7958-111">MIME type</span></span>              | <span data-ttu-id="e7958-112">Image/JPEG, Image/jpe, Image/JPG</span><span class="sxs-lookup"><span data-stu-id="e7958-112">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="e7958-113">Spezifikations Unterstützung</span><span class="sxs-lookup"><span data-stu-id="e7958-113">Specification Support</span></span>  | <span data-ttu-id="e7958-114">JFIF-Spezifikation 1,02</span><span class="sxs-lookup"><span data-stu-id="e7958-114">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="e7958-115">In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen JPEG-Codec-Komponenten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e7958-115">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="e7958-116">Komponente</span><span class="sxs-lookup"><span data-stu-id="e7958-116">Component</span></span>        | <span data-ttu-id="e7958-117">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="e7958-117">Friendly Name</span></span>             | <span data-ttu-id="e7958-118">GUID</span><span class="sxs-lookup"><span data-stu-id="e7958-118">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="e7958-119">Container Format</span><span class="sxs-lookup"><span data-stu-id="e7958-119">Container Format</span></span> | <span data-ttu-id="e7958-120">GUID \_ containerformatjpeg</span><span class="sxs-lookup"><span data-stu-id="e7958-120">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="e7958-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="e7958-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="e7958-122">Decoder</span><span class="sxs-lookup"><span data-stu-id="e7958-122">Decoder</span></span>          | <span data-ttu-id="e7958-123">CLSID \_ wicjpgdecoder</span><span class="sxs-lookup"><span data-stu-id="e7958-123">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="e7958-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="e7958-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="e7958-125">Encoder</span><span class="sxs-lookup"><span data-stu-id="e7958-125">Encoder</span></span>          | <span data-ttu-id="e7958-126">CLSID \_ wicjpeer-Coder</span><span class="sxs-lookup"><span data-stu-id="e7958-126">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="e7958-127">1a34f 5C1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="e7958-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="e7958-128">Codierung</span><span class="sxs-lookup"><span data-stu-id="e7958-128">Encoding</span></span>

<span data-ttu-id="e7958-129">Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="e7958-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e7958-130">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e7958-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="e7958-131">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="e7958-131">Encoder Options</span></span>

<span data-ttu-id="e7958-132">WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene.</span><span class="sxs-lookup"><span data-stu-id="e7958-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="e7958-133">Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="e7958-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="e7958-134">Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format</span><span class="sxs-lookup"><span data-stu-id="e7958-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="e7958-135">Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e7958-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="e7958-136">Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e7958-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="e7958-137">Der JPEG-Codec verwendet grundlegende WIC-Optionen.</span><span class="sxs-lookup"><span data-stu-id="e7958-137">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="e7958-138">In der folgenden Tabelle sind die vom systemeigenen JPEG-Codec unterstützten WIC-Encoder-Optionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7958-138">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="e7958-139">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="e7958-139">Property Name</span></span>                                        | <span data-ttu-id="e7958-140">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e7958-140">VARTYPE</span></span>           | <span data-ttu-id="e7958-141">Wertbereich</span><span class="sxs-lookup"><span data-stu-id="e7958-141">Value Range</span></span>                                                                       | <span data-ttu-id="e7958-142">Standardwert</span><span class="sxs-lookup"><span data-stu-id="e7958-142">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="e7958-143">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="e7958-143">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="e7958-144">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="e7958-144">VT\_R4</span></span>            | <span data-ttu-id="e7958-145">0-1,0</span><span class="sxs-lookup"><span data-stu-id="e7958-145">0 - 1.0</span></span>                                                                           | <span data-ttu-id="e7958-146">0.9</span><span class="sxs-lookup"><span data-stu-id="e7958-146">0.9</span></span>                                                                            |
| [<span data-ttu-id="e7958-147">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="e7958-147">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="e7958-148">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e7958-148">VT\_UI1</span></span>           | [<span data-ttu-id="e7958-149">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="e7958-149">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="e7958-150">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="e7958-150">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="e7958-151">Sättigung</span><span class="sxs-lookup"><span data-stu-id="e7958-151">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="e7958-152">VT \_ UI4/VT- \_ Array</span><span class="sxs-lookup"><span data-stu-id="e7958-152">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="e7958-153">64 Einträge (DCT)</span><span class="sxs-lookup"><span data-stu-id="e7958-153">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="e7958-154">Standardmäßige Leuchtkraft Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e7958-154">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="e7958-155">Chrominance</span><span class="sxs-lookup"><span data-stu-id="e7958-155">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="e7958-156">VT \_ UI4/VT- \_ Array</span><span class="sxs-lookup"><span data-stu-id="e7958-156">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="e7958-157">64 Einträge (DCT)</span><span class="sxs-lookup"><span data-stu-id="e7958-157">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="e7958-158">Standardmäßige Chrominanz-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e7958-158">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="e7958-159">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="e7958-159">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="e7958-160">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e7958-160">VT\_UI1</span></span>           | [<span data-ttu-id="e7958-161">**Wicjppfgycrcbsubsamplingoption**</span><span class="sxs-lookup"><span data-stu-id="e7958-161">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="e7958-162">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="e7958-162">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="e7958-163">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="e7958-163">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="e7958-164">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="e7958-164">VT\_BOOL</span></span>          | <span data-ttu-id="e7958-165">**True** / **False**</span><span class="sxs-lookup"><span data-stu-id="e7958-165">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="e7958-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="e7958-166">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="e7958-167">Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e7958-167">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="e7958-168">ImageQuality-Option</span><span class="sxs-lookup"><span data-stu-id="e7958-168">ImageQuality Option</span></span>

<span data-ttu-id="e7958-169">Gibt die gewünschte Bild Treue an.</span><span class="sxs-lookup"><span data-stu-id="e7958-169">Specifies the desired image fidelity.</span></span> <span data-ttu-id="e7958-170">0,0 gibt die niedrigste mögliche Treue an, und 1,0 gibt die höchste Genauigkeit an.</span><span class="sxs-lookup"><span data-stu-id="e7958-170">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="e7958-171">Der Standardwert ist 0,9.</span><span class="sxs-lookup"><span data-stu-id="e7958-171">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="e7958-172">BitmapTransform (Option)</span><span class="sxs-lookup"><span data-stu-id="e7958-172">BitmapTransform Option</span></span>

<span data-ttu-id="e7958-173">Gibt an, wie das Bild während der Decodierung von Bildern transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7958-173">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="e7958-174">Diese Option muss auf einen der [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) -Enumerationswerte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e7958-174">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="e7958-175">Der Standardwert ist [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span><span class="sxs-lookup"><span data-stu-id="e7958-175">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="e7958-176">Option "Leuchtkraft"</span><span class="sxs-lookup"><span data-stu-id="e7958-176">Luminance Option</span></span>

<span data-ttu-id="e7958-177">Gibt die für die Codierung zu verwendende Graustufen Helligkeit-Ebenen-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="e7958-177">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="e7958-178">Chrominance (Option)</span><span class="sxs-lookup"><span data-stu-id="e7958-178">Chrominance Option</span></span>

<span data-ttu-id="e7958-179">Gibt die für die Codierung zu verwendende Chrominanz-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="e7958-179">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="e7958-180">Jpgycrcbsubsampling (Option)</span><span class="sxs-lookup"><span data-stu-id="e7958-180">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="e7958-181">Gibt das unter Stichproben Verhältnis an, das für die YCrCb-Codierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7958-181">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="e7958-182">Der Standardwert ist [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="e7958-182">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="e7958-183">SuppressApp0-Option</span><span class="sxs-lookup"><span data-stu-id="e7958-183">SuppressApp0 Option</span></span>

<span data-ttu-id="e7958-184">Gibt an, ob das Schreiben von App0-Metadaten beim Codieren der Bilddaten unterdrückt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7958-184">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="e7958-185">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e7958-185">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="e7958-186">Decodierung</span><span class="sxs-lookup"><span data-stu-id="e7958-186">Decoding</span></span>

<span data-ttu-id="e7958-187">Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="e7958-187">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e7958-188">Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="e7958-188">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="e7958-189">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="e7958-189">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="e7958-190">Der Native JPEG-Codec unterstützt auch [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) bei Frame-Decodierung das Hinzufügen von bereitgestellten Optionen für das Decodieren eines bildstreams.</span><span class="sxs-lookup"><span data-stu-id="e7958-190">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="e7958-191">Weitere Informationen zu diesen erweiterten Optionen finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="e7958-191">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
