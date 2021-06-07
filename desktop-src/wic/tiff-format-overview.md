---
description: Dieses Thema enthält Informationen zum nativen TIFF-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Übersicht über das TIFF-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444421"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="59d61-103">Übersicht über das TIFF-Format</span><span class="sxs-lookup"><span data-stu-id="59d61-103">TIFF Format Overview</span></span>

<span data-ttu-id="59d61-104">Dieses Thema enthält Informationen zum nativen TIFF-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="59d61-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="59d61-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="59d61-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="59d61-106">Codieren</span><span class="sxs-lookup"><span data-stu-id="59d61-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="59d61-107">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="59d61-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="59d61-108">Decodierung</span><span class="sxs-lookup"><span data-stu-id="59d61-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="59d61-109">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="59d61-109">Codec Identity</span></span>

<span data-ttu-id="59d61-110">Die folgende Tabelle enthält Codec-Identifikationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="59d61-110">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="59d61-111">Komponente</span><span class="sxs-lookup"><span data-stu-id="59d61-111">Component</span></span>            |   <span data-ttu-id="59d61-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59d61-112">Description</span></span>                   |
|------------------------|---------------------------------|
| <span data-ttu-id="59d61-113">Formale Namen</span><span class="sxs-lookup"><span data-stu-id="59d61-113">Formal Name(s)</span></span>         | <span data-ttu-id="59d61-114">TIFF (Tagged Image File Format)</span><span class="sxs-lookup"><span data-stu-id="59d61-114">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="59d61-115">Dateinamenerweiterung(en)</span><span class="sxs-lookup"><span data-stu-id="59d61-115">File Name Extension(s)</span></span> | <span data-ttu-id="59d61-116">tiff, tif</span><span class="sxs-lookup"><span data-stu-id="59d61-116">tiff, tif</span></span>                       |
| <span data-ttu-id="59d61-117">MIME-Typen</span><span class="sxs-lookup"><span data-stu-id="59d61-117">MIME type(s)</span></span>           | <span data-ttu-id="59d61-118">image/tiff, image/tif</span><span class="sxs-lookup"><span data-stu-id="59d61-118">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="59d61-119">Spezifikationsunterstützung</span><span class="sxs-lookup"><span data-stu-id="59d61-119">Specification Support</span></span>  | <span data-ttu-id="59d61-120">TIFF-Spezifikation 6.0</span><span class="sxs-lookup"><span data-stu-id="59d61-120">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="59d61-121">In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen TIFF-Codeckomponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59d61-121">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="59d61-122">Komponente</span><span class="sxs-lookup"><span data-stu-id="59d61-122">Component</span></span>        | <span data-ttu-id="59d61-123">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="59d61-123">Friendly Name</span></span>             | <span data-ttu-id="59d61-124">GUID</span><span class="sxs-lookup"><span data-stu-id="59d61-124">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="59d61-125">Containerformat</span><span class="sxs-lookup"><span data-stu-id="59d61-125">Container Format</span></span> | <span data-ttu-id="59d61-126">GUID \_ ContainerFormatTiff</span><span class="sxs-lookup"><span data-stu-id="59d61-126">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="59d61-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="59d61-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="59d61-128">Decoder</span><span class="sxs-lookup"><span data-stu-id="59d61-128">Decoder</span></span>          | <span data-ttu-id="59d61-129">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="59d61-129">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="59d61-130">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="59d61-130">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="59d61-131">Encoder</span><span class="sxs-lookup"><span data-stu-id="59d61-131">Encoder</span></span>          | <span data-ttu-id="59d61-132">CLSID \_ WICTiffEncoder</span><span class="sxs-lookup"><span data-stu-id="59d61-132">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="59d61-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="59d61-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="59d61-134">Codierung</span><span class="sxs-lookup"><span data-stu-id="59d61-134">Encoding</span></span>

<span data-ttu-id="59d61-135">Die WIC-Codierungs-API ist codecunabhängig, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="59d61-135">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="59d61-136">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie unter Übersicht über [die Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="59d61-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="59d61-137">Encoderoptionen</span><span class="sxs-lookup"><span data-stu-id="59d61-137">Encoder Options</span></span>

<span data-ttu-id="59d61-138">WIC-fähige Codecs unterscheiden sich auf der Ebene der Codierungsoption.</span><span class="sxs-lookup"><span data-stu-id="59d61-138">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="59d61-139">Encoderoptionen spiegeln die Funktionen eines Bildencoder wider, und jeder native Codec unterstützt einen Satz dieser Encoderoptionen.</span><span class="sxs-lookup"><span data-stu-id="59d61-139">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="59d61-140">Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes (wenn auch nicht unbedingt unterstützt) oder codecspezifische Optionen verfügbar sind, die vom Bildformatcodec entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="59d61-140">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="59d61-141">Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="59d61-141">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="59d61-142">Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie unter Übersicht über [die Codierung.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="59d61-142">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="59d61-143">Der TIFF-Codec verwendet grundlegende WIC-Optionen.</span><span class="sxs-lookup"><span data-stu-id="59d61-143">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="59d61-144">In der folgenden Tabelle sind die WIC-Encoderoptionen aufgeführt, die vom nativen TIFF-Codec unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="59d61-144">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="59d61-145">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="59d61-145">Property Name</span></span>         | <span data-ttu-id="59d61-146">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="59d61-146">VARTYPE</span></span> | <span data-ttu-id="59d61-147">Wertbereich</span><span class="sxs-lookup"><span data-stu-id="59d61-147">Value Range</span></span> | <span data-ttu-id="59d61-148">Standardwert</span><span class="sxs-lookup"><span data-stu-id="59d61-148">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="59d61-149">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="59d61-149">CompressionQuality</span></span>    | <span data-ttu-id="59d61-150">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="59d61-150">VT\_R4</span></span>  | <span data-ttu-id="59d61-151">0 - 1.0</span><span class="sxs-lookup"><span data-stu-id="59d61-151">0 - 1.0</span></span>     | <span data-ttu-id="59d61-152">0</span><span class="sxs-lookup"><span data-stu-id="59d61-152">0</span></span>                |
| <span data-ttu-id="59d61-153">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="59d61-153">TiffCompressionMethod</span></span> | <span data-ttu-id="59d61-154">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="59d61-154">VT\_UI1</span></span> | [<span data-ttu-id="59d61-155">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="59d61-155">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="59d61-156">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="59d61-156">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="59d61-157">Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="59d61-157">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="59d61-158">CompressionQuality-Option</span><span class="sxs-lookup"><span data-stu-id="59d61-158">CompressionQuality Option</span></span>

<span data-ttu-id="59d61-159">Gibt die gewünschte Komprimierungsqualität an.</span><span class="sxs-lookup"><span data-stu-id="59d61-159">Specifies the desired compression quality.</span></span> <span data-ttu-id="59d61-160">0.0 gibt das am wenigsten effiziente Komprimierungsschema an.</span><span class="sxs-lookup"><span data-stu-id="59d61-160">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="59d61-161">In der Regel führt dieses Schema zu einer schnelleren Codierung, aber zu einer größeren Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="59d61-161">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="59d61-162">Der Wert 1.0 gibt das effizienteste verfügbare Komprimierungsschema an.</span><span class="sxs-lookup"><span data-stu-id="59d61-162">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="59d61-163">In der Regel führt dieses Schema zu einer längeren Codierung, erzeugt jedoch eine kleinere Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="59d61-163">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="59d61-164">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="59d61-164">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="59d61-165">TiffCompressionMethod-Option</span><span class="sxs-lookup"><span data-stu-id="59d61-165">TiffCompressionMethod Option</span></span>

<span data-ttu-id="59d61-166">Gibt die TIFF-Komprimierungsmethode an.</span><span class="sxs-lookup"><span data-stu-id="59d61-166">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="59d61-167">Der Standardwert ist [**WICTiffCompressionDontCare.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)</span><span class="sxs-lookup"><span data-stu-id="59d61-167">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="59d61-168">Decodierung</span><span class="sxs-lookup"><span data-stu-id="59d61-168">Decoding</span></span>

<span data-ttu-id="59d61-169">Die WIC-Decodierungs-APIs sind codecunabhängig, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="59d61-169">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="59d61-170">Weitere Informationen zur Bilddecodierung finden Sie in der [Übersicht über die Decodierung.](-wic-creating-decoder.md)</span><span class="sxs-lookup"><span data-stu-id="59d61-170">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="59d61-171">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)</span><span class="sxs-lookup"><span data-stu-id="59d61-171">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
