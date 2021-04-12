---
description: In diesem Thema werden die Anforderungen für das Erstellen von benutzerdefinierten metadatenhandlern für die Windows Imaging Component (WIC) vorgestellt, einschließlich der Metadaten-Reader und Writer.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Übersicht über die metadatenerweiterbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216819"
---
# <a name="metadata-extensibility-overview"></a><span data-ttu-id="9e49a-103">Übersicht über die metadatenerweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="9e49a-103">Metadata Extensibility Overview</span></span>

<span data-ttu-id="9e49a-104">In diesem Thema werden die Anforderungen für das Erstellen von benutzerdefinierten metadatenhandlern für die Windows Imaging Component (WIC) vorgestellt, einschließlich der Metadaten-Reader und Writer.</span><span class="sxs-lookup"><span data-stu-id="9e49a-104">This topic introduces the requirements for creating custom metadata handlers for the Windows Imaging Component (WIC), including both metadata readers and writers.</span></span> <span data-ttu-id="9e49a-105">Außerdem werden die Anforderungen für die Erweiterung der WIC-Laufzeitkomponenten Ermittlung erläutert, um Ihre benutzerdefinierten Metadatenhandler einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-105">It also discusses the requirements for extending WIC run-time component discovery to include your custom metadata handlers.</span></span>

<span data-ttu-id="9e49a-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="9e49a-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9e49a-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9e49a-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="9e49a-108">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="9e49a-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="9e49a-109">Erstellen eines metadatenreaders</span><span class="sxs-lookup"><span data-stu-id="9e49a-109">Creating a Metadata Reader</span></span>](#creating-a-metadata-reader)
    -   [<span data-ttu-id="9e49a-110">IWICMetadataReader-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-110">IWICMetadataReader Interface</span></span>](#iwicmetadatareader-interface)
    -   [<span data-ttu-id="9e49a-111">IWICPersistStream-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-111">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="9e49a-112">Iwicstreamprovider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-112">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="9e49a-113">Erstellen eines metadatenwriters</span><span class="sxs-lookup"><span data-stu-id="9e49a-113">Creating a Metadata Writer</span></span>](#creating-a-metadata-writer)
    -   [<span data-ttu-id="9e49a-114">IWICMetadataWriter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-114">IWICMetadataWriter Interface</span></span>](#iwicmetadatawriter-interface)
    -   [<span data-ttu-id="9e49a-115">IWICPersistStream-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-115">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="9e49a-116">Iwicstreamprovider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-116">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="9e49a-117">Installieren und Registrieren eines metadatenhandlers</span><span class="sxs-lookup"><span data-stu-id="9e49a-117">Installing and Registering a Metadata Handler</span></span>](#installing-and-registering-a-metadata-handler)
    -   [<span data-ttu-id="9e49a-118">Metadatenhandler-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="9e49a-118">Metadata Handler Registry Keys</span></span>](#metadata-handler-registry-keys)
    -   [<span data-ttu-id="9e49a-119">Metadatenleser</span><span class="sxs-lookup"><span data-stu-id="9e49a-119">Metadata Readers</span></span>](#metadata-readers)
    -   [<span data-ttu-id="9e49a-120">Metadatenschreiber</span><span class="sxs-lookup"><span data-stu-id="9e49a-120">Metadata Writers</span></span>](#metadata-writers)
    -   [<span data-ttu-id="9e49a-121">Signieren eines metadatenhandlers</span><span class="sxs-lookup"><span data-stu-id="9e49a-121">Signing a Metadata Handler</span></span>](#signing-a-metadata-handler)
-   [<span data-ttu-id="9e49a-122">Besondere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="9e49a-122">Special Considerations</span></span>](#special-considerations)
    -   [<span data-ttu-id="9e49a-123">Propvarianten</span><span class="sxs-lookup"><span data-stu-id="9e49a-123">PROPVARIANTS</span></span>](#propvariants)
    -   [<span data-ttu-id="9e49a-124">8bim-Handler</span><span class="sxs-lookup"><span data-stu-id="9e49a-124">8BIM Handlers</span></span>](#8bim-handlers)
-   [<span data-ttu-id="9e49a-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e49a-125">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="9e49a-126">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9e49a-126">Prerequisites</span></span>

<span data-ttu-id="9e49a-127">Um dieses Thema zu verstehen, sollten Sie über ein tiefgreifendes Verständnis von WIC, seinen Komponenten und Metadaten für Images verfügen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-127">To understand this topic you should have an in-depth understanding of WIC, its components, and metadata for images.</span></span> <span data-ttu-id="9e49a-128">Weitere Informationen zu WIC-Metadaten finden Sie in der [WIC-Metadatenübersicht](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="9e49a-128">For more information on WIC metadata, see the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="9e49a-129">Weitere Informationen zu WIC-Komponenten finden Sie unter [Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="9e49a-129">For more information on WIC components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="9e49a-130">Einführung</span><span class="sxs-lookup"><span data-stu-id="9e49a-130">Introduction</span></span>

<span data-ttu-id="9e49a-131">Wie in der [Übersicht über WIC-Metadaten](-wic-about-metadata.md)erläutert, gibt es häufig mehrere Metadatenblöcke innerhalb eines Bilds, von denen jedes verschiedene Informationstypen in verschiedenen Metadatenformaten verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9e49a-131">As discussed in the [WIC Metadata Overview](-wic-about-metadata.md), there are often multiple blocks of metadata within an image, each exposing different types of information in different metadata formats.</span></span> <span data-ttu-id="9e49a-132">Um mit einem in einem Bild eingebetteten Metadatenformat zu interagieren, muss eine Anwendung einen geeigneten Metadatenhandler verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-132">To interact with a metadata format embedded within an image, an application must use an appropriate metadata handler.</span></span> <span data-ttu-id="9e49a-133">WIC stellt mehrere Metadatenhandler (sowohl metadatenreader als auch Writer) bereit, die es Ihnen ermöglichen, bestimmte Metadatentypen wie EXIF oder XMP zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="9e49a-133">WIC provides several metadata handlers (both metadata readers and writers) that enable you to read and write specific types of metadata such as Exif or XMP.</span></span>

<span data-ttu-id="9e49a-134">Zusätzlich zu den bereitgestellten systemeigenen Handlern bietet WIC APIs, mit denen Sie neue Metadatenhandler erstellen können, die an der WIC-Laufzeitkomponenten Ermittlung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="9e49a-134">In addition to the native handlers provided, WIC provides APIs that enable you to create new metadata handlers that participate in WIC's run-time component discovery.</span></span> <span data-ttu-id="9e49a-135">Dadurch können Anwendungen, die WIC verwenden, Ihre benutzerdefinierten Metadatenformate lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="9e49a-135">This enables applications that use WIC to read and write your custom metadata formats.</span></span>

<span data-ttu-id="9e49a-136">Die folgenden Schritte ermöglichen es ihren metadatenhandlern, an der Ermittlung der Lauf Zeit Metadaten von WIC teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-136">The following steps enable your metadata handlers to participate in WIC's run-time metadata discovery.</span></span>

-   <span data-ttu-id="9e49a-137">Implementieren Sie eine metadatenleser-Handlerklasse ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)), die die erforderlichen WIC-Schnittstellen zum Lesen des benutzerdefinierten metadatenformats verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9e49a-137">Implement a metadata-reader handler class ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) that exposes the required WIC interfaces for reading your custom metadata format.</span></span> <span data-ttu-id="9e49a-138">Dadurch können WIC-basierte Anwendungen ihr Metadatenformat auf die gleiche Weise wie Native Metadatenformate lesen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-138">This enables WIC-based applications to read your metadata format the same way they read native metadata formats.</span></span>
-   <span data-ttu-id="9e49a-139">Implementieren Sie eine metadatenwriter-Handlerklasse ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)), die die erforderlichen WIC-Schnittstellen für die Codierung Ihres benutzerdefinierten metadatenformats verfügbar macht</span><span class="sxs-lookup"><span data-stu-id="9e49a-139">Implement a metadata-writer handler class ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) that exposes the required WIC interfaces for encoding your custom metadata format.</span></span> <span data-ttu-id="9e49a-140">Dies ermöglicht es WIC-basierten Anwendungen, Ihr Metadatenformat in Unterstützte Bildformate zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-140">This enables WIC-based applications to serialize your metadata format into supported image formats.</span></span>
-   <span data-ttu-id="9e49a-141">Signieren Sie Ihre Metadatenhandler Digital, und registrieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="9e49a-141">Digitally sign and register your metadata handlers.</span></span> <span data-ttu-id="9e49a-142">Dadurch können Ihre Metadatenhandler zur Laufzeit ermittelt werden, indem das identifizierende Muster in der Registrierung mit dem in die Bilddatei eingebetteten Muster übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9e49a-142">This enables your metadata handlers to be discovered at run time by matching the identifying pattern in the registry with the pattern embedded in the image file.</span></span>

## <a name="creating-a-metadata-reader"></a><span data-ttu-id="9e49a-143">Erstellen eines metadatenreaders</span><span class="sxs-lookup"><span data-stu-id="9e49a-143">Creating a Metadata Reader</span></span>

<span data-ttu-id="9e49a-144">Der Haupt Zugriff auf Metadatenblöcke innerhalb eines Codecs ist die [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Schnittstelle, die von jedem WIC-Codec implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="9e49a-144">The main access to metadata blocks within a codec is through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface that each WIC codec implements.</span></span> <span data-ttu-id="9e49a-145">Diese Schnittstelle listet jeden der in ein Bildformat eingebetteten Metadatenblöcke auf, sodass der geeignete Metadatenhandler für jeden Block ermittelt und instanziiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e49a-145">This interface enumerates each of the metadata blocks embedded in an image format so that the appropriate metadata handler can be discovered and instantiated for each block.</span></span> <span data-ttu-id="9e49a-146">Die Metadatenblöcke, die nicht von WIC erkannt werden, gelten als unbekannt und sind als GUID CLSID \_ WICUnknownMetadataReader definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-146">The metadata blocks that are not recognized by WIC are considered unknown and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="9e49a-147">Damit Ihr Metadatenformat von WIC erkannt wird, müssen Sie eine Klasse erstellen, die drei Schnittstellen implementiert: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)und [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="9e49a-147">To have your metadata format recognized by WIC, you must create a class that implements three interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="9e49a-148">Wenn Ihr Metadatenformat Einschränkungen aufweist, die einige Methoden der erforderlichen Schnittstellen ungeeignet sind, sollte diese Methode wincodec \_ Err \_ unsupportedoperation zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9e49a-148">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatareader-interface"></a><span data-ttu-id="9e49a-149">IWICMetadataReader-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-149">IWICMetadataReader Interface</span></span>

<span data-ttu-id="9e49a-150">Die [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) -Schnittstelle muss beim Erstellen eines metadatenreaders implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-150">The [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) interface must be implemented when creating a metadata reader.</span></span> <span data-ttu-id="9e49a-151">Diese Schnittstelle ermöglicht den Zugriff auf die zugrunde liegenden Metadatenelemente innerhalb des Datenstroms eines metadatenformats.</span><span class="sxs-lookup"><span data-stu-id="9e49a-151">This interface provides access to the underling metadata items within the data stream of a metadata format.</span></span>

<span data-ttu-id="9e49a-152">Der folgende Code zeigt die Definition der metadatenleseschnittstelle, wie in der Datei wincodecsdk. idl definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-152">The following code shows the definition of the metadata reader interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

<span data-ttu-id="9e49a-153">Die **GetMetadataFormat** -Methode gibt die GUID Ihres metadatenformats zurück.</span><span class="sxs-lookup"><span data-stu-id="9e49a-153">The **GetMetadataFormat** method returns the GUID of your metadata format.</span></span>

<span data-ttu-id="9e49a-154">Die **GetMetadataHandlerInfo** -Methode gibt eine [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) -Schnittstelle zurück, die Informationen über Ihren Metadatenhandler bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9e49a-154">The **GetMetadataHandlerInfo** method returns an [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) interface that provides information about your metadata handler.</span></span> <span data-ttu-id="9e49a-155">Hierzu gehören Informationen wie z. b. Welche Bildformate das Metadatenformat unterstützen und ob Ihr metadatenleser Zugriff auf den vollständigen Metadatenstream benötigt.</span><span class="sxs-lookup"><span data-stu-id="9e49a-155">This includes information such as what image formats support the metadata format and whether your metadata reader requires access to the full metadata stream.</span></span>

<span data-ttu-id="9e49a-156">Die **GetCount** -Methode gibt die Anzahl einzelner Metadatenelemente (einschließlich eingebetteter Metadatenblöcke) zurück, die im Metadatenstream enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9e49a-156">The **GetCount** method returns the number of individual metadata items (including embedded metadata blocks) found within the metadata stream.</span></span>

<span data-ttu-id="9e49a-157">Die **getvaluebyindex** -Methode gibt ein Metadatenelement durch einen Indexwert zurück.</span><span class="sxs-lookup"><span data-stu-id="9e49a-157">The **GetValueByIndex** method returns a metadata item by an index value.</span></span> <span data-ttu-id="9e49a-158">Diese Methode ermöglicht es Anwendungen, jedes Metadatenelement in einem Metadatenblock zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-158">This method enables applications to loop through each metadata item in a metadata block.</span></span> <span data-ttu-id="9e49a-159">Der folgende Code veranschaulicht, wie eine Anwendung diese Methode verwenden kann, um jedes Metadatenelement in einem Metadatenblock abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-159">The following code demonstrates how an application can use this method to retrieve each metadata item in a metadata block.</span></span>


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



<span data-ttu-id="9e49a-160">Die **GetValue** -Methode ruft ein bestimmtes Metadatenelement nach Schema und/oder ID ab.</span><span class="sxs-lookup"><span data-stu-id="9e49a-160">The **GetValue** method retrieves a specific metadata item by schema and/or ID.</span></span> <span data-ttu-id="9e49a-161">Diese Methode ähnelt der **getvaluebyindex** -Methode, mit der Ausnahme, dass Sie ein Metadatenelement mit einem bestimmten Schema oder einer ID abruft.</span><span class="sxs-lookup"><span data-stu-id="9e49a-161">This method is similar to the **GetValueByIndex** method except that it retrieves a metadata item that has a specific schema or ID.</span></span>

<span data-ttu-id="9e49a-162">Die **GetEnumerator** -Methode gibt einen Enumerator für jedes Metadatenelement im Metadatenblock zurück.</span><span class="sxs-lookup"><span data-stu-id="9e49a-162">The **GetEnumerator** method returns an enumerator of each metadata item in the metadata block.</span></span> <span data-ttu-id="9e49a-163">Dadurch können Anwendungen einen Enumerator für die Navigation in Ihrem Metadatenformat verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-163">This enables applications to use an enumerator to navigate your metadata format.</span></span>

<span data-ttu-id="9e49a-164">Wenn Ihr Metadatenformat keine Schemas für Metadatenelemente enthält, wird der GetValue... Methoden sollten diese Eigenschaft ignorieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-164">If your metadata format does not have a notion of schemas for metadata items, the GetValue... methods should ignore this property.</span></span> <span data-ttu-id="9e49a-165">Wenn Ihr Format jedoch Schema Benennung unterstützt, sollten Sie einen **null** -Wert erwarten.</span><span class="sxs-lookup"><span data-stu-id="9e49a-165">If, however, your format supports schema naming, you should anticipate a **NULL** value.</span></span>

<span data-ttu-id="9e49a-166">Wenn ein Metadatenelement ein eingebetteter Metadatenblock ist, erstellen Sie einen Metadatenhandler aus dem unter Datenstrom des eingebetteten Inhalts, und geben Sie den neuen Metadatenhandler zurück.</span><span class="sxs-lookup"><span data-stu-id="9e49a-166">If a metadata item is an embedded metadata block, create a metadata handler from the substream of the embedded content and return the new metadata handler.</span></span> <span data-ttu-id="9e49a-167">Wenn kein metadatenleser für den gruppierten Block verfügbar ist, instanziieren Sie einen unbekannten metadatenreader, und geben Sie ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="9e49a-167">If there is no metadata reader available for the nested block, instantiate and return an unknown metadata reader.</span></span> <span data-ttu-id="9e49a-168">Um einen neuen metadatenleser für den eingebetteten Block zu erstellen, rufen Sie die **CreateMetadataReaderFromContainer** -oder **CreateMetadataReader** -Methode der komponentenfactory auf, oder rufen Sie die [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) -Funktion auf</span><span class="sxs-lookup"><span data-stu-id="9e49a-168">To create a new metadata reader for the embedded block, call the component factory's **CreateMetadataReaderFromContainer** or **CreateMetadataReader** methods, or call the [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) function.</span></span>

<span data-ttu-id="9e49a-169">Wenn der Metadatenstream Big-Endian-Inhalte enthält, ist der metadatenleser für das Austauschen von Datenwerten zuständig, die er verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9e49a-169">If the metadata stream contains big-endian content, the metadata reader is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="9e49a-170">Es ist auch dafür verantwortlich, dass die Leser von blendbenutzern darüber informiert werden, dass Sie mit Big-Endian-Datenströmen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9e49a-170">It is also responsible for informing any nested metadata readers that they are working with big-endian data stream.</span></span> <span data-ttu-id="9e49a-171">Allerdings sollten alle Werte im Little-Endian-Format zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-171">However, all values should be returned in little-endian format.</span></span>

<span data-ttu-id="9e49a-172">Implementieren Sie Unterstützung für die Namespace Navigation durch Unterstützung von Abfragen, bei denen die metadatenelementid eine `VT_CLSID` (GUID) ist, die einem Metadatenformat entspricht.</span><span class="sxs-lookup"><span data-stu-id="9e49a-172">Implement support for namespace navigation by supporting queries where the metadata item ID is a `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="9e49a-173">Wenn ein geschzigter metadatenleser für dieses Format während der-Verarbeitung identifiziert wird, muss er zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-173">If a nested metadata reader for that format is identified during parsing, it must be returned.</span></span> <span data-ttu-id="9e49a-174">Dadurch können Anwendungen einen Metadatenabfrage-Reader verwenden, um Ihr Metadatenformat zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-174">This enables applications to use a metadata query reader to search your metadata format.</span></span>

<span data-ttu-id="9e49a-175">Wenn Sie ein Metadatenelement anhand der ID erhalten, sollten Sie die [Funktion "propvariantchangetype](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) " verwenden, um die ID in den erwarteten Typ umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="9e49a-175">When getting a metadata item by ID, you should use [PropVariantChangeType Function](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) to coerce the ID into the expected type.</span></span> <span data-ttu-id="9e49a-176">Beispielsweise wandelt der IFD-Reader eine ID in den Typ `VT_UI2` um, damit er mit dem Datentyp einer IFD-tagkennung ushort übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9e49a-176">For example, the IFD reader will coerce an ID to type `VT_UI2` to coincide with the data type of an IFD tag ID USHORT.</span></span> <span data-ttu-id="9e49a-177">Der Eingabetyp und der erwartete Typ müssen hierfür beide [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) sein.</span><span class="sxs-lookup"><span data-stu-id="9e49a-177">The input type and expected type must both be [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to do this.</span></span> <span data-ttu-id="9e49a-178">Dies ist nicht erforderlich, aber durch diese Umwandlung wird der Code vereinfacht, der den Reader aufruft, um Metadatenelemente abzufragen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-178">This is not required, but doing this coercion simplifies code that calls the reader to query for metadata items.</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="9e49a-179">IWICPersistStream-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-179">IWICPersistStream Interface</span></span>

<span data-ttu-id="9e49a-180">Die [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) -Schnittstelle erbt von **IPersistStream** und bietet zusätzliche Methoden zum Speichern und Laden von Objekten mithilfe der [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="9e49a-180">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="9e49a-181">Der folgende Code zeigt die Definition der [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) -Schnittstelle, wie in der Datei wincodecsdk. idl definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-181">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="9e49a-182">Die **Loadex** -Methode stellt ihrem metadatenleser einen Datenstrom mit Ihrem Metadatenblock bereit.</span><span class="sxs-lookup"><span data-stu-id="9e49a-182">The **LoadEx** method provides your metadata reader with a data stream containing your metadata block.</span></span> <span data-ttu-id="9e49a-183">Der Reader analysiert diesen Stream für den Zugriff auf die zugrunde liegenden Metadatenelemente.</span><span class="sxs-lookup"><span data-stu-id="9e49a-183">Your reader parses this stream to access the underlying metadata items.</span></span> <span data-ttu-id="9e49a-184">Ihr metadatenleser wird mit einem unter Datenstrom initialisiert, der am Anfang des rohmetadateninhalts positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="9e49a-184">Your metadata reader is initialized with a substream that is positioned at the beginning of the raw metadata content.</span></span> <span data-ttu-id="9e49a-185">Wenn der Reader den vollständigen Stream nicht benötigt, ist der unter Datenstrom auf den Inhalt des Metadatenblocks beschränkt. Andernfalls wird der vollständige Metadatenstream mit dem Positionswert bereitgestellt, der am Anfang des Metadatenblocks festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9e49a-185">If your reader does not require the full stream, the substream is limited in range to only the content of the metadata block; otherwise, the full metadata stream is provided with the position set at the beginning of your metadata block.</span></span>

<span data-ttu-id="9e49a-186">Die **saveex** -Methode wird von metadatenwritern verwendet, um den Metadatenblock zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-186">The **SaveEx** method is used by metadata writers to serialize your metadata block.</span></span> <span data-ttu-id="9e49a-187">Wenn **saveex** in einem metadatenreader verwendet wird, sollte wincodec \_ Err \_ unsupportedoperation zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-187">When **SaveEx** is used in a metadata reader, it should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="9e49a-188">Iwicstreamprovider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-188">IWICStreamProvider Interface</span></span>

<span data-ttu-id="9e49a-189">Die [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) -Schnittstelle ermöglicht es Ihrem metadatenleser, Verweise auf seinen Inhaltsstream bereitzustellen, Informationen zum Stream bereitzustellen und zwischengespeicherte Versionen des Streams zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-189">The [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface enables your metadata reader to provide references to its content stream, provide information about the stream, and refresh cached versions of the stream.</span></span>

<span data-ttu-id="9e49a-190">Der folgende Code zeigt die Definition der [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) -Schnittstelle, wie in der Datei wincodecsdk. idl definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-190">The following code shows the definition of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

<span data-ttu-id="9e49a-191">Die **GetStream** -Methode ruft einen Verweis auf den Metadatenstream ab.</span><span class="sxs-lookup"><span data-stu-id="9e49a-191">The **GetStream** method retrieves a reference to your metadata stream.</span></span> <span data-ttu-id="9e49a-192">Der zurückgegebene Stream sollte den Datenstrom Zeiger auf die Startposition zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-192">The stream you return should have the stream pointer reset to the start position.</span></span> <span data-ttu-id="9e49a-193">Wenn Ihr Metadatenformat vollen Datenstrom Zugriff erfordert, sollte die Startposition der Anfang des Metadatenblocks sein.</span><span class="sxs-lookup"><span data-stu-id="9e49a-193">If your metadata format requires full stream access, the start position should be the start of your metadata block.</span></span>

<span data-ttu-id="9e49a-194">Die **getpersistoptions** -Methode gibt die aktuellen Optionen des Streams aus der [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) -Enumeration zurück.</span><span class="sxs-lookup"><span data-stu-id="9e49a-194">The **GetPersistOptions** method returns the stream's current options from the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="9e49a-195">Die **getpreferredvendorguid** -Methode gibt die GUID des Anbieters des metadatenreaders zurück.</span><span class="sxs-lookup"><span data-stu-id="9e49a-195">The **GetPreferredVendorGUID** method returns the GUID of the vendor of the metadata reader.</span></span>

<span data-ttu-id="9e49a-196">Die **freshstream** -Methode aktualisiert den Metadatenstream.</span><span class="sxs-lookup"><span data-stu-id="9e49a-196">The **RefreshStream** method refreshes the metadata stream.</span></span> <span data-ttu-id="9e49a-197">Diese Methode muss **Loadex** mit einem **null** -Datenstrom für alle gruppierten Metadatenblöcke aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-197">This method must call **LoadEx** with a **NULL** stream for any nested metadata blocks.</span></span> <span data-ttu-id="9e49a-198">Dies ist erforderlich, da geschachtelte Metadata-Blöcke und deren Elemente aufgrund einer direkten Bearbeitung möglicherweise nicht mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9e49a-198">This is necessary because nested metadata blocks and their items may no longer exist, due to in-place editing.</span></span>

## <a name="creating-a-metadata-writer"></a><span data-ttu-id="9e49a-199">Erstellen eines metadatenwriters</span><span class="sxs-lookup"><span data-stu-id="9e49a-199">Creating a Metadata Writer</span></span>

<span data-ttu-id="9e49a-200">Ein metadatenwriter ist ein Typ von Metadatenhandler, der eine Möglichkeit bietet, einen Metadatenblock in einen Bildframe zu serialisieren oder außerhalb eines einzelnen Frames, wenn er vom Bildformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9e49a-200">A metadata writer is a type of metadata handler that provides a way to serialize a metadata block to an image frame, or outside an individual frame if the image format supports it.</span></span> <span data-ttu-id="9e49a-201">Der Haupt Zugriff auf die metadatenwriter innerhalb eines Codecs ist die [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) -Schnittstelle, die jeder WIC-Encoder implementiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-201">The main access to the metadata writers within a codec is through the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface that each WIC encoder implements.</span></span> <span data-ttu-id="9e49a-202">Diese Schnittstelle ermöglicht es Anwendungen, jeden der in ein Bild eingebetteten Metadatenblöcke aufzulisten, damit der entsprechende metadatenwriter für jeden Metadatenblock ermittelt und instanziiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e49a-202">This interface enables applications to enumerate each of the metadata blocks embedded in an image so that the appropriate metadata writer can be discovered and instantiated for each metadata block.</span></span> <span data-ttu-id="9e49a-203">Metadatenblöcke, die keinen entsprechenden metadatenwriter aufweisen, werden als unbekannt angesehen und als GUID CLSID \_ WICUnknownMetadataReader definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-203">Metadata blocks that do not have a corresponding metadata writer are considered unknown, and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="9e49a-204">Um für WIC-aktivierte Anwendungen das Serialisieren und Schreiben Ihres metadatenformats zu ermöglichen, müssen Sie eine Klasse erstellen, die die folgenden Schnittstellen implementiert: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)und [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="9e49a-204">To enable WIC enabled applications to serialize and write your metadata format, you must create a class that implements the following interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="9e49a-205">Wenn Ihr Metadatenformat Einschränkungen aufweist, die einige Methoden der erforderlichen Schnittstellen ungeeignet sind, sollte diese Methode wincodec \_ Err \_ unsupportedoperation zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9e49a-205">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatawriter-interface"></a><span data-ttu-id="9e49a-206">IWICMetadataWriter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-206">IWICMetadataWriter Interface</span></span>

<span data-ttu-id="9e49a-207">Die [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) -Schnittstelle muss von Ihrem metadatenwriter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-207">The [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) interface must be implemented by your metadata writer.</span></span> <span data-ttu-id="9e49a-208">Da **IWICMetadataWriter** außerdem von [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)erbt, müssen Sie auch alle Methoden von **IWICMetadataReader** implementieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-208">Additionally, because **IWICMetadataWriter** inherits from [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), you must also implement all the methods of **IWICMetadataReader**.</span></span> <span data-ttu-id="9e49a-209">Da beide Handlertypen dieselbe Schnittstellen Vererbung erfordern, können Sie eine einzelne Klasse erstellen, die sowohl Lese-als auch Schreibfunktionen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9e49a-209">Because both handler types require the same interface inheritance, you might want to create a single class that provides both reading and writing functionality.</span></span>

<span data-ttu-id="9e49a-210">Der folgende Code zeigt die Definition der metadatenwriter-Schnittstelle, wie in der Datei wincodecsdk. idl definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-210">The following code shows the definition of the metadata writer interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

<span data-ttu-id="9e49a-211">Die **SetValue** -Methode schreibt das angegebene Metadatenelement in den Metadatenstream.</span><span class="sxs-lookup"><span data-stu-id="9e49a-211">The **SetValue** method writes the specified metadata item to the metadata stream.</span></span>

<span data-ttu-id="9e49a-212">Die **setvaluebyindex** -Methode schreibt das angegebene Metadatenelement in den angegebenen Index im Metadatenstream.</span><span class="sxs-lookup"><span data-stu-id="9e49a-212">The **SetValueByIndex** method writes the specified metadata item to the specified index in the metadata stream.</span></span> <span data-ttu-id="9e49a-213">Der Index verweist nicht auf die ID, sondern auf die Position des Elements im Metadatenblock.</span><span class="sxs-lookup"><span data-stu-id="9e49a-213">The index does not refer to the ID but to the position of the item within the metadata block.</span></span>

<span data-ttu-id="9e49a-214">Die **removeValue** -Methode entfernt das angegebene Metadatenelement aus dem Metadatenstream.</span><span class="sxs-lookup"><span data-stu-id="9e49a-214">The **RemoveValue** method removes the specified metadata item from the metadata stream.</span></span>

<span data-ttu-id="9e49a-215">Die **removevaluebyindex** -Methode entfernt das Metadatenelement am angegebenen Index aus dem Metadatenstream.</span><span class="sxs-lookup"><span data-stu-id="9e49a-215">The **RemoveValueByIndex** method removes the metadata item at the specified index from the metadata stream.</span></span> <span data-ttu-id="9e49a-216">Nach dem Entfernen eines Elements wird erwartet, dass die verbleibenden Metadatenelemente den frei gewordenen Index belegen, wenn der Index nicht der letzte Index ist.</span><span class="sxs-lookup"><span data-stu-id="9e49a-216">After removing an item, it is expected that the remaining metadata items will occupy the vacated index if the index is not the last index.</span></span> <span data-ttu-id="9e49a-217">Außerdem wird erwartet, dass sich die Anzahl ändert, nachdem das Element entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="9e49a-217">It is also expected that the count will change after the item is removed.</span></span>

<span data-ttu-id="9e49a-218">Der metadatenwriter ist dafür verantwortlich, die [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Elemente in die zugrunde liegende Struktur zu konvertieren, die für Ihr Format erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9e49a-218">It is the metadata writer's responsibility to convert the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) items to the underlying structure required by your format.</span></span> <span data-ttu-id="9e49a-219">Im Gegensatz zum metadatenreader sollten Variant-Typen jedoch normalerweise nicht in verschiedene Typen umgewandelt werden, da der Aufrufer speziell angibt, welcher Datentyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e49a-219">However, unlike the metadata reader, VARIANT types should not normally be coerced to different types as the caller is specifically indicating what data type to use.</span></span>

<span data-ttu-id="9e49a-220">Ihr metadatenwriter muss alle Metadatenelemente in den Bildstream einbinden, einschließlich ausgeblendeter oder unbekannter Werte.</span><span class="sxs-lookup"><span data-stu-id="9e49a-220">Your metadata writer must commit all metadata items to the image stream, including hidden or unrecognized values.</span></span> <span data-ttu-id="9e49a-221">Dies schließt unbekannte gruppierten Metadatenblöcke ein.</span><span class="sxs-lookup"><span data-stu-id="9e49a-221">This includes unknown nested metadata blocks.</span></span> <span data-ttu-id="9e49a-222">Es ist jedoch Aufgabe des Encoders, alle kritischen Metadatenelemente festzulegen, bevor der Speichervorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="9e49a-222">However, it is the encoder's responsibility to set any critical metadata items prior to initiating the save operation.</span></span>

<span data-ttu-id="9e49a-223">Wenn der Metadatenstream Big-Endian-Inhalte enthält, ist der metadatenwriter für das Austauschen von Datenwerten zuständig, die er verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9e49a-223">If the metadata stream contains big-endian content, the metadata writer is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="9e49a-224">Es ist auch dafür verantwortlich, dass alle gruppierten metadatenwriter darüber informiert werden, dass Sie mit einem Big-Endian-Datenstream arbeiten, wenn Sie gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-224">It is also responsible for informing any nested metadata writers that they are working with a big-endian data stream when they save.</span></span>

<span data-ttu-id="9e49a-225">Implementieren Sie Unterstützung für das Erstellen und Entfernen von Namespaces durch Unterstützung von Set-und Remove-Vorgängen für Metadatenelemente mit einem Typ `VT_CLSID` (GUID), der einem Metadatenformat entspricht.</span><span class="sxs-lookup"><span data-stu-id="9e49a-225">Implement support for namespace creation and removal by supporting set and remove operations on metadata items with a type of `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="9e49a-226">Der metadatenwriter Ruft die [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) -Funktion auf, um den Inhalt des eingefügten metadatenwriters ordnungsgemäß in den übergeordneten metadatenwriter</span><span class="sxs-lookup"><span data-stu-id="9e49a-226">The metadata writer calls the [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) function to properly embed the nested metadata writer content into the parent metadata writer.</span></span>

<span data-ttu-id="9e49a-227">Wenn Ihr Metadatenformat eine direkte Codierung unterstützt, sind Sie für die Verwaltung der erforderlichen Auffüll Vorgänge verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="9e49a-227">If your metadata format supports in-place encoding, you are responsible for managing the required padding.</span></span> <span data-ttu-id="9e49a-228">Weitere Informationen zur direkten Codierung finden Sie unter Übersicht über [WIC-Metadaten](-wic-about-metadata.md) und [Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="9e49a-228">For more information on in-place encoding, see [WIC Metadata Overview](-wic-about-metadata.md) and [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="9e49a-229">IWICPersistStream-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-229">IWICPersistStream Interface</span></span>

<span data-ttu-id="9e49a-230">Die [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) -Schnittstelle erbt von **IPersistStream** und bietet zusätzliche Methoden zum Speichern und Laden von Objekten mithilfe der [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="9e49a-230">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="9e49a-231">Der folgende Code zeigt die Definition der [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) -Schnittstelle, wie in der Datei wincodecsdk. idl definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-231">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="9e49a-232">Die **Loadex** -Methode stellt ihrem Metadatenhandler einen Datenstrom mit Ihrem Metadatenblock bereit.</span><span class="sxs-lookup"><span data-stu-id="9e49a-232">The **LoadEx** method provides your metadata handler with a data stream containing your metadata block.</span></span>

<span data-ttu-id="9e49a-233">Die **saveex** -Methode serialisiert die Metadaten in einen Stream.</span><span class="sxs-lookup"><span data-stu-id="9e49a-233">The **SaveEx** method serializes the metadata into a stream.</span></span> <span data-ttu-id="9e49a-234">Wenn der angegebene Stream mit dem Initialisierungs Datenstrom identisch ist, sollten Sie eine direkte Codierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-234">If the provided stream is the same as initialization stream, you should perform in-place encoding.</span></span> <span data-ttu-id="9e49a-235">Wenn die direkte Codierung unterstützt wird, sollte diese Methode wincodec \_ Err " \_ deomuchmetadata" zurückgeben, wenn nicht genügend Auffüll Vorgänge vorhanden sind, um eine direkte Codierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-235">If in-place encoding is supported, this method should return WINCODEC\_ERR\_TOOMUCHMETADATA when there is insufficient padding to perform in-place encoding.</span></span> <span data-ttu-id="9e49a-236">Wenn die direkte Codierung nicht unterstützt wird, sollte diese Methode wincodec \_ Err \_ unsupportedoperation zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9e49a-236">If in-place encoding is not supported, this method should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

<span data-ttu-id="9e49a-237">Die **IPersistStream:: GetSizeMax** -Methode muss implementiert werden und muss die genaue Größe des metadateninhalts zurückgeben, der in der nachfolgenden Speicherung geschrieben würde.</span><span class="sxs-lookup"><span data-stu-id="9e49a-237">The **IPersistStream::GetSizeMax** method must be implemented and must return the exact size of the metadata content that would be written in subsequent save.</span></span>

<span data-ttu-id="9e49a-238">Die **IPersistStream:: IsDirty** -Methode sollte implementiert werden, wenn der metadatenwriter über einen Stream initialisiert wird, damit ein Bild zuverlässig ermitteln kann, ob sich der Inhalt geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9e49a-238">The **IPersistStream::IsDirty** method should be implemented if the metadata writer is initialized through a stream, so that an image can reliably determine whether its content has changed.</span></span>

<span data-ttu-id="9e49a-239">Wenn Ihr Metadatenformat gruppierten Metadatenblöcke unterstützt, sollte Ihr metadatenwriter an die gruppierten metadatenwriter delegieren, die den Inhalt beim Speichern in einem Stream serialisieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-239">If your metadata format supports nested metadata blocks, your metadata writer should delegate to the nested metadata writers the serializing of its content when saving to a stream.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="9e49a-240">Iwicstreamprovider-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9e49a-240">IWICStreamProvider Interface</span></span>

<span data-ttu-id="9e49a-241">Die Implementierung der [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) -Schnittstelle für einen metadatenwriter ist mit der Implementierung eines metadatenreaders identisch.</span><span class="sxs-lookup"><span data-stu-id="9e49a-241">The implementation of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface for a metadata writer is the same as that of a metadata reader.</span></span> <span data-ttu-id="9e49a-242">Weitere Informationen finden Sie im Abschnitt Erstellen eines metadatenreaders in diesem Dokument.</span><span class="sxs-lookup"><span data-stu-id="9e49a-242">For more information, see Creating a Metadata Reader section in this document.</span></span>

## <a name="installing-and-registering-a-metadata-handler"></a><span data-ttu-id="9e49a-243">Installieren und Registrieren eines metadatenhandlers</span><span class="sxs-lookup"><span data-stu-id="9e49a-243">Installing and Registering a Metadata Handler</span></span>

<span data-ttu-id="9e49a-244">Zum Installieren eines metadatenhandlers müssen Sie die Handlerassembly bereitstellen und in der Systemregistrierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-244">To install a metadata handler, you must provide the handler assembly and register it in the system registry.</span></span> <span data-ttu-id="9e49a-245">Sie können entscheiden, wie und wann die Registrierungsschlüssel aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-245">You can decide how and when the registry keys are populated.</span></span>

> [!Note]  
> <span data-ttu-id="9e49a-246">Zur besseren Lesbarkeit werden die tatsächlichen hexadezimalen GUIDs nicht in den Registrierungs Schlüsseln angezeigt, die in den folgenden Abschnitten dieses Dokuments angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-246">For readability, the actual hexadecimal GUIDs are not shown in the registry keys shown in the following sections of this document.</span></span> <span data-ttu-id="9e49a-247">Um den hexadezimalen Wert für einen angegebenen anzeigen Amen zu ermitteln, lesen Sie die Dateien wincodec. idl und wincodecsdk. idl.</span><span class="sxs-lookup"><span data-stu-id="9e49a-247">To find the hexadecimal value for a specified friendly name, see the wincodec.idl and wincodecsdk.idl files.</span></span>

 

### <a name="metadata-handler-registry-keys"></a><span data-ttu-id="9e49a-248">Metadatenhandler-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="9e49a-248">Metadata Handler Registry Keys</span></span>

<span data-ttu-id="9e49a-249">Jeder Metadatenhandler wird durch eine eindeutige CLSID identifiziert, und jeder Handler muss seine CLSID unter der Kategorie-ID-GUID des metadatenhandlers registrieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-249">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="9e49a-250">Die Kategoriekennung der einzelnen Handlertypen ist in wincodec. idl; definiert. der Name der Kategorie-ID für Reader lautet CATID \_ WICMetadataReader, und der Name der Kategorie-ID für Writer lautet CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="9e49a-250">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

<span data-ttu-id="9e49a-251">Jeder Metadatenhandler wird durch eine eindeutige CLSID identifiziert, und jeder Handler muss seine CLSID unter der Kategorie-ID-GUID des metadatenhandlers registrieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-251">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="9e49a-252">Die Kategoriekennung der einzelnen Handlertypen ist in wincodec. idl; definiert. der Name der Kategorie-ID für Reader lautet CATID \_ WICMetadataReader, und der Name der Kategorie-ID für Writer lautet CATID \_ WICMetadataWriter.</span><span class="sxs-lookup"><span data-stu-id="9e49a-252">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

> [!Note]  
> <span data-ttu-id="9e49a-253">In den folgenden Registrierungsschlüssel Listen verweist {Reader CLSID} auf die eindeutige CLSID, die Sie für Ihren metadatenreader bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-253">In the following registry key listings, {Reader CLSID} refers to the unique CLSID that you provide for your metadata reader.</span></span> <span data-ttu-id="9e49a-254">{Writer CLSID} verweist auf die eindeutige CLSID, die Sie für Ihren metadatenwriter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-254">{Writer CLSID} refers to the unique CLSID that you provide for your metadata writer.</span></span> <span data-ttu-id="9e49a-255">{Handler CLSID} bezieht sich auf die CLSID des Readers, die CLSID des Writers oder beides, abhängig von den Handlern, die Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-255">{Handler CLSID} refers to the reader's CLSID, the writer's CLSID, or both, depending on which handlers you are providing.</span></span> <span data-ttu-id="9e49a-256">{Container GUID} verweist auf das Container Objekt (Bildformat oder Metadatenformat), das den Metadatenblock enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="9e49a-256">{Container GUID} refers to the container object (image format or metadata format) that can contain the metadata block.</span></span>

 

<span data-ttu-id="9e49a-257">Die folgenden Registrierungsschlüssel registrieren Ihren Metadatenhandler mit den anderen verfügbaren metadatenhandlern:</span><span class="sxs-lookup"><span data-stu-id="9e49a-257">The following registry keys register your metadata handler with the other metadata handlers available:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

<span data-ttu-id="9e49a-258">Zusätzlich zum Registrieren von Handlern in ihren jeweiligen Kategorien müssen Sie auch zusätzliche Schlüssel registrieren, die für den Handler spezifische Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-258">In addition to registering your handlers in their respective categories, you must also register additional keys that provide information specific to the handler.</span></span> <span data-ttu-id="9e49a-259">Leser und Writer haben ähnliche Anforderungen an den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="9e49a-259">Readers and writers share similar registry key requirements.</span></span> <span data-ttu-id="9e49a-260">Die folgende Syntax zeigt, wie ein Handler registriert wird.</span><span class="sxs-lookup"><span data-stu-id="9e49a-260">The following syntax shows how to register a handler.</span></span> <span data-ttu-id="9e49a-261">Sowohl der Reader-als auch der Writer-Handler müssen auf diese Weise registriert werden, wobei die entsprechenden CLSIDs verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="9e49a-261">Both the reader handler and writer handler must be registered in this way, using their respective CLSIDs:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a><span data-ttu-id="9e49a-262">Metadatenleser</span><span class="sxs-lookup"><span data-stu-id="9e49a-262">Metadata Readers</span></span>

<span data-ttu-id="9e49a-263">Die Registrierung des metadatenreaders umfasst auch Schlüssel, die beschreiben, wie der Reader in ein Containerformat eingebettet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e49a-263">The metadata reader registration also includes keys that describe how the reader can be embedded in a container format.</span></span> <span data-ttu-id="9e49a-264">Ein Containerformat kann ein Bildformat (z. b. TIFF oder JPEG) sein. Es kann auch ein anderes Metadatenformat sein, z. b. ein IFD-Metadatenblock.</span><span class="sxs-lookup"><span data-stu-id="9e49a-264">A container format can be an image format such as TIFF or JPEG; it can also be another metadata format such as an IFD metadata block.</span></span> <span data-ttu-id="9e49a-265">Nativ unterstützte Bild Containerformate sind in wincodec. idl aufgeführt. jedes Bild Containerformat ist als GUID mit einem Namen definiert, der mit dem GUID- \_ Containerformat beginnt.</span><span class="sxs-lookup"><span data-stu-id="9e49a-265">Natively supported image container formats are listed in wincodec.idl; each image container format is defined as a GUID with a name that begins with GUID\_ContainerFormat.</span></span> <span data-ttu-id="9e49a-266">Nativ unterstützte metadatencontainerformate sind in wincodecsdk. idl aufgeführt. jedes metadatencontainerformat ist als GUID mit einem Namen definiert, der mit GUID \_ MetadataFormat beginnt.</span><span class="sxs-lookup"><span data-stu-id="9e49a-266">Natively supported metadata container formats are listed in wincodecsdk.idl; each metadata container format is defined as a GUID with a name that begins with GUID\_MetadataFormat.</span></span>

<span data-ttu-id="9e49a-267">Mit den folgenden Schlüsseln wird ein Container registriert, den der metadatenreader unterstützt, sowie die Daten, die zum Lesen aus diesem Container benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-267">The following keys register a container that the metadata reader supports, and the data needed to read from that container.</span></span> <span data-ttu-id="9e49a-268">Jeder Container, der vom Reader unterstützt wird, muss auf diese Weise registriert werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-268">Each container supported by the reader must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

<span data-ttu-id="9e49a-269">Der Muster Schlüssel beschreibt das binäre Muster, das verwendet wird, um den Metadatenblock mit dem Reader abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-269">The Pattern key describes the binary pattern that is used to match the metadata block to the reader.</span></span> <span data-ttu-id="9e49a-270">Wenn Sie ein Muster für den metadatenreader definieren, sollte es zuverlässig genug sein, dass eine positive Übereinstimmung bedeutet, dass der metadatenleser die Metadaten im Metadatenblock, der verarbeitet wird, verstehen kann.</span><span class="sxs-lookup"><span data-stu-id="9e49a-270">When defining a pattern for your metadata reader, it should be reliable enough that a positive match means the metadata reader can understand the metadata in the metadata block being processed.</span></span>

<span data-ttu-id="9e49a-271">Der DataOffset-Schlüssel beschreibt den fixierten Offset der Metadaten aus dem Block Header.</span><span class="sxs-lookup"><span data-stu-id="9e49a-271">The DataOffset key describes the fixed offset of the metadata from the block header.</span></span> <span data-ttu-id="9e49a-272">Dieser Schlüssel ist optional. wenn er nicht angegeben ist, bedeutet dies, dass die eigentlichen Metadaten nicht mithilfe eines Fixed-Offsets aus dem Block Header gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="9e49a-272">This key is optional and, if not specified, means that the actual metadata cannot be located using a fixed offset from the block header.</span></span>

### <a name="metadata-writers"></a><span data-ttu-id="9e49a-273">Metadatenschreiber</span><span class="sxs-lookup"><span data-stu-id="9e49a-273">Metadata Writers</span></span>

<span data-ttu-id="9e49a-274">Die Registrierung des metadatenwriters umfasst auch Schlüssel, die beschreiben, wie der Header vor dem in ein Containerformat eingebetteten metadateninhalt geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e49a-274">The metadata writer registration also includes keys that describe how to write out the header preceding the metadata content embedded in a container format.</span></span> <span data-ttu-id="9e49a-275">Ebenso wie der Reader kann ein Containerformat ein Bildformat oder ein anderer Metadatenblock sein.</span><span class="sxs-lookup"><span data-stu-id="9e49a-275">As with the reader, a container format can be an image format or another metadata block.</span></span>

<span data-ttu-id="9e49a-276">Mit den folgenden Schlüsseln wird ein Container registriert, den der metadatenwriter unterstützt, sowie die Daten, die zum Schreiben des Headers und der Metadaten benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-276">The following keys register a container that the metadata writer supports, and the data needed to write the header and metadata.</span></span> <span data-ttu-id="9e49a-277">Jeder Container, der vom Writer unterstützt wird, muss auf diese Weise registriert werden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-277">Each container supported by the writer must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

<span data-ttu-id="9e49a-278">Der Schlüssel schreibheader beschreibt das binäre Muster des Metadatenblock Headers, der geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e49a-278">The WriteHeader key describes the binary pattern of the metadata block header to be written.</span></span> <span data-ttu-id="9e49a-279">Dieses binäre Muster stimmt mit dem readermusterschlüssel des metadatenformats überein.</span><span class="sxs-lookup"><span data-stu-id="9e49a-279">This binary pattern coincides with the metadata format's reader Pattern key.</span></span>

<span data-ttu-id="9e49a-280">Der Schlüssel "Write-Offset" beschreibt den fixierten Offset aus dem Block Header, bei dem die Metadaten geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-280">The WriteOffset key describes the fixed offset from the block header at which the metadata should be written.</span></span> <span data-ttu-id="9e49a-281">Dieser Schlüssel ist optional. wenn er nicht angegeben ist, bedeutet dies, dass die eigentlichen Metadaten nicht mit dem-Header geschrieben werden sollten.</span><span class="sxs-lookup"><span data-stu-id="9e49a-281">This key is optional and, if not specified, means that the actual metadata should not be written out with the header.</span></span>

### <a name="signing-a-metadata-handler"></a><span data-ttu-id="9e49a-282">Signieren eines metadatenhandlers</span><span class="sxs-lookup"><span data-stu-id="9e49a-282">Signing a Metadata Handler</span></span>

<span data-ttu-id="9e49a-283">Alle Metadatenhandler müssen digital signiert werden, damit Sie am WIC-Ermittlungsprozess teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="9e49a-283">All metadata handlers must be digitally signed to participate in the WIC discovery process.</span></span> <span data-ttu-id="9e49a-284">WIC lädt keinen Handler, der nicht von einer vertrauenswürdigen Zertifizierungsstelle signiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e49a-284">WIC will not load any handler that is not signed by a trusted certificate authority.</span></span> <span data-ttu-id="9e49a-285">Weitere Informationen zum digitalen Signieren finden [Sie unter Einführung in die Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9e49a-285">For more information on digital signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="special-considerations"></a><span data-ttu-id="9e49a-286">Besondere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="9e49a-286">Special Considerations</span></span>

<span data-ttu-id="9e49a-287">Die folgenden Abschnitte enthalten zusätzliche Informationen, die Sie berücksichtigen müssen, wenn Sie Ihre eigenen Metadatenhandler erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-287">The following sections include additional information you must consider when creating your own metadata handlers.</span></span>

### <a name="propvariants"></a><span data-ttu-id="9e49a-288">Propvarianten</span><span class="sxs-lookup"><span data-stu-id="9e49a-288">PROPVARIANTS</span></span>

<span data-ttu-id="9e49a-289">WIC verwendet eine [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) , um ein Metadatenelement für Lese-und Schreibvorgänge darzustellen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-289">WIC uses a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to represent a metadata item for both reading and writing.</span></span> <span data-ttu-id="9e49a-290">Eine PROPVARIANT bietet einen Datentyp und Datenwert für ein Metadatenelement, das in einem Metadatenformat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e49a-290">A PROPVARIANT provides a data type and data value for a metadata item used within a metadata format.</span></span> <span data-ttu-id="9e49a-291">Als Writer eines metadatenhandlers haben Sie viel Flexibilität bei der Speicherung von Daten im Metadatenformat und der Darstellung von Daten in einem Metadatenblock.</span><span class="sxs-lookup"><span data-stu-id="9e49a-291">As the writer of a metadata handler, you have a lot of flexibility on how data is stored in the metadata format and how data is represented within a metadata block.</span></span> <span data-ttu-id="9e49a-292">In der folgenden Tabelle finden Sie Richtlinien, die Ihnen bei der Entscheidung helfen, den geeigneten PROPVARIANT-Typ in unterschiedlichen Situationen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-292">The following table provides guidelines to help you decide on the appropriate PROPVARIANT type to use in different situations.</span></span>



| <span data-ttu-id="9e49a-293">Metadatentyp ist...</span><span class="sxs-lookup"><span data-stu-id="9e49a-293">Metadata type is...</span></span>          | <span data-ttu-id="9e49a-294">PROPVARIANT-Typ verwenden</span><span class="sxs-lookup"><span data-stu-id="9e49a-294">Use PROPVARIANT type</span></span>      | <span data-ttu-id="9e49a-295">PROPVARIANT-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e49a-295">PROPVARIANT Property</span></span>                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e49a-296">Leer oder nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9e49a-296">Empty or non-existent.</span></span>       | <span data-ttu-id="9e49a-297">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="9e49a-297">VT\_EMPTY</span></span>                 | <span data-ttu-id="9e49a-298">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="9e49a-298">Not applicable.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="9e49a-299">Nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-299">Undefined.</span></span>                   | <span data-ttu-id="9e49a-300">VT- \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="9e49a-300">VT\_BLOB</span></span>                  | <span data-ttu-id="9e49a-301">Verwenden Sie die BLOB-Eigenschaft, um die Größe und den Zeiger auf das BLOB-Objekt festzulegen, das mithilfe von cotaskmemzugewieszugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="9e49a-301">Use the blob property to set the size and pointer to the BLOB object allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="9e49a-302">Ein Metadatenblock.</span><span class="sxs-lookup"><span data-stu-id="9e49a-302">A metadata block.</span></span>            | <span data-ttu-id="9e49a-303">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="9e49a-303">VT\_UNKNOWN</span></span>               | <span data-ttu-id="9e49a-304">Dieser Typ verwendet die punkVal-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9e49a-304">This type uses the punkVal property.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="9e49a-305">Ein Array von Typen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-305">An array of types.</span></span>           | <span data-ttu-id="9e49a-306">VT \_ Vector \| VT \_ {Type}</span><span class="sxs-lookup"><span data-stu-id="9e49a-306">VT\_VECTOR \| VT\_{type}</span></span>  | <span data-ttu-id="9e49a-307">Verwenden Sie die Eigenschaft "ca {Type}", um die Anzahl und den Zeiger auf das mit cotaskmemzuzugeordnete Array festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-307">Use the ca{type} property to set the count and pointer to the array allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="9e49a-308">Ein Array von metadatenblöcken.</span><span class="sxs-lookup"><span data-stu-id="9e49a-308">An array of metadata blocks.</span></span> | <span data-ttu-id="9e49a-309">VT \_ Vector \| VT \_ Variant</span><span class="sxs-lookup"><span data-stu-id="9e49a-309">VT\_VECTOR \| VT\_VARIANT</span></span> | <span data-ttu-id="9e49a-310">Verwenden Sie die capropvar-Eigenschaft, um das Array von Varianten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-310">Use the capropvar property to set the array of variants.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="9e49a-311">Ein-Wert mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-311">A signed rational value.</span></span>     | <span data-ttu-id="9e49a-312">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="9e49a-312">VT\_I8</span></span>                    | <span data-ttu-id="9e49a-313">Verwenden Sie die Hval-Eigenschaft, um den Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-313">Use the hVal property to set the value.</span></span> <span data-ttu-id="9e49a-314">Legen Sie das hohe Wort auf den Nenner und das niedrige Wort auf den Zähler fest.</span><span class="sxs-lookup"><span data-stu-id="9e49a-314">Set the high word to the denominator and the low word to the numerator.</span></span>                                                                                                                                                                |
| <span data-ttu-id="9e49a-315">Ein rationeller Wert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-315">A rational value.</span></span>            | <span data-ttu-id="9e49a-316">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="9e49a-316">VT\_UI8</span></span>                   | <span data-ttu-id="9e49a-317">Verwenden Sie die uhval-Eigenschaft, um den Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9e49a-317">Use the uhVal property to set the value.</span></span> <span data-ttu-id="9e49a-318">Legen Sie das highpart-Element auf den Nenner und den LowPart-Wert auf den Zähler fest.</span><span class="sxs-lookup"><span data-stu-id="9e49a-318">Set the HighPart to the denominator and the LowPart to the numerator.</span></span> <span data-ttu-id="9e49a-319">Beachten Sie, dass LowPart ein int ohne Vorzeichen ist. Der Zähler muss von einem Ganzzahl ohne Vorzeichen int in einen int-Wert konvertiert werden, um sicherzustellen, dass das Signier Bit beibehalten wird, wenn es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e49a-319">Note that the LowPart is an unsigned int. The numerator should be converted from an unsigned int to an int to ensure that the sign bit is preserved if present.</span></span> |



 

<span data-ttu-id="9e49a-320">Verwenden Sie keine sicheren Arrays, um Redundanz bei der Darstellung von Array Elementen zu vermeiden. Verwenden Sie nur einfache Arrays.</span><span class="sxs-lookup"><span data-stu-id="9e49a-320">To avoid redundancy in representing array items, do not use safe arrays; use only simple arrays.</span></span> <span data-ttu-id="9e49a-321">Dadurch wird die Arbeit reduziert, die eine Anwendung bei der Interpretation von [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Typen ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="9e49a-321">This reduces the work an application needs to perform when interpreting [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types.</span></span>

<span data-ttu-id="9e49a-322">Vermeiden Sie die Verwendung `VT_BYREF` und Speicherung von Werten, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="9e49a-322">Avoid using `VT_BYREF` and store values inline whenever possible.</span></span> <span data-ttu-id="9e49a-323">`VT_BYREF` ist bei kleinen Typen (häufig für Metadatenelemente) ineffizient und stellt keine Größen Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="9e49a-323">`VT_BYREF` is inefficient for small types (common for metadata items) and does not provide size information.</span></span>

<span data-ttu-id="9e49a-324">Bevor Sie eine [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)verwenden, wird immer **propvariantinit** aufgerufen, um den Wert zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="9e49a-324">Before using a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), always call **PropVariantInit** to initialize the value.</span></span> <span data-ttu-id="9e49a-325">Wenn Sie mit dem PROPVARIANT-Vorgang fertig sind, müssen Sie immer **propvariantclear** aufzurufen, um den für die Variable zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9e49a-325">When you are finished with the PROPVARIANT, always call **PropVariantClear** to release any memory allocated for the variable.</span></span>

### <a name="8bim-handlers"></a><span data-ttu-id="9e49a-326">8bim-Handler</span><span class="sxs-lookup"><span data-stu-id="9e49a-326">8BIM Handlers</span></span>

<span data-ttu-id="9e49a-327">Beim Schreiben eines metadatenhandlers für einen 8bim-Metadatenblock müssen Sie eine Signatur verwenden, die sowohl die 8bim-Signatur als auch die ID kapselt.</span><span class="sxs-lookup"><span data-stu-id="9e49a-327">When writing a metadata handler for an 8BIM metadata block, you must use a signature that encapsulates both the 8BIM signature and the ID.</span></span> <span data-ttu-id="9e49a-328">Der Native 8bimiptc-metadatenreader stellt z. b. die folgenden Registrierungsinformationen für die Leser Ermittlung bereit:</span><span class="sxs-lookup"><span data-stu-id="9e49a-328">For example, the native 8BIMIPTC metadata reader provides the following registry information for reader discovery:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

<span data-ttu-id="9e49a-329">Der 8bimiptc-Reader hat ein registriertes Muster von 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span><span class="sxs-lookup"><span data-stu-id="9e49a-329">The 8BIMIPTC reader has a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span></span> <span data-ttu-id="9e49a-330">Die ersten vier Bytes (0x38, 0x42, 0x49, 0x4D) sind die 8bim-Signatur, und die letzten zwei Bytes (0x04, 0x04) stellen die ID für den IPTC-Datensatz dar.</span><span class="sxs-lookup"><span data-stu-id="9e49a-330">The first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature, and the last two bytes (0x04, 0x04) are the ID for the IPTC record.</span></span>

<span data-ttu-id="9e49a-331">Wenn Sie also einen 8bim-metadatenleser für Auflösungsinformationen schreiben möchten, benötigen Sie ein registriertes Muster von 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span><span class="sxs-lookup"><span data-stu-id="9e49a-331">So, to write an 8BIM metadata reader for resolution information, you would need a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span></span> <span data-ttu-id="9e49a-332">Auch hier handelt es sich bei den ersten vier Bytes (0x38, 0x42, 0x49, 0x4D) um die 8bim-Signatur.</span><span class="sxs-lookup"><span data-stu-id="9e49a-332">Again, the first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature.</span></span> <span data-ttu-id="9e49a-333">Die letzten zwei Bytes (0x03, 0xED) sind jedoch die Auflösungs Informations-ID, wie im PSD-Format definiert.</span><span class="sxs-lookup"><span data-stu-id="9e49a-333">The last two bytes (0x03, 0xED), however, are the resolution information ID as defined by the PSD format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e49a-334">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e49a-334">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9e49a-335">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9e49a-335">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9e49a-336">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="9e49a-336">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="9e49a-337">Übersicht über WIC-Metadaten</span><span class="sxs-lookup"><span data-stu-id="9e49a-337">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="9e49a-338">Übersicht über die Metadaten-Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="9e49a-338">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="9e49a-339">Übersicht über das Lesen und Schreiben von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="9e49a-339">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="9e49a-340">Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="9e49a-340">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

<span data-ttu-id="9e49a-341">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9e49a-341">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9e49a-342">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="9e49a-342">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
