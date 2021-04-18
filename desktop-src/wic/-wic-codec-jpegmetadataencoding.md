---
description: Im folgenden Beispiel wird veranschaulicht, wie ein Bild und seine Metadaten erneut in eine neue Datei mit demselben Format codiert werden.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: 'Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106365146"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a><span data-ttu-id="d20c9-103">Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="d20c9-103">How-to re-encode a JPEG image with metadata</span></span>

<span data-ttu-id="d20c9-104">Im folgenden Beispiel wird veranschaulicht, wie ein Bild und seine Metadaten erneut in eine neue Datei mit demselben Format codiert werden.</span><span class="sxs-lookup"><span data-stu-id="d20c9-104">The following example demonstrates how to re-encode an image and its metadata to a new file of the same format.</span></span> <span data-ttu-id="d20c9-105">Außerdem werden in diesem Beispiel Metadaten hinzugefügt, um einen einzelnen Element Ausdruck zu veranschaulichen, der von einem Abfrage-Writer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d20c9-105">In addition, this example adds metadata to demonstrate a single-item expression used by a query writer.</span></span>

<span data-ttu-id="d20c9-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d20c9-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d20c9-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d20c9-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="d20c9-108">Teil 1: Decodieren eines Bilds</span><span class="sxs-lookup"><span data-stu-id="d20c9-108">Part 1: Decode an Image</span></span>](#part-1-decode-an-image)
-   [<span data-ttu-id="d20c9-109">Teil 2: Erstellen und Initialisieren des Image Encoders</span><span class="sxs-lookup"><span data-stu-id="d20c9-109">Part 2: Create and Initialize the Image Encoder</span></span>](#part-2-create-and-initialize-the-image-encoder)
-   [<span data-ttu-id="d20c9-110">Teil 3: Kopieren von decodierten Frame Informationen</span><span class="sxs-lookup"><span data-stu-id="d20c9-110">Part 3: Copy Decoded Frame Information</span></span>](#part-3-copy-decoded-frame-information)
-   [<span data-ttu-id="d20c9-111">Teil 4: Kopieren der Metadaten</span><span class="sxs-lookup"><span data-stu-id="d20c9-111">Part 4: Copy the Metadata</span></span>](#part-4-copy-the-metadata)
-   [<span data-ttu-id="d20c9-112">Teil 5: Hinzufügen zusätzlicher Metadaten</span><span class="sxs-lookup"><span data-stu-id="d20c9-112">Part 5: Add Additional Metadata</span></span>](#part-5-add-additional-metadata)
-   [<span data-ttu-id="d20c9-113">Teil 6: Finalisieren des codierten Bilds</span><span class="sxs-lookup"><span data-stu-id="d20c9-113">Part 6: Finalize the Encoded Image</span></span>](#part-6-finalize-the-encoded-image)
-   [<span data-ttu-id="d20c9-114">JPEG Umcodieren von Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="d20c9-114">JPEG Re-encode Example Code</span></span>](#jpeg-re-encode-example-code)
-   [<span data-ttu-id="d20c9-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d20c9-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="d20c9-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d20c9-116">Prerequisites</span></span>

<span data-ttu-id="d20c9-117">Um dieses Thema zu verstehen, sollten Sie sich mit dem Metadatensystem der Windows Imaging Component (WIC) vertraut machen, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d20c9-117">To understand this topic, you should be familiar with the Windows Imaging Component (WIC) metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="d20c9-118">Sie sollten auch mit den WIC-Codec-Komponenten vertraut sein, wie in der [Übersicht über Windows Imaging](-wic-about-windows-imaging-codec.md)-Komponenten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d20c9-118">You should also be familiar with the WIC codec components as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="part-1-decode-an-image"></a><span data-ttu-id="d20c9-119">Teil 1: Decodieren eines Bilds</span><span class="sxs-lookup"><span data-stu-id="d20c9-119">Part 1: Decode an Image</span></span>

<span data-ttu-id="d20c9-120">Bevor Sie Bilddaten oder Metadaten in eine neue Bilddatei kopieren können, müssen Sie zuerst einen Decoder für das vorhandene Abbild erstellen, das Sie erneut codieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d20c9-120">Before you can copy image data or metadata to a new image file, you must first create a decoder for the existing image that you want to re-encode.</span></span> <span data-ttu-id="d20c9-121">Der folgende Code veranschaulicht, wie ein WIC-Decoder für die Bilddatei test.jpg erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d20c9-121">The following code demonstrates how to create a WIC decoder for the image file test.jpg.</span></span>


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



<span data-ttu-id="d20c9-122">Beim Aufrufen von " **anatedecoderfromfilename** " wurde der Wert WICDecodeMetadataCacheOnDemand aus der [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) -Enumeration als vierter Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="d20c9-122">The call to **CreateDecoderFromFilename** used the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration as the fourth parameter.</span></span> <span data-ttu-id="d20c9-123">Dadurch wird der Decoder aufgefordert, die Metadaten zwischenzuspeichern, wenn die Metadaten benötigt werden, entweder durch Abrufen eines Abfrage Readers oder durch Verwendung des zugrunde liegenden metadatenreaders.</span><span class="sxs-lookup"><span data-stu-id="d20c9-123">This tells the decoder to cache the metadata when the metadata is needed, either by obtaining a query reader or by using the underlying metadata reader.</span></span> <span data-ttu-id="d20c9-124">Wenn Sie diese Option verwenden, können Sie den Datenstrom in den Metadaten beibehalten. Dies ist für die schnelle metadatencodierung erforderlich und ermöglicht die Verlust lose Decodierung und Codierung von JPEG-Bildern.</span><span class="sxs-lookup"><span data-stu-id="d20c9-124">Using this option enables you to retain the stream to the metadata, which is required for performing fast metadata encoding and enables lossless decoding and encoding of JPEG images.</span></span> <span data-ttu-id="d20c9-125">Alternativ können Sie auch den anderen **wicdecodeoptions** -Wert, WICDecodeMetadataCacheOnLoad, verwenden, der die eingebetteten Bild Metadaten zwischenspeichert, sobald das Bild geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d20c9-125">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

## <a name="part-2-create-and-initialize-the-image-encoder"></a><span data-ttu-id="d20c9-126">Teil 2: Erstellen und Initialisieren des Image Encoders</span><span class="sxs-lookup"><span data-stu-id="d20c9-126">Part 2: Create and Initialize the Image Encoder</span></span>

<span data-ttu-id="d20c9-127">Der folgende Code veranschaulicht die Erstellung des Encoders, den Sie verwenden, um das Image zu codieren, das Sie zuvor decodiert haben.</span><span class="sxs-lookup"><span data-stu-id="d20c9-127">The following code demonstrates the creation of the encoder you will use to encode the image you previously decoded.</span></span>


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



<span data-ttu-id="d20c9-128">Ein WIC-Datei Datenstrom: pifilestream wird erstellt und zum Schreiben in die Bilddatei "test2.jpg" initialisiert.</span><span class="sxs-lookup"><span data-stu-id="d20c9-128">A WIC file stream piFileStream is created and initialized for writing to the image file "test2.jpg".</span></span> <span data-ttu-id="d20c9-129">pifilestream wird dann verwendet, um den Encoder zu initialisieren und den Encoder darüber zu informieren, wo die Abbild Bits geschrieben werden sollen, wenn die Codierung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="d20c9-129">piFileStream is then used to initialize the encoder, informing the encoder where to write the image bits when the encoding is complete.</span></span>

## <a name="part-3-copy-decoded-frame-information"></a><span data-ttu-id="d20c9-130">Teil 3: Kopieren von decodierten Frame Informationen</span><span class="sxs-lookup"><span data-stu-id="d20c9-130">Part 3: Copy Decoded Frame Information</span></span>

<span data-ttu-id="d20c9-131">Der folgende Code kopiert jeden Frame eines Bilds in einen neuen Frame des Encoders.</span><span class="sxs-lookup"><span data-stu-id="d20c9-131">The following code copies each frame of an image to a new frame of the encoder.</span></span> <span data-ttu-id="d20c9-132">Diese Kopie umfasst Größe, Auflösung und Pixel Format. Alle sind erforderlich, um einen gültigen Frame zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d20c9-132">This copy includes size, resolution, and pixel format; all of which are necessary to create a valid frame.</span></span>

> [!Note]  
> <span data-ttu-id="d20c9-133">JPEG-Bilder verfügen nur über einen Frame, und die nachfolgende Schleife ist technisch nicht erforderlich, ist jedoch enthalten, um die Multi-Frame-Verwendung für Formate zu veranschaulichen, die diese unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d20c9-133">JPEG images will only have one frame and the loop below is not technically necessary but is included to demonstrate multi-frame usage for formats that support it.</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



<span data-ttu-id="d20c9-134">Der folgende Code führt eine schnelle Überprüfung durch, um zu bestimmen, ob die Quell-und Ziel Bildformate identisch sind.</span><span class="sxs-lookup"><span data-stu-id="d20c9-134">The following code performs a quick check to determine whether the source and destination image formats are the same.</span></span> <span data-ttu-id="d20c9-135">Dies ist erforderlich, da Teil 4 einen Vorgang anzeigt, der nur unterstützt wird, wenn das Quell-und Zielformat identisch sind.</span><span class="sxs-lookup"><span data-stu-id="d20c9-135">This is needed as Part 4 shows an operation that is only supported when the source and destination format are the same.</span></span>


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a><span data-ttu-id="d20c9-136">Teil 4: Kopieren der Metadaten</span><span class="sxs-lookup"><span data-stu-id="d20c9-136">Part 4: Copy the Metadata</span></span>

> [!Note]  
> <span data-ttu-id="d20c9-137">Der Code in diesem Abschnitt ist nur gültig, wenn die Quell-und Ziel Image Formate identisch sind.</span><span class="sxs-lookup"><span data-stu-id="d20c9-137">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="d20c9-138">Wenn Sie in ein anderes Bildformat codieren, können Sie nicht alle Metadaten eines Bilds in einem einzelnen Vorgang kopieren.</span><span class="sxs-lookup"><span data-stu-id="d20c9-138">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="d20c9-139">Zum Beibehalten von Metadaten beim erneuten Codieren eines Bilds in dasselbe Bildformat stehen Methoden zum Kopieren aller Metadaten in einem einzelnen Vorgang zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d20c9-139">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="d20c9-140">Jeder dieser Vorgänge folgt einem ähnlichen Muster: jede legt die Metadaten des decodierten Frames direkt in den neuen Frame fest, der codiert wird.</span><span class="sxs-lookup"><span data-stu-id="d20c9-140">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span> <span data-ttu-id="d20c9-141">Beachten Sie, dass dies für jeden einzelnen Bild Rahmen erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d20c9-141">Note that this is done for each individual image frame.</span></span>

<span data-ttu-id="d20c9-142">Die bevorzugte Methode zum Kopieren von Metadaten besteht darin, den blockwriter des neuen Frames mit dem Block Reader des decodierten Frames zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d20c9-142">The preferred method for copying metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="d20c9-143">Der folgende Code veranschaulicht diese Methode.</span><span class="sxs-lookup"><span data-stu-id="d20c9-143">The following code demonstrates this method.</span></span>


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



<span data-ttu-id="d20c9-144">In diesem Beispiel rufen Sie einfach den Block Reader und den blockwriter aus dem Quellframe bzw. dem Zielframe ab.</span><span class="sxs-lookup"><span data-stu-id="d20c9-144">In this example, you simply obtain the block reader and block writer from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="d20c9-145">Der blockwriter wird dann vom Block Reader initialisiert.</span><span class="sxs-lookup"><span data-stu-id="d20c9-145">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="d20c9-146">Dadurch wird der blockwriter mit den vorab aufgefüllten Metadaten des Block Readers initialisiert.</span><span class="sxs-lookup"><span data-stu-id="d20c9-146">This initializes the block writer with the pre-populated metadata of the block reader.</span></span> <span data-ttu-id="d20c9-147">Weitere Methoden zum Kopieren von Metadaten finden Sie im Abschnitt Schreiben von Metadaten in der [Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="d20c9-147">To learn additional methods for copying metadata, see the Writing Metadata section in the [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="d20c9-148">Auch dieser Vorgang funktioniert nur, wenn die Quell-und Ziel Images das gleiche Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d20c9-148">Again, this operation works only when the source and destination images have the same format.</span></span> <span data-ttu-id="d20c9-149">Dies liegt daran, dass unterschiedliche Bildformate die Metadatenblöcke an verschiedenen Speicherorten speichern.</span><span class="sxs-lookup"><span data-stu-id="d20c9-149">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="d20c9-150">Beispielsweise unterstützen sowohl JPEG als auch Tagged Image File Format (TIFF) Extensible Metadata Platform (XMP)-Metadatenblöcke.</span><span class="sxs-lookup"><span data-stu-id="d20c9-150">For instance, both JPEG and Tagged Image File Format (TIFF) support Extensible Metadata Platform (XMP) metadata blocks.</span></span> <span data-ttu-id="d20c9-151">In JPEG-Bildern befindet sich der XMP-Block im stammmetadatenblock, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d20c9-151">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="d20c9-152">In einem TIFF-Bild wird der XMP-Block jedoch in den IFD-Stammblock eingebettet.</span><span class="sxs-lookup"><span data-stu-id="d20c9-152">However, in a TIFF image, the XMP block is embedded in the root IFD block.</span></span>

## <a name="part-5-add-additional-metadata"></a><span data-ttu-id="d20c9-153">Teil 5: Hinzufügen zusätzlicher Metadaten</span><span class="sxs-lookup"><span data-stu-id="d20c9-153">Part 5: Add Additional Metadata</span></span>

<span data-ttu-id="d20c9-154">Im folgenden Beispiel wird veranschaulicht, wie dem Zielbild Metadaten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d20c9-154">The following example demonstrates how to add metadata to the destination image.</span></span> <span data-ttu-id="d20c9-155">Dies erfolgt durch Aufrufen der **SetMetadataByName** -Methode des Abfrage Writers mithilfe eines Abfrage Ausdrucks und der in einem [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="d20c9-155">This is done by calling the query writer's **SetMetadataByName** method using a query expression and the data stored in a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span>


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



<span data-ttu-id="d20c9-156">Weitere Informationen zum Abfrage Ausdruck finden Sie in der [Übersicht über die Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="d20c9-156">For more information on the query expression, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="part-6-finalize-the-encoded-image"></a><span data-ttu-id="d20c9-157">Teil 6: Finalisieren des codierten Bilds</span><span class="sxs-lookup"><span data-stu-id="d20c9-157">Part 6: Finalize the Encoded Image</span></span>

<span data-ttu-id="d20c9-158">Die abschließenden Schritte zum Kopieren des Bilds sind das Schreiben der Pixeldaten für den Frame, das Ausführen eines Commit für den Frame an den Encoder und das Ausführen eines Commit für den Encoder.</span><span class="sxs-lookup"><span data-stu-id="d20c9-158">The final steps for copying the image are to write the pixel data for the frame, commit the frame to the encoder, and commit the encoder.</span></span> <span data-ttu-id="d20c9-159">Durch das committen des Encoders wird der Bildstream in die Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d20c9-159">Committing the encoder writes the image stream to the file.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



<span data-ttu-id="d20c9-160">Die "Write **tesource** "-Methode des Frames dient zum Schreiben der Pixeldaten für das Bild.</span><span class="sxs-lookup"><span data-stu-id="d20c9-160">The frame's **WriteSource** method is used to write the pixel data for the image.</span></span> <span data-ttu-id="d20c9-161">Beachten Sie, dass dies geschieht, nachdem die Metadaten geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="d20c9-161">Note that this is done after the metadata has been written.</span></span> <span data-ttu-id="d20c9-162">Dies ist erforderlich, um sicherzustellen, dass die Metadaten über ausreichend Speicherplatz innerhalb der Bilddatei verfügen.</span><span class="sxs-lookup"><span data-stu-id="d20c9-162">This is necessary to ensure that the metadata has enough space within the image file.</span></span> <span data-ttu-id="d20c9-163">Nachdem die Pixeldaten geschrieben wurden, wird der Frame mithilfe der **Commit** -Methode von Frame in den Stream geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d20c9-163">After the pixel data is written, the frame is written to the stream using the frame's **Commit** method.</span></span> <span data-ttu-id="d20c9-164">Nachdem alle Frames verarbeitet wurden, wird der Encoder (und damit das Bild) mithilfe der **Commit** -Methode des Encoders fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="d20c9-164">After all frames have been processed, the encoder (and thus the image) is finalized using the encoder's **Commit** method.</span></span>

<span data-ttu-id="d20c9-165">Nachdem Sie einen Commit für den Frame durchgeführt haben, müssen Sie die in der-Schleife erstellten COM-Objekte freigeben.</span><span class="sxs-lookup"><span data-stu-id="d20c9-165">Once you commit the frame, you must release the COM objects created in the loop.</span></span>

## <a name="jpeg-re-encode-example-code"></a><span data-ttu-id="d20c9-166">JPEG Umcodieren von Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="d20c9-166">JPEG Re-encode Example Code</span></span>

<span data-ttu-id="d20c9-167">Im folgenden finden Sie den Code von den Teilen 1 bis 6 in einem convienient-Block.</span><span class="sxs-lookup"><span data-stu-id="d20c9-167">The following is the code from Parts 1 through 6 in one convienient block.</span></span>


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d20c9-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d20c9-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d20c9-169">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d20c9-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d20c9-170">Übersicht über WIC-Metadaten</span><span class="sxs-lookup"><span data-stu-id="d20c9-170">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="d20c9-171">Übersicht über die Metadaten-Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="d20c9-171">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="d20c9-172">Übersicht über das Lesen und Schreiben von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="d20c9-172">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="d20c9-173">Übersicht über die metadatenerweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="d20c9-173">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
