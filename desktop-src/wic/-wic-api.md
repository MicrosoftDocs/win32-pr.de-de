---
description: Die Windows Imaging Component (WIC) stellt eine Component Object Model (com)-basierte API für die Verwendung in C und C++ bereit.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: WIC-API-Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368815"
---
# <a name="wic-api-overview"></a><span data-ttu-id="35bda-103">WIC-API-Übersicht</span><span class="sxs-lookup"><span data-stu-id="35bda-103">WIC API Overview</span></span>

<span data-ttu-id="35bda-104">Die Windows Imaging Component (WIC) stellt eine Component Object Model (com)-basierte API für die Verwendung in C und C++ bereit.</span><span class="sxs-lookup"><span data-stu-id="35bda-104">The Windows Imaging Component (WIC) provides a Component Object Model (COM) based API for use in C and C++.</span></span> <span data-ttu-id="35bda-105">Die WIC-API bietet eine Vielzahl von Bild bezogenen Funktionen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="35bda-105">The WIC API exposes a variety of image-related functionality, including:</span></span>

-   <span data-ttu-id="35bda-106">Integrierte Codecs für die Standardweb Bildformate.</span><span class="sxs-lookup"><span data-stu-id="35bda-106">Built-in codecs for the standard web image formats.</span></span>
-   <span data-ttu-id="35bda-107">Integrierte Unterstützung für standardmetadatenformate.</span><span class="sxs-lookup"><span data-stu-id="35bda-107">Built-in support for standard metadata formats.</span></span>
-   <span data-ttu-id="35bda-108">Unterstützung für eine breite Palette an Pixel Formaten.</span><span class="sxs-lookup"><span data-stu-id="35bda-108">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="35bda-109">Unterstützung für hohe Farben; Dazu zählen der erweiterte 30-Bit-Bereich, die 30-Bit-Genauigkeit mit hoher Genauigkeit und 48-Bit-Pixel Formate mit hoher Genauigkeit und Breite.</span><span class="sxs-lookup"><span data-stu-id="35bda-109">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="35bda-110">Erweiterbares Framework für Bild Codecs, Pixel Formate und Metadatenformate.</span><span class="sxs-lookup"><span data-stu-id="35bda-110">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>

<span data-ttu-id="35bda-111">Dieses Thema enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="35bda-111">This topic contains the following topics.</span></span>

-   [<span data-ttu-id="35bda-112">WIC-Header Dateien</span><span class="sxs-lookup"><span data-stu-id="35bda-112">WIC Header Files</span></span>](#wic-header-files)
-   [<span data-ttu-id="35bda-113">Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="35bda-113">Library Files</span></span>](#library-files)
-   [<span data-ttu-id="35bda-114">Klassenfactory</span><span class="sxs-lookup"><span data-stu-id="35bda-114">Class Factories</span></span>](#class-factories)
-   [<span data-ttu-id="35bda-115">Bildverarbeitungskomponenten</span><span class="sxs-lookup"><span data-stu-id="35bda-115">Imaging Components</span></span>](#imaging-components)
-   [<span data-ttu-id="35bda-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35bda-116">See Also</span></span>](#see-also)

## <a name="wic-header-files"></a><span data-ttu-id="35bda-117">WIC-Header Dateien</span><span class="sxs-lookup"><span data-stu-id="35bda-117">WIC Header Files</span></span>

<span data-ttu-id="35bda-118">Die WIC-APIs werden in den folgenden Header-und IDL-Dateien (Interface Definition Language) definiert:</span><span class="sxs-lookup"><span data-stu-id="35bda-118">The WIC APIs are defined in the following header and Interface Definition Language (IDL) files:</span></span>



| <span data-ttu-id="35bda-119">Datei</span><span class="sxs-lookup"><span data-stu-id="35bda-119">File</span></span>              | <span data-ttu-id="35bda-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35bda-120">Description</span></span>                                          |
|-------------------|------------------------------------------------------|
| <span data-ttu-id="35bda-121">wincodec. h</span><span class="sxs-lookup"><span data-stu-id="35bda-121">wincodec.h</span></span>        | <span data-ttu-id="35bda-122">Definiert die C-und C++-Versionen der primären WIC-APIs.</span><span class="sxs-lookup"><span data-stu-id="35bda-122">Defines C and C++ versions of the primary WIC APIs.</span></span>  |
| <span data-ttu-id="35bda-123">wincodec. idl</span><span class="sxs-lookup"><span data-stu-id="35bda-123">wincodec.idl</span></span>      | <span data-ttu-id="35bda-124">Definiert die primären WIC-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="35bda-124">Defines the primary WIC interfaces.</span></span>                  |
| <span data-ttu-id="35bda-125">wincodecsdk. h</span><span class="sxs-lookup"><span data-stu-id="35bda-125">wincodecsdk.h</span></span>     | <span data-ttu-id="35bda-126">Definiert die C-und C++-Versionen der Metadaten-WIC-APIs.</span><span class="sxs-lookup"><span data-stu-id="35bda-126">Defines C and C++ versions of the metadata WIC APIs.</span></span> |
| <span data-ttu-id="35bda-127">wincodecsdk. idl</span><span class="sxs-lookup"><span data-stu-id="35bda-127">wincodecsdk.idl</span></span>   | <span data-ttu-id="35bda-128">Definiert die WIC-Metadatenschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="35bda-128">Defines the WIC metadata interfaces.</span></span>                 |
| <span data-ttu-id="35bda-129">wincodec- \_ Proxy. h</span><span class="sxs-lookup"><span data-stu-id="35bda-129">wincodec\_proxy.h</span></span> | <span data-ttu-id="35bda-130">Definiert die WIC-Proxy Exporte.</span><span class="sxs-lookup"><span data-stu-id="35bda-130">Defines the WIC proxy exports.</span></span>                       |



 

<span data-ttu-id="35bda-131">Um WIC verwenden zu können, müssen Ihre Anwendungen abhängig von der API, die Ihre Anwendung benötigt, wincodec. h und/oder wincodecsdk. h einschließen.</span><span class="sxs-lookup"><span data-stu-id="35bda-131">To use WIC, your applications must include wincodec.h and/or wincodecsdk.h, depending on the API your application needs.</span></span>

## <a name="library-files"></a><span data-ttu-id="35bda-132">Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="35bda-132">Library Files</span></span>

<span data-ttu-id="35bda-133">Die WIC-Bibliotheksdateien:</span><span class="sxs-lookup"><span data-stu-id="35bda-133">The WIC library files:</span></span>



| <span data-ttu-id="35bda-134">Datei</span><span class="sxs-lookup"><span data-stu-id="35bda-134">File</span></span>              | <span data-ttu-id="35bda-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35bda-135">Description</span></span>                                                            |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="35bda-136">windowscodebug. lib</span><span class="sxs-lookup"><span data-stu-id="35bda-136">windowscodecs.lib</span></span> | <span data-ttu-id="35bda-137">Import Bibliothek, die vom Windows Software Development Kit (SDK) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="35bda-137">Import library provided by the Windows Software Development Kit (SDK).</span></span> |
| <span data-ttu-id="35bda-138">windowscodecs.dll</span><span class="sxs-lookup"><span data-stu-id="35bda-138">windowscodecs.dll</span></span> | <span data-ttu-id="35bda-139">Vom Betriebssystem bereitgestellte Bestands Implementierungs Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="35bda-139">Stock implementation library provided by the operating system.</span></span>         |



 

<span data-ttu-id="35bda-140">Um einen Link zu WIC-APIs zu erhalten, muss Ihre Anwendung windowscodec. lib als zusätzliche Linker-Abhängigkeit einschließen.</span><span class="sxs-lookup"><span data-stu-id="35bda-140">To link to WIC APIs, your application must include windowscodec.lib as an additional linker dependency.</span></span>

## <a name="class-factories"></a><span data-ttu-id="35bda-141">Klassenfactory</span><span class="sxs-lookup"><span data-stu-id="35bda-141">Class Factories</span></span>

<span data-ttu-id="35bda-142">In der folgenden Tabelle werden die beiden com-Klassenfactorys beschrieben, die die WIC-APIs zum Erstellen von WIC-</span><span class="sxs-lookup"><span data-stu-id="35bda-142">The following table describes the two COM class factories the WIC APIs provide for creating WIC components.</span></span>



| <span data-ttu-id="35bda-143">Factory-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="35bda-143">Factory Interface</span></span>                                               | <span data-ttu-id="35bda-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35bda-144">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35bda-145">**IWICImagingFactory**</span><span class="sxs-lookup"><span data-stu-id="35bda-145">**IWICImagingFactory**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | <span data-ttu-id="35bda-146">Primäre Klassenfactory für die Anwendungsentwicklung mit WIC-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="35bda-146">Primary class factory for application development using WIC components.</span></span> <span data-ttu-id="35bda-147">Diese Factory erstellt Komponenten, z. b. Image-Decoders, Encoder und Streams.</span><span class="sxs-lookup"><span data-stu-id="35bda-147">This factory creates components such as image decoders, encoders and streams.</span></span>   |
| [<span data-ttu-id="35bda-148">**IWICComponentFactory**</span><span class="sxs-lookup"><span data-stu-id="35bda-148">**IWICComponentFactory**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | <span data-ttu-id="35bda-149">Klassenfactory, die für WIC-Komponenten Entwickler konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="35bda-149">Class factory targeted for WIC component developers.</span></span> <span data-ttu-id="35bda-150">Komponenten, die aus dieser Factory erstellt werden, werden primär in der Codec-und metadatenhandlerentwicklung verwendet</span><span class="sxs-lookup"><span data-stu-id="35bda-150">Components created from this factory are primarily used in codec and metadata handler development.</span></span> |



 

<span data-ttu-id="35bda-151">Verwenden Sie die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -com-Funktion, um entweder eine Klassenfactory zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35bda-151">To create either class factory, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="35bda-152">Im folgenden Beispiel wird die Erstellung der WIC Imaging Factory veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="35bda-152">The following example demonstrates the creation of the WIC imaging factory.</span></span>


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a><span data-ttu-id="35bda-153">Bildverarbeitungskomponenten</span><span class="sxs-lookup"><span data-stu-id="35bda-153">Imaging Components</span></span>

<span data-ttu-id="35bda-154">Die WIC-APIs stellen verschiedene Arten von Abbild Erstellungs Komponenten bereit.</span><span class="sxs-lookup"><span data-stu-id="35bda-154">The WIC APIs provide several types of imaging components.</span></span> <span data-ttu-id="35bda-155">In der folgenden Tabelle werden einige der gängigen WIC-Komponenten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="35bda-155">The following table describes some of the common WIC components.</span></span> <span data-ttu-id="35bda-156">Eine vollständige Liste der verfügbaren Komponenten finden Sie unter [WIC-Schnittstellen](-wic-codec-ifaces.md).</span><span class="sxs-lookup"><span data-stu-id="35bda-156">For a full list of available components, see [WIC interfaces](-wic-codec-ifaces.md).</span></span>



| <span data-ttu-id="35bda-157">Komponententyp</span><span class="sxs-lookup"><span data-stu-id="35bda-157">Component Type</span></span>                                                      | <span data-ttu-id="35bda-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35bda-158">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35bda-159">**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="35bda-159">**Bitmap**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | <span data-ttu-id="35bda-160">Stellt eine beschreibbare Darstellung im Arbeitsspeicher einer [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)dar.</span><span class="sxs-lookup"><span data-stu-id="35bda-160">Represents a writable in-memory representation of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span></span> |
| [<span data-ttu-id="35bda-161">**Decoder**</span><span class="sxs-lookup"><span data-stu-id="35bda-161">**Decoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | <span data-ttu-id="35bda-162">Wird zum Decodieren von Bilddaten aus einem Stream in ein Format verwendet, das für die Bildverarbeitung nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="35bda-162">Used to decode image data from a stream into a format that is useful for image processing.</span></span>                    |
| [<span data-ttu-id="35bda-163">**ASA**</span><span class="sxs-lookup"><span data-stu-id="35bda-163">**Encoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | <span data-ttu-id="35bda-164">Schreibt Bilddaten in einen Stream.</span><span class="sxs-lookup"><span data-stu-id="35bda-164">Writes image data to a stream.</span></span>                                                                                |
| [<span data-ttu-id="35bda-165">**Datenstrom**</span><span class="sxs-lookup"><span data-stu-id="35bda-165">**Stream**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | <span data-ttu-id="35bda-166">Wird verwendet, um Daten aus einer Datei, einer Netzwerkressource, einem Speicherblock usw. zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="35bda-166">Used to read and write data from a file, network resource, a block of memory, and so on.</span></span>                      |
| [<span data-ttu-id="35bda-167">**Format Konverter**</span><span class="sxs-lookup"><span data-stu-id="35bda-167">**Format Converter**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | <span data-ttu-id="35bda-168">Wird verwendet, um ein Pixel Format in ein anderes zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="35bda-168">Used to convert from one pixel format to another.</span></span>                                                             |
| [<span data-ttu-id="35bda-169">**Metadatenabfrage-Reader**</span><span class="sxs-lookup"><span data-stu-id="35bda-169">**Metadata Query Reader**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | <span data-ttu-id="35bda-170">Wird zum Lesen von Metadaten eines Bilds oder Bilds verwendet.</span><span class="sxs-lookup"><span data-stu-id="35bda-170">Used to read metadata of an image or image frame.</span></span>                                                             |
| [<span data-ttu-id="35bda-171">**Metadatenabfrage-Writer**</span><span class="sxs-lookup"><span data-stu-id="35bda-171">**Metadata Query Writer**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | <span data-ttu-id="35bda-172">Wird verwendet, um Metadaten in einen Bild-oder Bild Rahmen zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="35bda-172">Used to write metadata to an image or image frame.</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="35bda-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35bda-173">See Also</span></span>

[<span data-ttu-id="35bda-174">Referenzen</span><span class="sxs-lookup"><span data-stu-id="35bda-174">References</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="35bda-175">Beispiele und Code Beispiele</span><span class="sxs-lookup"><span data-stu-id="35bda-175">Samples and Code Examples</span></span>](-wic-samples.md)


 

 
