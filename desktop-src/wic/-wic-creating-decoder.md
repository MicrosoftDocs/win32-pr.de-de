---
description: Das Thema enthält eine Einführung in den Bitmap-Decoder, eine Windows Imaging Component-Kernkomponente (WIC), die zum Decodieren von Bilddateien aus einem Stream verwendet wird.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: 'Decodierung: Übersicht'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349869"
---
# <a name="decoding-overview"></a><span data-ttu-id="70576-103">Decodierung: Übersicht</span><span class="sxs-lookup"><span data-stu-id="70576-103">Decoding Overview</span></span>

<span data-ttu-id="70576-104">Das Thema enthält eine Einführung in den Bitmap-Decoder, eine Windows Imaging Component-Kernkomponente (WIC), die zum Decodieren von Bilddateien aus einem Stream verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70576-104">The topic introduces the bitmap decoder, a core Windows Imaging Component (WIC) codec component used to decode image files from a stream.</span></span>

<span data-ttu-id="70576-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="70576-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="70576-106">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="70576-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="70576-107">Native Bitmap-decoderer</span><span class="sxs-lookup"><span data-stu-id="70576-107">Native Bitmap Decoders</span></span>](#native-bitmap-decoders)
-   [<span data-ttu-id="70576-108">Erstellen eines Bitmap-Decoders</span><span class="sxs-lookup"><span data-stu-id="70576-108">Creating a Bitmap Decoder</span></span>](#creating-a-bitmap-decoder)
-   [<span data-ttu-id="70576-109">Decodererweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="70576-109">Decoder Extensibility</span></span>](#decoder-extensibility)
-   [<span data-ttu-id="70576-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70576-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="70576-111">Einführung</span><span class="sxs-lookup"><span data-stu-id="70576-111">Introduction</span></span>

<span data-ttu-id="70576-112">BitmapDecoder können als äußerer Container eines digitalen Bilds angezeigt werden und bieten Zugriff auf globale Eigenschaften und Bild Frames.</span><span class="sxs-lookup"><span data-stu-id="70576-112">Bitmap decoders can be viewed as the outer container of a digital image and provides access to global properties and image frames.</span></span> <span data-ttu-id="70576-113">Einige Bildformate unterstützen globale Miniaturansichten, Vorschau Versionen, Farb Kontexte oder Metadaten, während andere diese Eigenschaften nur auf Frame-Ebene bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="70576-113">Some image formats support global thumbnails, previews, color contexts, or metadata, while others provide these properties only at the frame level.</span></span> <span data-ttu-id="70576-114">Beachten Sie jedoch, dass viele der Standardbild Formate diese globalen Eigenschaften nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="70576-114">Note, however, many of the standard image formats do not support these global properties.</span></span> <span data-ttu-id="70576-115">Daher unterstützen viele der systemeigenen Codec-Implementierungen, die von WIC bereitgestellt werden, nicht die Mehrzahl dieser globalen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="70576-115">As such, many of the native codec implementations provided by WIC do not support the majority of these global properties.</span></span> <span data-ttu-id="70576-116">Weitere Informationen zur Unterstützung von globalen Eigenschaften finden Sie in der Tabelle im Abschnitt Native Bitmap-Decoders dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="70576-116">See the table in the Native Bitmap Decoders section of this topic for information about global property support.</span></span>

<span data-ttu-id="70576-117">In WIC werden Bitmap-Decoder durch die [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle dargestellt und ermöglichen den Zugriff auf diese globalen Eigenschaften der Bitmap und, was noch wichtiger ist, die darin enthaltenen Frames.</span><span class="sxs-lookup"><span data-stu-id="70576-117">In WIC, bitmap decoders are represented by the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface and provides access to these global properties of the bitmap and, more importantly, the frames it contains.</span></span> <span data-ttu-id="70576-118">Die [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstelle stellt einen einzelnen BitmapFrame dar und wird in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md)ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="70576-118">The [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface represents an individual bitmap frame and is discussed in detail in the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="native-bitmap-decoders"></a><span data-ttu-id="70576-119">Native Bitmap-decoderer</span><span class="sxs-lookup"><span data-stu-id="70576-119">Native Bitmap Decoders</span></span>

<span data-ttu-id="70576-120">WIC stellt mehrere systemeigene Implementierungen der [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -Schnittstelle für die Standardweb Bildformate und das High Dynamic Range HD Photo-Format bereit.</span><span class="sxs-lookup"><span data-stu-id="70576-120">WIC provides several native implementations of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface for the standard web image formats and the high dynamic range HD Photo format.</span></span> <span data-ttu-id="70576-121">In der folgenden Tabelle sind die verfügbaren systemeigenen Decoders, der Klassen Bezeichnername und die Unterstützung für globale Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="70576-121">The following table lists the available native decoders, class identifier name, and support for global properties.</span></span> <span data-ttu-id="70576-122">Obwohl eine Funktion eine Eigenschaft, z. b. Miniaturansichten auf globaler Ebene, nicht unterstützt, kann das Bildformat solche Eigenschaften auf der einzelnen Frame Ebene unterstützen.</span><span class="sxs-lookup"><span data-stu-id="70576-122">Though a feature may not support a property such as thumbnails at the global level, the image format may support such properties at the individual frame level.</span></span>



| <span data-ttu-id="70576-123">Bildformat</span><span class="sxs-lookup"><span data-stu-id="70576-123">Image Format</span></span> | <span data-ttu-id="70576-124">CLSID-Name</span><span class="sxs-lookup"><span data-stu-id="70576-124">CLSID Name</span></span>            | <span data-ttu-id="70576-125">Miniaturbilder</span><span class="sxs-lookup"><span data-stu-id="70576-125">Thumbnails</span></span> | <span data-ttu-id="70576-126">Vorschau</span><span class="sxs-lookup"><span data-stu-id="70576-126">Previews</span></span> | <span data-ttu-id="70576-127">Farb Kontexte</span><span class="sxs-lookup"><span data-stu-id="70576-127">Color Contexts</span></span> | <span data-ttu-id="70576-128">Metadaten</span><span class="sxs-lookup"><span data-stu-id="70576-128">Metadata</span></span> |
|--------------|-----------------------|------------|----------|----------------|----------|
| <span data-ttu-id="70576-129">BMP</span><span class="sxs-lookup"><span data-stu-id="70576-129">BMP</span></span>          | <span data-ttu-id="70576-130">CLSID \_ wicbmpdecoder</span><span class="sxs-lookup"><span data-stu-id="70576-130">CLSID\_WICBmpDecoder</span></span>  | <span data-ttu-id="70576-131">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-131">No</span></span>         | <span data-ttu-id="70576-132">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-132">No</span></span>       | <span data-ttu-id="70576-133">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-133">No</span></span>             | <span data-ttu-id="70576-134">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-134">No</span></span>       |
| <span data-ttu-id="70576-135">GIF</span><span class="sxs-lookup"><span data-stu-id="70576-135">GIF</span></span>          | <span data-ttu-id="70576-136">CLSID- \_ wicgifdecoder</span><span class="sxs-lookup"><span data-stu-id="70576-136">CLSID\_WICGifDecoder</span></span>  | <span data-ttu-id="70576-137">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-137">No</span></span>         | <span data-ttu-id="70576-138">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-138">No</span></span>       | <span data-ttu-id="70576-139">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-139">No</span></span>             | <span data-ttu-id="70576-140">Ja</span><span class="sxs-lookup"><span data-stu-id="70576-140">Yes</span></span>      |
| <span data-ttu-id="70576-141">ICO</span><span class="sxs-lookup"><span data-stu-id="70576-141">ICO</span></span>          | <span data-ttu-id="70576-142">CLSID- \_ wicikodecoder</span><span class="sxs-lookup"><span data-stu-id="70576-142">CLSID\_WICIcoDecoder</span></span>  | <span data-ttu-id="70576-143">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-143">No</span></span>         | <span data-ttu-id="70576-144">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-144">No</span></span>       | <span data-ttu-id="70576-145">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-145">No</span></span>             | <span data-ttu-id="70576-146">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-146">No</span></span>       |
| <span data-ttu-id="70576-147">JPEG</span><span class="sxs-lookup"><span data-stu-id="70576-147">JPEG</span></span>         | <span data-ttu-id="70576-148">CLSID \_ wicjpgdecoder</span><span class="sxs-lookup"><span data-stu-id="70576-148">CLSID\_WICJpegDecoder</span></span> | <span data-ttu-id="70576-149">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-149">No</span></span>         | <span data-ttu-id="70576-150">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-150">No</span></span>       | <span data-ttu-id="70576-151">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-151">No</span></span>             | <span data-ttu-id="70576-152">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-152">No</span></span>       |
| <span data-ttu-id="70576-153">PNG</span><span class="sxs-lookup"><span data-stu-id="70576-153">PNG</span></span>          | <span data-ttu-id="70576-154">CLSID- \_ wicpngdecoder</span><span class="sxs-lookup"><span data-stu-id="70576-154">CLSID\_WICPngDecoder</span></span>  | <span data-ttu-id="70576-155">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-155">No</span></span>         | <span data-ttu-id="70576-156">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-156">No</span></span>       | <span data-ttu-id="70576-157">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-157">No</span></span>             | <span data-ttu-id="70576-158">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-158">No</span></span>       |
| <span data-ttu-id="70576-159">TIFF</span><span class="sxs-lookup"><span data-stu-id="70576-159">TIFF</span></span>         | <span data-ttu-id="70576-160">CLSID \_ wictiffdecoder</span><span class="sxs-lookup"><span data-stu-id="70576-160">CLSID\_WICTiffDecoder</span></span> | <span data-ttu-id="70576-161">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-161">No</span></span>         | <span data-ttu-id="70576-162">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-162">No</span></span>       | <span data-ttu-id="70576-163">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-163">No</span></span>             | <span data-ttu-id="70576-164">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-164">No</span></span>       |
| <span data-ttu-id="70576-165">HD-Foto</span><span class="sxs-lookup"><span data-stu-id="70576-165">HD Photo</span></span>     | <span data-ttu-id="70576-166">CLSID \_ wicwmpdecoder</span><span class="sxs-lookup"><span data-stu-id="70576-166">CLSID\_WICWmpDecoder</span></span>  | <span data-ttu-id="70576-167">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-167">No</span></span>         | <span data-ttu-id="70576-168">Ja</span><span class="sxs-lookup"><span data-stu-id="70576-168">Yes</span></span>      | <span data-ttu-id="70576-169">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-169">No</span></span>             | <span data-ttu-id="70576-170">Nein</span><span class="sxs-lookup"><span data-stu-id="70576-170">No</span></span>       |



 

## <a name="creating-a-bitmap-decoder"></a><span data-ttu-id="70576-171">Erstellen eines Bitmap-Decoders</span><span class="sxs-lookup"><span data-stu-id="70576-171">Creating a Bitmap Decoder</span></span>

<span data-ttu-id="70576-172">Zum Decodieren eines Bilds mit WIC müssen Sie zunächst eine Instanz des [**iwicbitmapdecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) für das Ziel Bildformat erstellen.</span><span class="sxs-lookup"><span data-stu-id="70576-172">To decode an image using WIC, you first need to create an instance of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) for the targeted image format.</span></span> <span data-ttu-id="70576-173">Die decoderinstanz ermöglicht Ihnen den Zugriff auf die globalen Eigenschaften und Metadaten, sofern dies unterstützt wird, sowie auf die Bildframes.</span><span class="sxs-lookup"><span data-stu-id="70576-173">The decoder instance enables you to access the global properties and metadata, if supported, as well as the image frames.</span></span> <span data-ttu-id="70576-174">Die WIC Imaging Factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), bietet verschiedene Methoden zum Erstellen von bitmapdecodern.</span><span class="sxs-lookup"><span data-stu-id="70576-174">The WIC imaging factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), provides several methods for creating bitmap decoders.</span></span> <span data-ttu-id="70576-175">Die folgenden Factorymethoden werden zum Erstellen von Bitmap-Decodern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="70576-175">The following factory methods are provided to create bitmap decoders.</span></span>

-   [<span data-ttu-id="70576-176">**Bilderstellungsfactory**</span><span class="sxs-lookup"><span data-stu-id="70576-176">**CreateDecoder**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [<span data-ttu-id="70576-177">**"Kreatedecoderfromfilehandle"**</span><span class="sxs-lookup"><span data-stu-id="70576-177">**CreateDecoderFromFileHandle**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [<span data-ttu-id="70576-178">**"Kreatedecoderfromfilename"**</span><span class="sxs-lookup"><span data-stu-id="70576-178">**CreateDecoderFromFilename**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [<span data-ttu-id="70576-179">**"Kreatedecoderfromstream"**</span><span class="sxs-lookup"><span data-stu-id="70576-179">**CreateDecoderFromStream**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

<span data-ttu-id="70576-180">Der folgende Code veranschaulicht, wie ein Bitmap-Decoder mit einem Bilddateinamen erstellt und der erste Frame des Bilds abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="70576-180">The following code demonstrates the how to create a bitmap decoder using an image filename and retrieve the first frame of the image.</span></span>


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a><span data-ttu-id="70576-181">Decodererweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="70576-181">Decoder Extensibility</span></span>

<span data-ttu-id="70576-182">Eines der wichtigsten Features von WIC ist ein Erweiterbarkeits Framework, mit dem Codec-Entwickler ihre eigenen Bild Codecs entwickeln und die gleiche Platt Form Unterstützung wie die systemeigenen Implementierungen von Bild Codecs erhalten können.</span><span class="sxs-lookup"><span data-stu-id="70576-182">One of the core features of WIC is an extensibility framework that enables codec developers to develop their own image codecs and get the same platform support as the native implementations of image codecs.</span></span> <span data-ttu-id="70576-183">Für alle Bildverarbeitung wird unabhängig vom Bildformat ein einzelner, einheitlicher Satz von Schnittstellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="70576-183">A single, consistent set of interfaces is used for all image processing, regardless of image format.</span></span> <span data-ttu-id="70576-184">Jede Anwendung, die WIC verwendet, erhält automatische Unterstützung für neue Bildformate, sobald der Codec installiert ist.</span><span class="sxs-lookup"><span data-stu-id="70576-184">Any application using WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="70576-185">Weitere Informationen zur Codec-Entwicklung finden Sie in den Themen unter [Komponentenentwicklung](-wic-component-development.md).</span><span class="sxs-lookup"><span data-stu-id="70576-185">For more information on codec development, see the topics in [Component Development](-wic-component-development.md).</span></span> <span data-ttu-id="70576-186">Weitere Informationen zur decoderentwicklung finden Sie unter [Implementieren eines WIC-Enabled Decoders](-wic-implementingwicdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="70576-186">For more information on decoder development, see [Implementing a WIC-Enabled Decoder](-wic-implementingwicdecoder.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="70576-187">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70576-187">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="70576-188">**Licher**</span><span class="sxs-lookup"><span data-stu-id="70576-188">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="70576-189">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="70576-189">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="70576-190">Übersicht über die Codierung</span><span class="sxs-lookup"><span data-stu-id="70576-190">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> <dt>

[<span data-ttu-id="70576-191">Komponentenentwicklung</span><span class="sxs-lookup"><span data-stu-id="70576-191">Component Development</span></span>](-wic-component-development.md)
</dt> </dl>

 

 



