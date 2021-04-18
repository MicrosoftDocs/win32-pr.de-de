---
description: Dieses Thema enthält Informationen über den nativen TIFF-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Übersicht über TIFF-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366143"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="e0299-103">Übersicht über TIFF-Format</span><span class="sxs-lookup"><span data-stu-id="e0299-103">TIFF Format Overview</span></span>

<span data-ttu-id="e0299-104">Dieses Thema enthält Informationen über den nativen TIFF-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e0299-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="e0299-105">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="e0299-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="e0299-106">Codieren</span><span class="sxs-lookup"><span data-stu-id="e0299-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="e0299-107">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="e0299-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="e0299-108">Decodierung</span><span class="sxs-lookup"><span data-stu-id="e0299-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="e0299-109">Codec-Identität</span><span class="sxs-lookup"><span data-stu-id="e0299-109">Codec Identity</span></span>

<span data-ttu-id="e0299-110">In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e0299-110">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="e0299-111">Formaler Name (n)</span><span class="sxs-lookup"><span data-stu-id="e0299-111">Formal Name(s)</span></span>         | <span data-ttu-id="e0299-112">TIFF (Tagged Image File Format)</span><span class="sxs-lookup"><span data-stu-id="e0299-112">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="e0299-113">Dateinamenerweiterung (en)</span><span class="sxs-lookup"><span data-stu-id="e0299-113">File Name Extension(s)</span></span> | <span data-ttu-id="e0299-114">TIFF, TIF</span><span class="sxs-lookup"><span data-stu-id="e0299-114">tiff, tif</span></span>                       |
| <span data-ttu-id="e0299-115">MIME-Typ (en)</span><span class="sxs-lookup"><span data-stu-id="e0299-115">MIME type(s)</span></span>           | <span data-ttu-id="e0299-116">Bild/TIFF, Bild/TIF</span><span class="sxs-lookup"><span data-stu-id="e0299-116">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="e0299-117">Spezifikations Unterstützung</span><span class="sxs-lookup"><span data-stu-id="e0299-117">Specification Support</span></span>  | <span data-ttu-id="e0299-118">TIFF-Spezifikation 6,0</span><span class="sxs-lookup"><span data-stu-id="e0299-118">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="e0299-119">In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen TIFF-Codec-Komponenten identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e0299-119">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="e0299-120">Komponente</span><span class="sxs-lookup"><span data-stu-id="e0299-120">Component</span></span>        | <span data-ttu-id="e0299-121">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="e0299-121">Friendly Name</span></span>             | <span data-ttu-id="e0299-122">GUID</span><span class="sxs-lookup"><span data-stu-id="e0299-122">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="e0299-123">Container Format</span><span class="sxs-lookup"><span data-stu-id="e0299-123">Container Format</span></span> | <span data-ttu-id="e0299-124">GUID \_ containerformattiff</span><span class="sxs-lookup"><span data-stu-id="e0299-124">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="e0299-125">163bcc30-e2e9-4f 0B-961da3e9sdb788a3</span><span class="sxs-lookup"><span data-stu-id="e0299-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="e0299-126">Decoder</span><span class="sxs-lookup"><span data-stu-id="e0299-126">Decoder</span></span>          | <span data-ttu-id="e0299-127">CLSID \_ wictiffdecoder</span><span class="sxs-lookup"><span data-stu-id="e0299-127">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="e0299-128">b54e85d9-FE23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="e0299-128">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="e0299-129">Encoder</span><span class="sxs-lookup"><span data-stu-id="e0299-129">Encoder</span></span>          | <span data-ttu-id="e0299-130">CLSID- \_ wictiffencoder</span><span class="sxs-lookup"><span data-stu-id="e0299-130">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="e0299-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="e0299-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="e0299-132">Codierung</span><span class="sxs-lookup"><span data-stu-id="e0299-132">Encoding</span></span>

<span data-ttu-id="e0299-133">Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="e0299-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e0299-134">Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e0299-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="e0299-135">Codierungsoptionen</span><span class="sxs-lookup"><span data-stu-id="e0299-135">Encoder Options</span></span>

<span data-ttu-id="e0299-136">WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene.</span><span class="sxs-lookup"><span data-stu-id="e0299-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="e0299-137">Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="e0299-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="e0299-138">Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format</span><span class="sxs-lookup"><span data-stu-id="e0299-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="e0299-139">Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e0299-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="e0299-140">Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e0299-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="e0299-141">Der TIFF-Codec verwendet grundlegende WIC-Optionen.</span><span class="sxs-lookup"><span data-stu-id="e0299-141">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="e0299-142">In der folgenden Tabelle sind die vom systemeigenen TIFF-Codec unterstützten WIC-Encoder-Optionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0299-142">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="e0299-143">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="e0299-143">Property Name</span></span>         | <span data-ttu-id="e0299-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e0299-144">VARTYPE</span></span> | <span data-ttu-id="e0299-145">Wertbereich</span><span class="sxs-lookup"><span data-stu-id="e0299-145">Value Range</span></span> | <span data-ttu-id="e0299-146">Standardwert</span><span class="sxs-lookup"><span data-stu-id="e0299-146">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="e0299-147">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="e0299-147">CompressionQuality</span></span>    | <span data-ttu-id="e0299-148">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="e0299-148">VT\_R4</span></span>  | <span data-ttu-id="e0299-149">0-1,0</span><span class="sxs-lookup"><span data-stu-id="e0299-149">0 - 1.0</span></span>     | <span data-ttu-id="e0299-150">0</span><span class="sxs-lookup"><span data-stu-id="e0299-150">0</span></span>                |
| <span data-ttu-id="e0299-151">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="e0299-151">TiffCompressionMethod</span></span> | <span data-ttu-id="e0299-152">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e0299-152">VT\_UI1</span></span> | [<span data-ttu-id="e0299-153">**Wictiffcompressionoption**</span><span class="sxs-lookup"><span data-stu-id="e0299-153">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="e0299-154">**Wictiffcompressiondontcare**</span><span class="sxs-lookup"><span data-stu-id="e0299-154">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="e0299-155">Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e0299-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="e0299-156">CompressionQuality (Option)</span><span class="sxs-lookup"><span data-stu-id="e0299-156">CompressionQuality Option</span></span>

<span data-ttu-id="e0299-157">Gibt die gewünschte Komprimierungs Qualität an.</span><span class="sxs-lookup"><span data-stu-id="e0299-157">Specifies the desired compression quality.</span></span> <span data-ttu-id="e0299-158">0,0 gibt das am wenigsten effiziente verfügbare Komprimierungs Schema an.</span><span class="sxs-lookup"><span data-stu-id="e0299-158">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="e0299-159">In der Regel führt dieses Schema zu einer schnelleren Codierung, aber eine größere Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e0299-159">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="e0299-160">Der Wert 1,0 gibt das effizienteste verfügbare Komprimierungs Schema an.</span><span class="sxs-lookup"><span data-stu-id="e0299-160">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="e0299-161">In der Regel führt dieses Schema zu einer längeren Codierung, erzeugt jedoch eine geringere Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e0299-161">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="e0299-162">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="e0299-162">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="e0299-163">Tiffcompressionmethod (Option)</span><span class="sxs-lookup"><span data-stu-id="e0299-163">TiffCompressionMethod Option</span></span>

<span data-ttu-id="e0299-164">Gibt die TIFF-Komprimierungs Methode an.</span><span class="sxs-lookup"><span data-stu-id="e0299-164">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="e0299-165">Der Standardwert ist [**wictiffcompressiondontcare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span><span class="sxs-lookup"><span data-stu-id="e0299-165">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="e0299-166">Decodierung</span><span class="sxs-lookup"><span data-stu-id="e0299-166">Decoding</span></span>

<span data-ttu-id="e0299-167">Die WIC-Decodierung-APIs sind als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch.</span><span class="sxs-lookup"><span data-stu-id="e0299-167">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="e0299-168">Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="e0299-168">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="e0299-169">Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="e0299-169">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
