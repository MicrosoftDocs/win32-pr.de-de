---
description: Dieses Thema bietet einen Überblick über die Verwendung der WIC-APIs (Windows Imaging Component) zum Lesen und Schreiben von Metadaten, die in Bilddateien eingebettet sind.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Übersicht über das Lesen und Schreiben von Bild Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959943"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a><span data-ttu-id="ee962-103">Übersicht über das Lesen und Schreiben von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-103">Overview of Reading and Writing Image Metadata</span></span>

<span data-ttu-id="ee962-104">Dieses Thema bietet einen Überblick über die Verwendung der WIC-APIs (Windows Imaging Component) zum Lesen und Schreiben von Metadaten, die in Bilddateien eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="ee962-104">This topic provides an overview of how you can use the Windows Imaging Component (WIC) APIs to read and write metadata that is embedded in image files.</span></span>

<span data-ttu-id="ee962-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ee962-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ee962-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ee962-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="ee962-107">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="ee962-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="ee962-108">Lesen von Metadadata mithilfe eines Abfrage Readers</span><span class="sxs-lookup"><span data-stu-id="ee962-108">Reading Metadadata Using a Query Reader</span></span>](#reading-metadadata-using-a-query-reader)
    -   [<span data-ttu-id="ee962-109">Abrufen eines Abfrage Readers</span><span class="sxs-lookup"><span data-stu-id="ee962-109">Obtaining a Query Reader</span></span>](#obtaining-a-query-reader)
    -   [<span data-ttu-id="ee962-110">Lesen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-110">Reading Metadata</span></span>](#reading-metadata)
    -   [<span data-ttu-id="ee962-111">Zusätzliche Abfrage Reader-Methoden</span><span class="sxs-lookup"><span data-stu-id="ee962-111">Additional Query Reader Methods</span></span>](#additional-query-reader-methods)
-   [<span data-ttu-id="ee962-112">Schreiben von Metadaten mit einem Abfrage-Writer</span><span class="sxs-lookup"><span data-stu-id="ee962-112">Writing Metadata Using a Query Writer</span></span>](#writing-metadata-using-a-query-writer)
    -   [<span data-ttu-id="ee962-113">Abrufen eines Abfrage-Writers</span><span class="sxs-lookup"><span data-stu-id="ee962-113">Obtaining a Query Writer</span></span>](#obtaining-a-query-writer)
    -   [<span data-ttu-id="ee962-114">Hinzufügen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-114">Adding Metadata</span></span>](#adding-metadata)
    -   [<span data-ttu-id="ee962-115">Entfernen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-115">Removing Metadata</span></span>](#removing-metadata)
    -   [<span data-ttu-id="ee962-116">Kopieren von Metadaten für die erneute Codierung</span><span class="sxs-lookup"><span data-stu-id="ee962-116">Copying Metadata for Re-encoding</span></span>](#copying-metadata-for-re-encoding)
-   [<span data-ttu-id="ee962-117">Schnelle metadatencodierung</span><span class="sxs-lookup"><span data-stu-id="ee962-117">Fast Metadata Encoding</span></span>](#fast-metadata-encoding)
    -   [<span data-ttu-id="ee962-118">Hinzufügen von Padding zu metadatenblöcken</span><span class="sxs-lookup"><span data-stu-id="ee962-118">Adding Padding to Metadata Blocks</span></span>](#adding-padding-to-metadata-blocks)
    -   [<span data-ttu-id="ee962-119">Abrufen eines schnellen metadatenencoders</span><span class="sxs-lookup"><span data-stu-id="ee962-119">Obtaining a Fast Metadata Encoder</span></span>](#obtaining-a-fast-metadata-encoder)
    -   [<span data-ttu-id="ee962-120">Verwenden des schnellen metadatenencoders</span><span class="sxs-lookup"><span data-stu-id="ee962-120">Using the Fast Metadata Encoder</span></span>](#using-the-fast-metadata-encoder)
-   [<span data-ttu-id="ee962-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee962-121">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="ee962-122">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ee962-122">Prerequisites</span></span>

<span data-ttu-id="ee962-123">Um dieses Thema zu verstehen, sollten Sie mit dem WIC-Metadatensystem vertraut sein, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee962-123">To understand this topic, you should be familiar with the WIC metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="ee962-124">Sie sollten auch mit der Abfragesprache vertraut sein, die zum Lesen und Schreiben von Metadaten verwendet wird, wie unter [Übersicht über die metadatenquery-Sprache](-wic-codec-metadataquerylanguage.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee962-124">You should also be familiar with the query language used to read and write metadata, as described in [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="ee962-125">Einführung</span><span class="sxs-lookup"><span data-stu-id="ee962-125">Introduction</span></span>

<span data-ttu-id="ee962-126">WIC bietet Anwendungsentwicklern Component Object Model (com)-Komponenten zum Lesen und Schreiben von Metadaten, die in Bilddateien eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="ee962-126">WIC provides application developers with Component Object Model (COM) components to read and write metadata embedded in image files.</span></span> <span data-ttu-id="ee962-127">Es gibt zwei Möglichkeiten, um Metadaten zu lesen und zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="ee962-127">There are two ways to read and write metadata:</span></span>

-   <span data-ttu-id="ee962-128">Verwenden eines Abfrage Readers/Writer und eines Abfrage Ausdrucks, um Metadatenblöcke für geschachtelte Blöcke oder bestimmte Metadaten innerhalb eines-Blocks abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ee962-128">Using a query reader/writer and a query expression to query metadata blocks for nested blocks or specific metadata within a block.</span></span>
-   <span data-ttu-id="ee962-129">Verwenden eines metadatenhandlers (ein metadatenreader oder ein metadatenwriter) für den Zugriff auf geschachtelte Metadatenblöcke oder bestimmte Metadaten innerhalb der Metadatenblöcke.</span><span class="sxs-lookup"><span data-stu-id="ee962-129">Using a metadata handler (a metadata reader or a metadata writer) to access the nested metadata blocks or specific metadata within the metadata blocks.</span></span>

<span data-ttu-id="ee962-130">Am einfachsten ist es, einen Abfrage Reader/-Writer und einen Abfrage Ausdruck zu verwenden, um auf die Metadaten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee962-130">The easiest of these is to use a query reader/writer and a query expression to access the metadata.</span></span> <span data-ttu-id="ee962-131">Ein Abfrage Reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) wird zum Lesen von Metadaten verwendet, während ein Abfrage Schreiber ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) verwendet wird, um Metadaten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ee962-131">A query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) is used to read metadata while a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used to write metadata.</span></span> <span data-ttu-id="ee962-132">Beide verwenden einen Abfrage Ausdruck, um die gewünschten Metadaten zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ee962-132">Both of these use a query expression to read or write the desired metadata.</span></span> <span data-ttu-id="ee962-133">Im Hintergrund verwendet ein Abfrage Leser (und Writer) einen Metadatenhandler, um auf die vom Abfrage Ausdruck beschriebenen Metadaten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee962-133">Behind the scenes, a query reader (and writer) uses a metadata handler to access the metadata described by the query expression.</span></span>

<span data-ttu-id="ee962-134">Die erweiterte Methode besteht darin, direkt auf die Metadatenhandler zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee962-134">The more advanced method is to directly access the metadata handlers.</span></span> <span data-ttu-id="ee962-135">Ein Metadatenhandler wird aus den einzelnen Frames mithilfe eines Block Readers ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) oder eines blockwriter ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-135">A metadata handler is obtained from the individual frames using a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) or a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span></span> <span data-ttu-id="ee962-136">Die beiden verfügbaren Metadatenhandler sind der metadatenreader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) und der metadatenwriter ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span><span class="sxs-lookup"><span data-stu-id="ee962-136">The two types of metadata handlers available are the metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) and the metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span></span>

<span data-ttu-id="ee962-137">Das folgende Diagramm des Inhalts einer JPEG-Bilddatei wird in den Beispielen in diesem Thema verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee962-137">The following diagram of the contents of a JPEG image file is used throughout the examples in this topic.</span></span> <span data-ttu-id="ee962-138">Das durch dieses Diagramm dargestellte Bild wurde mit Microsoft Paint erstellt. die Bewertungs Metadaten wurden mithilfe der Photo Gallery-Funktion von Windows Vista hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ee962-138">The image represented by this diagram was created by using Microsoft Paint; the rating metadata was added by using the Photo Gallery feature of Windows Vista.</span></span>

![Abbildung des JPEG-Bilds mit Bewertungs Metadaten](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a><span data-ttu-id="ee962-140">Lesen von Metadadata mithilfe eines Abfrage Readers</span><span class="sxs-lookup"><span data-stu-id="ee962-140">Reading Metadadata Using a Query Reader</span></span>

<span data-ttu-id="ee962-141">Die einfachste Möglichkeit zum Lesen von Metadaten ist die Verwendung der Abfrage Lese Schnittstelle, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="ee962-141">The easiest way to read metadata is to use the query reader interface, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span> <span data-ttu-id="ee962-142">Der Abfrage Reader ermöglicht das Lesen von metadatenblöcken und Elementen innerhalb von metadatenblöcken mithilfe eines Abfrage Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="ee962-142">The query reader enables you to read metadata blocks and items within metadata blocks using a query expression.</span></span>

<span data-ttu-id="ee962-143">Es gibt drei Möglichkeiten zum Abrufen eines Abfrage Readers: über einen Bitmap-Decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), über die einzelnen Frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) oder über einen Abfrage-Writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="ee962-143">There are three ways to obtain a query reader: through a bitmap decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), through its individual frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)), or through a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span>

### <a name="obtaining-a-query-reader"></a><span data-ttu-id="ee962-144">Abrufen eines Abfrage Readers</span><span class="sxs-lookup"><span data-stu-id="ee962-144">Obtaining a Query Reader</span></span>

<span data-ttu-id="ee962-145">Der folgende Beispielcode zeigt, wie Sie einen Bitmap-Decoder aus der Imaging Factory abrufen und einen einzelnen BitmapFrame abrufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-145">The following example code shows how to obtain a bitmap decoder from the imaging factory and retrieve an individual bitmap frame.</span></span> <span data-ttu-id="ee962-146">Dieser Code führt auch Setup Schritte aus, die zum Abrufen eines Abfrage Readers von einem decodierten Frame erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ee962-146">This code also performs setup work needed to obtain a query reader from a decoded frame.</span></span>


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



<span data-ttu-id="ee962-147">Der Bitmap-Decoder für die test.jpg Datei wird mithilfe der Methode " **kreatedecoderfromfilename** " der Imaging Factory abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-147">The bitmap decoder for the test.jpg file is obtained by using the **CreateDecoderFromFilename** method of the imaging factory.</span></span> <span data-ttu-id="ee962-148">In dieser Methode wird der vierte Parameter auf den Wert WICDecodeMetadataCacheOnDemand aus der [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) -Enumeration festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee962-148">In this method, the fourth parameter is set to the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration.</span></span> <span data-ttu-id="ee962-149">Dadurch wird der Decoder aufgefordert, die Metadaten zwischenzuspeichern, wenn die Metadaten benötigt werden. entweder durch Abrufen eines Abfrage Readers oder des zugrunde liegenden metadatenreaders.</span><span class="sxs-lookup"><span data-stu-id="ee962-149">This tells the decoder to cache the metadata when the metadata is needed; either by obtaining a query reader or the underlying metadata reader.</span></span> <span data-ttu-id="ee962-150">Wenn Sie diese Option verwenden, können Sie den Datenstrom in den Metadaten aufbewahren, die für die schnelle metadatencodierung erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="ee962-150">Using this option enables you to retain the stream to the metadata required for fast metadata encoding and enables lossless decoding of the JPEG image.</span></span> <span data-ttu-id="ee962-151">Alternativ können Sie auch den anderen **wicdecodeoptions** -Wert, WICDecodeMetadataCacheOnLoad, verwenden, der die eingebetteten Bild Metadaten zwischenspeichert, sobald das Bild geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-151">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

<span data-ttu-id="ee962-152">Um den Abfrage Reader des Frames abzurufen, führen Sie einen einfachen Abruf der **GetMetadataQueryReader** -Methode des Frames aus.</span><span class="sxs-lookup"><span data-stu-id="ee962-152">To obtain the frame's query reader, make a simple call to the frame's **GetMetadataQueryReader** method.</span></span> <span data-ttu-id="ee962-153">Der folgende Code veranschaulicht diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="ee962-153">The following code demonstrates this call.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="ee962-154">Ebenso kann ein Abfrage Reader auch auf der decoderebene abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-154">Similarly, a query reader can also be obtained at the decoder level.</span></span> <span data-ttu-id="ee962-155">Ein einfacher Aufrufder **GetMetadataQueryReader** -Methode des Decoders Ruft den Abfrage Reader des Decoders ab.</span><span class="sxs-lookup"><span data-stu-id="ee962-155">A simple call to the decoder's **GetMetadataQueryReader** method gets the decoder's query reader.</span></span> <span data-ttu-id="ee962-156">Im Gegensatz zum Abfrage Leser eines Frames liest der Abfrage Reader eines Decoders Metadaten für ein Bild, das sich außerhalb der einzelnen Frames befindet.</span><span class="sxs-lookup"><span data-stu-id="ee962-156">An decoder's query reader, unlike a frame's query reader, reads metadata for an image that is outside of the individual frames.</span></span> <span data-ttu-id="ee962-157">Dieses Szenario ist jedoch nicht üblich, und die nativen Image Formate unterstützen diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="ee962-157">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="ee962-158">Das systemeigene Bild, das von WIC bereitgestellt wird, dient zum Lesen und Schreiben von Metadaten auf Frame-Ebene, auch bei Einzel Frame Formaten wie JPEG.</span><span class="sxs-lookup"><span data-stu-id="ee962-158">The native image CODECS provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

### <a name="reading-metadata"></a><span data-ttu-id="ee962-159">Lesen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-159">Reading Metadata</span></span>

<span data-ttu-id="ee962-160">Bevor Sie mit dem Lesen von Metadaten fortfahren, sehen Sie sich das folgende Diagramm einer JPEG-Datei an, die eingebettete Metadatenblöcke und die tatsächlich abzurufenden Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ee962-160">Before you move on to actually reading metadata, look at the following diagram of a JPEG file that includes embedded metadata blocks and actual data to retrieve.</span></span> <span data-ttu-id="ee962-161">Dieses Diagramm stellt Legenden für bestimmte Metadatenblöcke und Elemente innerhalb des Bilds bereit und stellt den metadatenabfrageausdruck für jeden Block oder jedes Element bereit.</span><span class="sxs-lookup"><span data-stu-id="ee962-161">This diagram provides callouts to specific metadata blocks and items within the image providing the metadata query expression to each block or item.</span></span>

![Abbildung des JPEG-Bilds mit metadatenaufrufen](graphics/jpegwithcallouts.png)

<span data-ttu-id="ee962-163">Um eingebettete Metadatenblöcke oder bestimmte Elemente anhand des Namens abzufragen, müssen Sie die **GetMetadataByName** -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-163">To query for embedded metadata blocks or specific items by name, call the **GetMetadataByName** method.</span></span> <span data-ttu-id="ee962-164">Diese Methode nimmt einen Abfrage Ausdruck und eine [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) an, in der das Metadatenelement zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-164">This method takes a query expression and a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in which the metadata item is returned.</span></span> <span data-ttu-id="ee962-165">Der folgende Code fragt einen gruppierten Metadatenblock ab und konvertiert die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Komponente, die vom PROPVARIANT-Wert bereitgestellt wird, in einen Abfrage Reader, sofern gefunden.</span><span class="sxs-lookup"><span data-stu-id="ee962-165">The following code queries for a nested metadata block and converts the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) component provided by the PROPVARIANT value to a query reader if found.</span></span>


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="ee962-166">Der Abfrage Ausdruck "/App1/IFD" fragt den im App1-Block geblösteten IFD-Block ab.</span><span class="sxs-lookup"><span data-stu-id="ee962-166">The query expression "/app1/ifd" is querying for the IFD block nested in the App1 block.</span></span> <span data-ttu-id="ee962-167">Die JPEG-Bilddatei enthält den in der Tabelle eingefügten IFD-Metadatenblock, sodass die [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) mit einem Variablentyp (VT) von `VT_UNKNOWN` und einem Zeiger auf eine [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle (punkVal) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-167">The JPEG image file contains the IFD nested metadata block, so the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) is returned with a variable type (vt) of `VT_UNKNOWN` and a pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface (punkVal).</span></span> <span data-ttu-id="ee962-168">Anschließend Fragen Sie die IUnknown-Schnittstelle nach einem Abfrage Reader ab.</span><span class="sxs-lookup"><span data-stu-id="ee962-168">You then query the IUnknown interface for a query reader.</span></span>

<span data-ttu-id="ee962-169">Der folgende Code veranschaulicht eine neue Abfrage auf der Grundlage des neuen Abfrage Readers in Bezug auf den Block mit dem Block "IFD".</span><span class="sxs-lookup"><span data-stu-id="ee962-169">The following code demonstrates a new query based on the new query reader relative to the nested IFD block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="ee962-170">Der Abfrage Ausdruck "/{ushort = 18249}" fragt den IFD-Block für die microsoftphoto-Bewertung ab, die unter Tag 18249 eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="ee962-170">The query expression "/{ushort=18249}" queries the IFD block for the MicrosoftPhoto rating embedded under tag 18249.</span></span> <span data-ttu-id="ee962-171">Der [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Wert enthält jetzt den Werttyp `VT_UI2` und den Datenwert 50.</span><span class="sxs-lookup"><span data-stu-id="ee962-171">The [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will now contain a value type of `VT_UI2` and a data value of 50.</span></span>

<span data-ttu-id="ee962-172">Es ist jedoch nicht erforderlich, einen-Block zu erhalten, bevor bestimmte Datenwerte abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-172">However, it is not necessary to obtain a nested block before querying for specific data values.</span></span> <span data-ttu-id="ee962-173">Anstatt z. b. die geclusterte IFD und dann die microsoftphoto-Bewertung abzufragen, können Sie stattdessen den Block "root Metadata" und die im folgenden Code gezeigte Abfrage verwenden, um dieselben Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee962-173">For instance, instead of querying for the nested IFD and then for the MicrosoftPhoto rating, you can instead use the root metadata block and the query shown in the following code to obtain the same information.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



<span data-ttu-id="ee962-174">Zusätzlich zum Abfragen spezifischer Metadatenelemente in einem Metadatenblock können Sie auch alle Metadatenelemente in einem Metadatenblock auflisten (ohne Metadatenelemente in gruppierten metadatenblöcken).</span><span class="sxs-lookup"><span data-stu-id="ee962-174">In addition to querying for specific metadata items in a metadata block, you can also enumerate all the metadata items in a metadata block (not including metadata items in nested metadata blocks).</span></span> <span data-ttu-id="ee962-175">Um die Metadatenelemente im aktuellen Block aufzulisten, wird die **GetEnumeration** -Methode des Abfrage Readers verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee962-175">To enumerate the metadata items in the current block, the query reader's **GetEnumeration** method is used.</span></span> <span data-ttu-id="ee962-176">Diese Methode ruft eine **IEnumString** -Schnittstelle ab, die mit den Metadatenelementen im aktuellen Block gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ee962-176">This method obtains an **IEnumString** interface populated with the metadata items in the current block.</span></span> <span data-ttu-id="ee962-177">Der folgende Code listet z. b. die XMP-Bewertung und die microsoftphoto-Bewertung für den zuvor erhaltenen Block-IFD-Block auf.</span><span class="sxs-lookup"><span data-stu-id="ee962-177">For example, the following code enumerates the XMP rating and MicrosoftPhoto rating for the nested IFD block that was obtained earlier.</span></span>


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



<span data-ttu-id="ee962-178">Weitere Informationen zum Identifizieren geeigneter Tags für verschiedene Bildformate und Metadatenformate finden Sie unter [Metadatenabfragen für das Native Image](-wic-native-image-format-metadata-queries.md).</span><span class="sxs-lookup"><span data-stu-id="ee962-178">For more information on identifying appropriate tags for various image formats and metadata formats, see [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md).</span></span>

### <a name="additional-query-reader-methods"></a><span data-ttu-id="ee962-179">Zusätzliche Abfrage Reader-Methoden</span><span class="sxs-lookup"><span data-stu-id="ee962-179">Additional Query Reader Methods</span></span>

<span data-ttu-id="ee962-180">Zusätzlich zum Lesen von Metadaten können Sie auch zusätzliche Informationen über den Abfrage Leser abrufen und Metadaten auf andere Weise abrufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-180">In addition to reading metadata, you can also obtain additional information about the query reader and obtain metadata through other means.</span></span> <span data-ttu-id="ee962-181">Der Abfrage Reader stellt zwei Methoden bereit, die Informationen über den Abfrage Reader, **GetContainerFormat** und **getLocation** bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ee962-181">The query reader provides two methods that provide information about the query reader, **GetContainerFormat** and **GetLocation**.</span></span>

<span data-ttu-id="ee962-182">Mit dem eingebetteten Abfrage Reader können Sie **GetContainerFormat** verwenden, um den Typ des Metadatenblocks zu bestimmen, und Sie können **getLocation** aufrufen, um den Pfad relativ zum stammmetadatenblock abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-182">With the embedded query reader, you can use **GetContainerFormat** to determine the type of metadata block, and you can call **GetLocation** to obtain the path relative to the root metadata block.</span></span> <span data-ttu-id="ee962-183">Der folgende Code fragt den eingebetteten Abfrage Reader nach seinem Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="ee962-183">The following code queries the embedded query reader for its location.</span></span>


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



<span data-ttu-id="ee962-184">Der get-Befehl von **GetContainerFormat** für den eingebetteten Abfrage Reader gibt die GUID des IFD-metadatenformats zurück.</span><span class="sxs-lookup"><span data-stu-id="ee962-184">The call to **GetContainerFormat** for the embedded query reader returns the IFD metadata format GUID.</span></span> <span data-ttu-id="ee962-185">Der **getLocation** -Rückruf gibt einen Namespace von "/App1/IFD" zurück. Bereitstellen des relativen Pfads, von dem nachfolgende Abfragen für den neuen Abfrage Reader ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-185">The call to **GetLocation** returns a namespace of "/app1/ifd"; providing you with the relative path from which subsequent queries to the new query reader will be executed.</span></span> <span data-ttu-id="ee962-186">Der vorangehende Code ist natürlich nicht sehr nützlich, es wird jedoch veranschaulicht, wie die **getLocation** -Methode zum Suchen von geschposteten metadatenblöcken verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee962-186">Of course, the preceding code isn't very useful, but it does demonstrate how to use the **GetLocation** method for finding nested metadata blocks.</span></span>

## <a name="writing-metadata-using-a-query-writer"></a><span data-ttu-id="ee962-187">Schreiben von Metadaten mit einem Abfrage-Writer</span><span class="sxs-lookup"><span data-stu-id="ee962-187">Writing Metadata Using a Query Writer</span></span>

> [!Note]  
> <span data-ttu-id="ee962-188">Einige der in diesem Abschnitt bereitgestellten Codebeispiele werden im Kontext der eigentlichen Schritte, die zum Schreiben von Metadaten erforderlich sind, nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ee962-188">Some of the code examples provided in this section are not shown in the context of the actual steps required to write metadata.</span></span> <span data-ttu-id="ee962-189">Um die Codebeispiele im Kontext eines funktionierenden Beispiels anzuzeigen, finden Sie weitere Informationen unter Gewusst wie: Erneutes Codieren eines Bilds mit Metadaten.</span><span class="sxs-lookup"><span data-stu-id="ee962-189">To view the code examples in the context of a working sample, see the How-to: Re-encode an Image with Metadata tutorial.</span></span>

 

<span data-ttu-id="ee962-190">Die Hauptkomponente zum Schreiben von Metadaten ist der Abfrage-Writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="ee962-190">The main component for writing metadata is the query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span> <span data-ttu-id="ee962-191">Mit dem Query Writer können Sie Metadatenblöcke und Elemente innerhalb eines Metadatenblocks festlegen und entfernen.</span><span class="sxs-lookup"><span data-stu-id="ee962-191">The query writer enables you to set and remove metadata blocks and items within a metadata block.</span></span>

<span data-ttu-id="ee962-192">Ebenso wie der Abfrage Reader gibt es drei Möglichkeiten, einen Abfragewriter abzurufen: über einen Bitmap-Encoder ([**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), über seine einzelnen Frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) oder über einen schnellen metadatenencoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span><span class="sxs-lookup"><span data-stu-id="ee962-192">Like the query reader, there are three ways to obtain a query writer: through a bitmap encoder ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), through its individual frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)), or through a fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span></span>

### <a name="obtaining-a-query-writer"></a><span data-ttu-id="ee962-193">Abrufen eines Abfrage-Writers</span><span class="sxs-lookup"><span data-stu-id="ee962-193">Obtaining a Query Writer</span></span>

<span data-ttu-id="ee962-194">Der häufigste Abfrage-Writer ist für einen einzelnen Frame einer Bitmap.</span><span class="sxs-lookup"><span data-stu-id="ee962-194">The most common query writer is for an individual frame of a bitmap.</span></span> <span data-ttu-id="ee962-195">Dieser Abfrage-Writer legt die Metadatenblöcke und Elemente eines Bilds fest und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="ee962-195">This query writer sets and removes an image frame's metadata blocks and items.</span></span> <span data-ttu-id="ee962-196">Um den Abfrage-Writer eines Bild Frames abzurufen, rufen Sie die **GetMetadataQueryWriter** -Methode des Frames auf.</span><span class="sxs-lookup"><span data-stu-id="ee962-196">To obtain an image frame's query writer, call the frame's **GetMetadataQueryWriter** method.</span></span> <span data-ttu-id="ee962-197">Der folgende Code veranschaulicht den einfachen Methoden Aufrufzum Abrufen des Abfrage Writers eines Frames.</span><span class="sxs-lookup"><span data-stu-id="ee962-197">The following code demonstrates the simple method call to obtain a frame's query writer.</span></span>


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



<span data-ttu-id="ee962-198">Auf ähnliche Weise kann auch ein Abfrage-Writer für die Encoder-Ebene abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-198">Similarly, a query writer can also be obtained for the encoder level.</span></span> <span data-ttu-id="ee962-199">Ein einfacher Rückruf der **GetMetadataQueryWriter** -Methode des Encoders Ruft den Abfragewriter des Encoders ab.</span><span class="sxs-lookup"><span data-stu-id="ee962-199">A simple call to the encoder's **GetMetadataQueryWriter** method gets the encoder's query writer.</span></span> <span data-ttu-id="ee962-200">Im Gegensatz zum Abfrage-Writer eines Frames schreibt der Abfrage Schreiber eines Encoders Metadaten für ein Bild außerhalb des einzelnen Frames.</span><span class="sxs-lookup"><span data-stu-id="ee962-200">An encoder's query writer, unlike a frame's query writer, writes metadata for an image outside of the individual frame.</span></span> <span data-ttu-id="ee962-201">Dieses Szenario ist jedoch nicht üblich, und die nativen Image Formate unterstützen diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="ee962-201">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="ee962-202">Das systemeigene Bild, das von WIC bereitgestellt wird, dient zum Lesen und Schreiben von Metadaten auf Frame-Ebene, auch bei Einzel Frame Formaten wie JPEG.</span><span class="sxs-lookup"><span data-stu-id="ee962-202">The native image codecs provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

<span data-ttu-id="ee962-203">Sie können einen Abfrage-Writer auch direkt von der Imaging Factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)) abrufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-203">You can also obtain a query writer directly from the imaging factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span></span> <span data-ttu-id="ee962-204">Es gibt zwei Imaging Factory-Methoden, die einen Abfrage-Writer zurückgeben: " **kreatequerywriter** " und " **kreatequeryschreiterfromreader**".</span><span class="sxs-lookup"><span data-stu-id="ee962-204">There are two imaging factory methods that return a query writer: **CreateQueryWriter** and **CreateQueryWriterFromReader**.</span></span>

<span data-ttu-id="ee962-205">Mit " **anatequerywriter** " wird ein Abfrage Schreiber für das angegebene Metadatenformat und den angegebenen Anbieter erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee962-205">**CreateQueryWriter** creates a query writer for the specified metadata format and vendor.</span></span> <span data-ttu-id="ee962-206">Dieser Abfragewriter ermöglicht das Schreiben von Metadaten für ein bestimmtes Metadatenformat und das Hinzufügen zum Image.</span><span class="sxs-lookup"><span data-stu-id="ee962-206">This query writer enables you to write metadata for a specific metadata format and add it to the image.</span></span> <span data-ttu-id="ee962-207">Der folgende Code veranschaulicht einen " **anatequerywriter** "-Befehl zum Erstellen eines XMP-Abfrage-Writers.</span><span class="sxs-lookup"><span data-stu-id="ee962-207">The following code demonstrates a **CreateQueryWriter** call to create an XMP query writer.</span></span>


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



<span data-ttu-id="ee962-208">In diesem Beispiel wird der Anzeige Name `GUID_MetadataFormatXMP` als *guidMetadataFormat* -Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee962-208">In this example, the friendly name `GUID_MetadataFormatXMP` is used as the *guidMetadataFormat* parameter.</span></span> <span data-ttu-id="ee962-209">Sie stellt die GUID des XMP-metadatenformats dar, und der Hersteller stellt den von Microsoft erstellten Handler dar.</span><span class="sxs-lookup"><span data-stu-id="ee962-209">It represents the XMP metadata format GUID, and vendor represents the Microsoft created handler.</span></span> <span data-ttu-id="ee962-210">Alternativ kann **null** als *pguidVendor* -Parameter mit denselben Ergebnissen übergeben werden, wenn kein anderer XMP-Handler vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ee962-210">Alternatively, **NULL** can be passed as the *pguidVendor* parameter with the same results if no other XMP handler exists.</span></span> <span data-ttu-id="ee962-211">Wenn ein benutzerdefinierter XMP-Handler neben dem systemeigenen XMP-Handler installiert wird, führt das Übergeben von **null** für den Hersteller dazu, dass der Abfragewriter mit der niedrigsten GUID zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-211">If a custom XMP handler is installed alongside the native XMP handler, passing **NULL** for the vendor will result in the query writer with the lowest GUID being returned.</span></span>

<span data-ttu-id="ee962-212">" **Kreatequeryschreiterfromreader** " ähnelt der Methode " **kreatequerywriter** ", mit dem Unterschied, dass Sie den neuen Abfragewriter mit den vom Abfrage Reader bereitgestellten Daten vorab füllt.</span><span class="sxs-lookup"><span data-stu-id="ee962-212">**CreateQueryWriterFromReader** is similar to the **CreateQueryWriter** method except that it prepopulates the new query writer with the data provided by the query reader.</span></span> <span data-ttu-id="ee962-213">Dies ist nützlich für die erneute Codierung eines Bilds bei Beibehaltung der vorhandenen Metadaten oder zum Entfernen unerwünschter Metadaten.</span><span class="sxs-lookup"><span data-stu-id="ee962-213">This is useful for re-encoding an image while maintaining the existing metadata, or for removing unwanted metadata.</span></span> <span data-ttu-id="ee962-214">Der folgende Code veranschaulicht einen Befehl zum Aufrufen von " **exatequeryschreiterfromreader** ".</span><span class="sxs-lookup"><span data-stu-id="ee962-214">The following code demonstrates a **CreateQueryWriterFromReader** call.</span></span>


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a><span data-ttu-id="ee962-215">Hinzufügen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-215">Adding Metadata</span></span>

<span data-ttu-id="ee962-216">Nachdem Sie einen Abfrage-Writer erhalten haben, können Sie ihn verwenden, um Metadatenblöcke und Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ee962-216">After you obtain a query writer, you can use it to add metadata blocks and items.</span></span> <span data-ttu-id="ee962-217">Um Metadaten zu schreiben, verwenden Sie die **SetMetadataByName** -Methode des Abfrage-Writers.</span><span class="sxs-lookup"><span data-stu-id="ee962-217">To write metadata, you use the query writer's **SetMetadataByName** method.</span></span> <span data-ttu-id="ee962-218">**SetMetadataByName** nimmt zwei Parameter an: einen Abfrage Ausdruck (*wzName*) und einen Zeiger auf eine [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarvalue*).</span><span class="sxs-lookup"><span data-stu-id="ee962-218">**SetMetadataByName** takes two parameters: a query expression (*wzName*) and a pointer to a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span></span> <span data-ttu-id="ee962-219">Der Abfrage Ausdruck definiert den festzulegenden Block oder das Element, während die PROPVARIANT den tatsächlich festzulegenden Datenwert bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ee962-219">The query expression defines the block or item to set while the PROPVARIANT provides the actual data value to set.</span></span>

<span data-ttu-id="ee962-220">Das folgende Beispiel veranschaulicht das Hinzufügen eines Titels mithilfe des XMP-Abfrage-Writers, der zuvor mithilfe der Methode " **kreatequerywriter** " abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ee962-220">The following example demonstrates how to add a title by using the XMP query writer previously obtained by using the **CreateQueryWriter** method.</span></span>


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



<span data-ttu-id="ee962-221">In diesem Beispiel ist der Werttyp (VT) auf festgelegt `VT_LPWSTR` , was bedeutet, dass eine Zeichenfolge als Datenwert verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-221">In this example, value's type (vt) is set to `VT_LPWSTR`, indicating that a string will be used as the data value.</span></span> <span data-ttu-id="ee962-222">Da der *Werttyp* eine Zeichenfolge ist, wird *pwszval* verwendet, um den zu verwendenden Titel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ee962-222">Because *value*'s type is a string, *pwszVal* is used to set the title to use.</span></span> <span data-ttu-id="ee962-223">**SetMetadataByName** wird dann mit dem Abfrage Ausdruck ""/DC: Title "und der neu festgelegten [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-223">**SetMetadataByName** is then called using the query expression "/dc:title" and the newly set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="ee962-224">Der verwendete Abfrage Ausdruck gibt an, dass die Title-Eigenschaft im Schema der digitalen Kamera (DC) festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ee962-224">The query expression used indicates that the title property in the digital camera (dc) schema should be set.</span></span> <span data-ttu-id="ee962-225">Beachten Sie, dass der Ausdruck nicht "/XMP/DC: Title" ist; Dies liegt daran, dass der Abfrage Schreiber bereits für XMP spezifisch ist und keinen eingebetteten XMP-Block enthält, den "/XMP/DC: Title" vorschlagen würde.</span><span class="sxs-lookup"><span data-stu-id="ee962-225">Note that the expression is not "/xmp/dc:title"; this is because the query writer is already specific to XMP and does not contain an embedded XMP block, which "/xmp/dc:title" would suggest.</span></span>

<span data-ttu-id="ee962-226">Bis zu diesem Punkt haben Sie einem Bild Rahmen noch keine Metadaten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ee962-226">Up to this point you haven't actually added any metadata to an image frame.</span></span> <span data-ttu-id="ee962-227">Sie haben einfach einen Abfrage-Writer mit Daten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="ee962-227">You've simply populated a query writer with data.</span></span> <span data-ttu-id="ee962-228">Um einem Frame einen Metadatenblock hinzuzufügen, der durch den Abfrage-Writer dargestellt wird, wird **SetMetadataByName** erneut mit dem Abfrage-Writer als Wert der [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-228">To add to a frame a metadata block represented by the query writer, you again call **SetMetadataByName** using the query writer as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="ee962-229">Auf diese Weise werden die Metadaten im Abfrage-Writer in den Bildframe kopiert.</span><span class="sxs-lookup"><span data-stu-id="ee962-229">This effectively copies the metadata in the query writer to the image frame.</span></span> <span data-ttu-id="ee962-230">Der folgende Code veranschaulicht, wie Sie die Metadaten im XMP-Abfrage-Writer hinzufügen, die zuvor dem Stamm-Metadatenblock eines Frames abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="ee962-230">The following code demonstrates how to add the metadata in the XMP query writer previously obtained to a frame's root metadata block.</span></span>


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



<span data-ttu-id="ee962-231">In diesem Beispiel wird ein Werttyp (VT) von verwendet, der `VT_UNKOWN` einen COM-Schnittstellen Werttyp angibt.</span><span class="sxs-lookup"><span data-stu-id="ee962-231">In this example, a value type (vt) of `VT_UNKOWN` is used; indicating a COM interface value type.</span></span> <span data-ttu-id="ee962-232">Der XMP-Abfrage-Writer (pixmpwriter) wird dann als Wert für die [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)verwendet, und es wird mithilfe der adressf-Methode ein Verweis darauf hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ee962-232">The XMP query writer (piXMPWriter) is then used as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adding a reference to it by using the AddRef method.</span></span> <span data-ttu-id="ee962-233">Schließlich wird der XMP-Abfrage-Writer festgelegt, indem die **SetMetadataByName** -Methode des Frames aufgerufen und der Abfrage Ausdruck "/", der den Stamm Block angibt, und die neu festgelegte PROPVARIANT übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-233">Finally, the XMP query writer is set by calling the frame's **SetMetadataByName** method and passing the query expression "/", indicating the root block, and the newly set PROPVARIANT.</span></span>

> [!Note]  
> <span data-ttu-id="ee962-234">Wenn der Frame bereits den Metadatenblock enthält, den Sie hinzufügen möchten, werden die Metadaten hinzugefügt, die Sie hinzufügen, und vorhandene Metadaten werden überschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee962-234">If the frame already contains the metadata block you are trying to add, the metadata you are adding will be added and existing metadata overwritten.</span></span>

 

### <a name="removing-metadata"></a><span data-ttu-id="ee962-235">Entfernen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-235">Removing Metadata</span></span>

<span data-ttu-id="ee962-236">Mit einem Abfrage-Writer können Sie auch Metadaten entfernen, indem Sie die **RemoveMetadataByName** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-236">A query writer also enables you to remove metadata by calling the **RemoveMetadataByName** method.</span></span> <span data-ttu-id="ee962-237">**RemoveMetadataByName** nimmt einen Abfrage Ausdruck an und entfernt den Metadatenblock bzw. das Element, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ee962-237">**RemoveMetadataByName** takes a query expression and removes the metadata block or item if it exists.</span></span> <span data-ttu-id="ee962-238">Der folgende Code veranschaulicht, wie der zuvor hinzugefügte Titel entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-238">The following code demonstrates how to remove the title that was previously added.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



<span data-ttu-id="ee962-239">Der folgende Code veranschaulicht, wie der gesamte XMP-Metadatenblock entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-239">The following code demonstrates how to remove the entire XMP metadata block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a><span data-ttu-id="ee962-240">Kopieren von Metadaten für die erneute Codierung</span><span class="sxs-lookup"><span data-stu-id="ee962-240">Copying Metadata for Re-encoding</span></span>

> [!Note]  
> <span data-ttu-id="ee962-241">Der Code in diesem Abschnitt ist nur gültig, wenn die Quell-und Ziel Image Formate identisch sind.</span><span class="sxs-lookup"><span data-stu-id="ee962-241">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="ee962-242">Wenn Sie in ein anderes Bildformat codieren, können Sie nicht alle Metadaten eines Bilds in einem einzelnen Vorgang kopieren.</span><span class="sxs-lookup"><span data-stu-id="ee962-242">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="ee962-243">Zum Beibehalten von Metadaten beim erneuten Codieren eines Bilds in dasselbe Bildformat stehen Methoden zum Kopieren aller Metadaten in einem einzelnen Vorgang zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ee962-243">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="ee962-244">Jeder dieser Vorgänge folgt einem ähnlichen Muster: jede legt die Metadaten des decodierten Frames direkt in den neuen Frame fest, der codiert wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-244">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span>

<span data-ttu-id="ee962-245">Die bevorzugte Methode zum Kopieren von Metadaten besteht darin, den blockwriter des neuen Frames mit dem Block Reader des decodierten Frames zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="ee962-245">The preferred method to copy metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="ee962-246">Der folgende Code veranschaulicht diese Methode.</span><span class="sxs-lookup"><span data-stu-id="ee962-246">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



<span data-ttu-id="ee962-247">In diesem Beispiel werden der Block Reader und der blockwriter aus dem Quellframe bzw. dem Zielframe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-247">In this example, the block reader and the block writer are obtained from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="ee962-248">Der blockwriter wird dann vom Block Reader initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ee962-248">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="ee962-249">Dies initialisiert den Block Reader mit den vorab aufgefüllten Metadaten des Block Readers.</span><span class="sxs-lookup"><span data-stu-id="ee962-249">This initializes the block reader with the pre-populated metadata of the block reader.</span></span>

<span data-ttu-id="ee962-250">Eine andere Methode zum Kopieren von Metadaten besteht darin, den Metadatenblock zu schreiben, auf den der Abfrage Reader mit dem Abfrage Schreiber des Encoders verweist.</span><span class="sxs-lookup"><span data-stu-id="ee962-250">Another method to copy metadata is to write the metadata block referenced by the query reader using the encoder's query writer.</span></span> <span data-ttu-id="ee962-251">Der folgende Code veranschaulicht diese Methode.</span><span class="sxs-lookup"><span data-stu-id="ee962-251">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



<span data-ttu-id="ee962-252">Hier wird ein Abfrage Reader aus dem decodierten Frame abgerufen und dann als Eigenschafts Wert der [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) verwendet, wobei ein Werttyp auf VT Unknown festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="ee962-252">Here, a query reader is obtained from the decoded frame and then used as the property value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) with a value type set to VT\_UNKNOWN.</span></span> <span data-ttu-id="ee962-253">Der Abfragewriter für den Encoder wird abgerufen, und der Abfrage Ausdruck "/" wird verwendet, um die Metadaten im Stamm Navigationspfad festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ee962-253">The query writer for the encoder is obtained and the query expression "/" is used to set the metadata at the root navigation path.</span></span> <span data-ttu-id="ee962-254">Sie können diese Methode auch verwenden, wenn Sie gruppierten Metadatenblöcke festlegen, indem Sie den Abfrage Ausdruck an den gewünschten Speicherort anpassen.</span><span class="sxs-lookup"><span data-stu-id="ee962-254">You can also use this method when setting nested metadata blocks, by adjusting the query expression to the desired location.</span></span>

<span data-ttu-id="ee962-255">Auf ähnliche Weise können Sie einen Abfrage-Writer basierend auf dem Abfrage Reader des decodierten Frames erstellen, indem Sie die **Methode "Methode" von "** Image der Abbild Erstellung" verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee962-255">Similarly, you can create a query writer based on the decoded frame's query reader by using the imaging factory's **CreateQueryWriterFromReader** method.</span></span> <span data-ttu-id="ee962-256">Der in diesem Vorgang erstellte Abfrage-Writer wird mit den Metadaten aus dem Abfrage Leser aufgefüllt und kann dann im Frame festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-256">The query writer created in this operation will be prepopulated with the metadata from the query reader and can then be set in the frame.</span></span> <span data-ttu-id="ee962-257">Der folgende Code veranschaulicht den Kopiervorgang " **dedeequeryschreiterfromreader** ".</span><span class="sxs-lookup"><span data-stu-id="ee962-257">The following code demonstrates the **CreateQueryWriterFromReader** copy operation.</span></span>


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



<span data-ttu-id="ee962-258">Diese Methode verwendet einen separaten Abfrage-Writer, der auf den Daten des Abfrage Readers basiert.</span><span class="sxs-lookup"><span data-stu-id="ee962-258">This method uses a separate query writer is created that is based on the data of the query reader.</span></span> <span data-ttu-id="ee962-259">Dieser neue Abfragewriter wird dann im Frame festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee962-259">This new query writer then set in the frame.</span></span>

<span data-ttu-id="ee962-260">Diese Vorgänge zum Kopieren von Metadaten funktionieren nur, wenn die Quell-und Ziel Images das gleiche Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ee962-260">Again, these operations to copy metadata only work when the source and destination images have the same format.</span></span> <span data-ttu-id="ee962-261">Dies liegt daran, dass unterschiedliche Bildformate die Metadatenblöcke an verschiedenen Speicherorten speichern.</span><span class="sxs-lookup"><span data-stu-id="ee962-261">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="ee962-262">Beispielsweise unterstützen sowohl JPEG als auch TIFF XMP-Metadatenblöcke.</span><span class="sxs-lookup"><span data-stu-id="ee962-262">For instance, both JPEG and TIFF support XMP metadata blocks.</span></span> <span data-ttu-id="ee962-263">In JPEG-Bildern befindet sich der XMP-Block im stammmetadatenblock, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ee962-263">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="ee962-264">In einem TIFF-Bild ist der XMP-Block jedoch in einem IFD-Stammblock eingebettet.</span><span class="sxs-lookup"><span data-stu-id="ee962-264">However, in a TIFF image, the XMP block is nested in a root IFD block.</span></span> <span data-ttu-id="ee962-265">Das folgende Diagramm veranschaulicht die Unterschiede zwischen einem JPEG-Bild und einem TIFF-Bild mit denselben Bewertungs Metadaten.</span><span class="sxs-lookup"><span data-stu-id="ee962-265">The following diagram illustrates the differences between a JPEG image and a TIFF image with the same rating metadata.</span></span>

![Vergleich zwischen JPEG und TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a><span data-ttu-id="ee962-267">Schnelle metadatencodierung</span><span class="sxs-lookup"><span data-stu-id="ee962-267">Fast Metadata Encoding</span></span>

<span data-ttu-id="ee962-268">Es ist nicht immer erforderlich, ein Bild neu zu codieren, um neue Metadaten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ee962-268">It is not always necessary to re-encode an image to write new metadata to it.</span></span> <span data-ttu-id="ee962-269">Metadaten können auch mithilfe eines schnellen metadatenencoders geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-269">Metadata can also be written by using a fast metadata encoder.</span></span> <span data-ttu-id="ee962-270">Ein schneller metadatenencoder kann eine begrenzte Menge an Metadaten in ein Bild schreiben, ohne das Bild neu zu codieren.</span><span class="sxs-lookup"><span data-stu-id="ee962-270">A fast metadata encoder can write a limited amount of metadata to an image without re-encoding the image.</span></span> <span data-ttu-id="ee962-271">Dies erfolgt durch das Schreiben der neuen Metadaten innerhalb der leeren Auffüll Zeichen, die von einigen Metadatenformaten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-271">This is accomplished by writing the new metadata within the empty padding provided by some metadata formats.</span></span> <span data-ttu-id="ee962-272">Die nativen Metadatenformate, die die Auffüll Auffüll Vorgänge unterstützen, sind EXIF, IFD, GPS und XMP.</span><span class="sxs-lookup"><span data-stu-id="ee962-272">The native metadata formats that support metadata padding are Exif, IFD, GPS and XMP.</span></span>

### <a name="adding-padding-to-metadata-blocks"></a><span data-ttu-id="ee962-273">Hinzufügen von Padding zu metadatenblöcken</span><span class="sxs-lookup"><span data-stu-id="ee962-273">Adding Padding to Metadata Blocks</span></span>

<span data-ttu-id="ee962-274">Bevor Sie eine schnelle metadatencodierung durchführen können, muss im Metadatenblock Platz vorhanden sein, um weitere Metadaten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ee962-274">Before you can perform fast metadata encoding, there must be room within the metadata block to write more metadata.</span></span> <span data-ttu-id="ee962-275">Wenn nicht genügend Platz innerhalb der vorhandenen Auffüll Zeichen vorhanden ist, um die neuen Metadaten zu schreiben, schlägt die schnelle metadatencodierung fehl.</span><span class="sxs-lookup"><span data-stu-id="ee962-275">If there is not enough room within the existing padding to write the new metadata, the fast metadata encoding will fail.</span></span> <span data-ttu-id="ee962-276">Zum Hinzufügen von metadatenauffüllungen zu einem Bild muss das Bild erneut codiert werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-276">To add metadata padding to an image, the image must be re-encoded.</span></span> <span data-ttu-id="ee962-277">Sie können Auffüll Zeichen genauso wie jedes andere Metadatenelement hinzufügen, indem Sie einen Abfrage Ausdruck verwenden, wenn der Metadatenblock, den Sie auffüllen, ihn unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee962-277">You can add padding the same way you would add any other metadata item, by using a query expression, if the metadata block you are padding supports it.</span></span> <span data-ttu-id="ee962-278">Im folgenden Beispiel wird veranschaulicht, wie einem in einem App1-Block eingebetteten IFD-Block Auffüll Zeichen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-278">The following example demonstrates how to add padding to an IFD block embedded in an App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



<span data-ttu-id="ee962-279">Um Auffüll Zeichen hinzuzufügen, erstellen Sie eine PROPVARIANT vom Typ VT \_ UI4 und einen Wert, der der Anzahl der hinzu zufügenden Bytes von Auffüll Zeichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="ee962-279">To add padding, create a PROPVARIANT of type VT\_UI4 and a value corresponding to the number of bytes of padding to add.</span></span> <span data-ttu-id="ee962-280">Ein typischer Wert ist 4096 Bytes.</span><span class="sxs-lookup"><span data-stu-id="ee962-280">A typical value is 4096 bytes.</span></span> <span data-ttu-id="ee962-281">Die Metadatenabfragen für JPEG, TIFF und JPEG-XR befinden sich in dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ee962-281">The metadata queries for JPEG, TIFF, and JPEG-XR are in this table.</span></span>



| <span data-ttu-id="ee962-282">Metadatenformat</span><span class="sxs-lookup"><span data-stu-id="ee962-282">Metadata format</span></span> | <span data-ttu-id="ee962-283">JPEG-Metadatenabfrage</span><span class="sxs-lookup"><span data-stu-id="ee962-283">JPEG metadata query</span></span>                  | <span data-ttu-id="ee962-284">TIFF, JPEG-XR-Metadatenabfrage</span><span class="sxs-lookup"><span data-stu-id="ee962-284">TIFF, JPEG-XR metadata query</span></span>    |
|-----------------|--------------------------------------|---------------------------------|
| <span data-ttu-id="ee962-285">IFD</span><span class="sxs-lookup"><span data-stu-id="ee962-285">IFD</span></span>             | <span data-ttu-id="ee962-286">/App1/IFD/PaddingSchema: Padding</span><span class="sxs-lookup"><span data-stu-id="ee962-286">/app1/ifd/PaddingSchema:Padding</span></span>      | <span data-ttu-id="ee962-287">/IFD/PaddingSchema: Padding</span><span class="sxs-lookup"><span data-stu-id="ee962-287">/ifd/PaddingSchema:Padding</span></span>      |
| <span data-ttu-id="ee962-288">EXIF</span><span class="sxs-lookup"><span data-stu-id="ee962-288">EXIF</span></span>            | <span data-ttu-id="ee962-289">/App1/IFD/EXIF/PaddingSchema: Padding</span><span class="sxs-lookup"><span data-stu-id="ee962-289">/app1/ifd/exif/PaddingSchema:Padding</span></span> | <span data-ttu-id="ee962-290">/IFD/EXIF/PaddingSchema: Padding</span><span class="sxs-lookup"><span data-stu-id="ee962-290">/ifd/exif/PaddingSchema:Padding</span></span> |
| <span data-ttu-id="ee962-291">XMP</span><span class="sxs-lookup"><span data-stu-id="ee962-291">XMP</span></span>             | <span data-ttu-id="ee962-292">/XMP/PaddingSchema: Padding</span><span class="sxs-lookup"><span data-stu-id="ee962-292">/xmp/PaddingSchema:Padding</span></span>           | <span data-ttu-id="ee962-293">/IFD/XMP/PaddingSchema: Padding</span><span class="sxs-lookup"><span data-stu-id="ee962-293">/ifd/xmp/PaddingSchema:Padding</span></span>  |
| <span data-ttu-id="ee962-294">GPS</span><span class="sxs-lookup"><span data-stu-id="ee962-294">GPS</span></span>             | <span data-ttu-id="ee962-295">/App1/IFD/GPS/PaddingSchema: Padding</span><span class="sxs-lookup"><span data-stu-id="ee962-295">/app1/ifd/gps/PaddingSchema:Padding</span></span>  | <span data-ttu-id="ee962-296">/IFD/GPS/PaddingSchema: Padding</span><span class="sxs-lookup"><span data-stu-id="ee962-296">/ifd/gps/PaddingSchema:Padding</span></span>  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a><span data-ttu-id="ee962-297">Abrufen eines schnellen metadatenencoders</span><span class="sxs-lookup"><span data-stu-id="ee962-297">Obtaining a Fast Metadata Encoder</span></span>

<span data-ttu-id="ee962-298">Wenn Sie ein Bild mit metadatenauffüll Zeichen haben, kann ein schneller metadatenencoder mithilfe der Imaging Factory-Methoden **CreateFastMetadataEncoderFromDecoder** und **CreateFastMetadataEncoderFromFrameDecode** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-298">When you have an image with metadata padding, a fast metadata encoder can be obtained by using the imaging factory methods **CreateFastMetadataEncoderFromDecoder** and **CreateFastMetadataEncoderFromFrameDecode**.</span></span>

<span data-ttu-id="ee962-299">Wie der Name schon sagt, erstellt **CreateFastMetadataEncoderFromDecoder** einen schnellen metadatenencoder für Metadaten auf Decoder-Ebene.</span><span class="sxs-lookup"><span data-stu-id="ee962-299">As the name implies, **CreateFastMetadataEncoderFromDecoder** creates a fast metadata encoder for decoder-level metadata.</span></span> <span data-ttu-id="ee962-300">Die von WIC bereitgestellten systemeigenen Image Formate unterstützen keine Metadaten auf Decoder-Ebene, aber diese Methode wird für den Fall bereitgestellt, dass ein solches Bildformat in der Zukunft entwickelt wird.</span><span class="sxs-lookup"><span data-stu-id="ee962-300">The native image formats provided by WIC do not support decoder-level metadata but this method is provided in case such an image format is developed in the future.</span></span>

<span data-ttu-id="ee962-301">Das gängigste Szenario ist das Abrufen eines schnellen metadatenencoders aus einem Bildframe mithilfe von **CreateFastMetadataEncoderFromFrameDecode**.</span><span class="sxs-lookup"><span data-stu-id="ee962-301">The more common scenario is to obtain a fast metadata encoder from an image frame by using **CreateFastMetadataEncoderFromFrameDecode**.</span></span> <span data-ttu-id="ee962-302">Der folgende Code Ruft den schnellen metadatenencoder eines decodierten Frames ab und ändert den Bewertungs Wert im App1-Block.</span><span class="sxs-lookup"><span data-stu-id="ee962-302">The following code obtains a decoded frame's fast metadata encoder and changes the rating value in the App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a><span data-ttu-id="ee962-303">Verwenden des schnellen metadatenencoders</span><span class="sxs-lookup"><span data-stu-id="ee962-303">Using the Fast Metadata Encoder</span></span>

<span data-ttu-id="ee962-304">Aus dem schnellen metadatenencoder können Sie einen Abfragewriter abrufen.</span><span class="sxs-lookup"><span data-stu-id="ee962-304">From the fast metadata encoder, you can obtain a query writer.</span></span> <span data-ttu-id="ee962-305">Dies ermöglicht es Ihnen, Metadaten mithilfe eines Abfrage Ausdrucks zu schreiben, wie zuvor gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ee962-305">This enables you to write metadata by using a query expression as previously demonstrated.</span></span> <span data-ttu-id="ee962-306">Nachdem Metadaten im Abfrage-Writer festgelegt wurden, müssen Sie einen Commit für den schnellen metadatenencoder durchsetzen, um die Metadatenaktualisierung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ee962-306">After metadata has been set in the query writer, commit the fast metadata encoder to finalize the metadata update.</span></span> <span data-ttu-id="ee962-307">Der folgende Code veranschaulicht das Festlegen und Ausführen von Änderungen an Metadatenänderungen.</span><span class="sxs-lookup"><span data-stu-id="ee962-307">The following code demonstrates setting and committing the metadata changes</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



<span data-ttu-id="ee962-308">Wenn **Commit** aus irgendeinem Grund fehlschlägt, müssen Sie das Image erneut codieren, um sicherzustellen, dass die neuen Metadaten dem Image hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ee962-308">If **Commit** fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee962-309">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee962-309">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ee962-310">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ee962-310">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee962-311">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="ee962-311">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ee962-312">Übersicht über WIC-Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-312">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="ee962-313">Übersicht über die Metadaten-Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="ee962-313">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="ee962-314">Übersicht über die metadatenerweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="ee962-314">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="ee962-315">Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee962-315">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
