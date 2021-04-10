---
description: Dieses Thema enthält eine Einführung in das neue Extensible Metadata Platform (XMP)-Schema und die Windows 7 Photo-Eigenschaft System. Photo. People Ames, die das Markieren von Einzelpersonen in einem digitalen Foto ermöglicht.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Übersicht über Personen Tags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131893"
---
# <a name="people-tagging-overview"></a><span data-ttu-id="38b78-103">Übersicht über Personen Tags</span><span class="sxs-lookup"><span data-stu-id="38b78-103">People Tagging Overview</span></span>

<span data-ttu-id="38b78-104">Dieses Thema enthält eine Einführung in das neue Extensible Metadata Platform (XMP)-Schema und die Windows 7 Photo-Eigenschaft [System. Photo. People Ames](../properties/props-system-photo-peoplenames.md) , die das Markieren von Einzelpersonen in einem digitalen Foto ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="38b78-104">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span> <span data-ttu-id="38b78-105">In diesem Thema wird auch erläutert, wie Sie die WIC-API (Windows Imaging Component) zum Lesen und Schreiben der Metadaten verwenden, die für das Tagging von Personen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="38b78-105">This topic also discusses how to use the Windows Imaging Component (WIC) API to both read and write the metadata needed for people tagging.</span></span>

<span data-ttu-id="38b78-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="38b78-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="38b78-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="38b78-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="38b78-108">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="38b78-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="38b78-109">Personen Tags</span><span class="sxs-lookup"><span data-stu-id="38b78-109">People Tagging</span></span>](#people-tagging-overview)
    -   [<span data-ttu-id="38b78-110">Personennamen</span><span class="sxs-lookup"><span data-stu-id="38b78-110">People Names</span></span>](#people-names)
    -   [<span data-ttu-id="38b78-111">Menschen Rechtecke</span><span class="sxs-lookup"><span data-stu-id="38b78-111">People Rectangles</span></span>](#people-rectangles)
-   [<span data-ttu-id="38b78-112">Schema Verweis</span><span class="sxs-lookup"><span data-stu-id="38b78-112">Schema Reference</span></span>](#schema-reference)
    -   [<span data-ttu-id="38b78-113">Microsoft-Foto 1,2-Schema</span><span class="sxs-lookup"><span data-stu-id="38b78-113">Microsoft Photo 1.2 Schema</span></span>](#microsoft-photo-12-schema)
    -   [<span data-ttu-id="38b78-114">Microsoft Photo RegionInfo-Schema</span><span class="sxs-lookup"><span data-stu-id="38b78-114">Microsoft Photo RegionInfo Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="38b78-115">Microsoft-Foto Regions Schema</span><span class="sxs-lookup"><span data-stu-id="38b78-115">Microsoft Photo Region Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="38b78-116">Beispiel Metadaten</span><span class="sxs-lookup"><span data-stu-id="38b78-116">Sample Metadata</span></span>](#sample-metadata)
-   [<span data-ttu-id="38b78-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38b78-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="38b78-118">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="38b78-118">Prerequisites</span></span>

<span data-ttu-id="38b78-119">Um dieses Thema zu verstehen, sollten Sie mit den WIC-decoderschnittstellen und den zugehörigen COM-Komponenten (Related Component Object Model) vertraut sein, wie in der [Übersicht über Windows Imaging Component](-wic-about-windows-imaging-codec.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="38b78-119">To understand this topic, you should be familiar with the WIC decoder interfaces and its related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="38b78-120">Außerdem ist es hilfreich, eine allgemeine Vertrautheit mit der Erstellung von Metadaten zu erhalten, insbesondere mit XMP.</span><span class="sxs-lookup"><span data-stu-id="38b78-120">It also helps to have a general familiarity with imaging metadata, especially XMP.</span></span>

## <a name="introduction"></a><span data-ttu-id="38b78-121">Einführung</span><span class="sxs-lookup"><span data-stu-id="38b78-121">Introduction</span></span>

<span data-ttu-id="38b78-122">Microsoft hat ein neues XMP-Schema zum Markieren von Personen in einem digitalen Image erstellt.</span><span class="sxs-lookup"><span data-stu-id="38b78-122">Microsoft has created a new XMP schema for tagging people within a digital image.</span></span> <span data-ttu-id="38b78-123">Mit diesem Schema können Anwendungen die Namen und Speicherorte von Personen, die sich im Image befinden, als Metadaten innerhalb des Bilds speichern.</span><span class="sxs-lookup"><span data-stu-id="38b78-123">This schema enables applications to store the names and locations of individuals who are in the image as metadata within the image.</span></span> <span data-ttu-id="38b78-124">Zusätzlich zum neuen Schema ist die neue Photo-Eigenschaft [System. Photo. People Ames](../properties/props-system-photo-peoplenames.md) in Windows 7 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38b78-124">In addition to the new schema, the new photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) is available in Windows 7.</span></span> <span data-ttu-id="38b78-125">Diese neue Eigenschaft ermöglicht es Anwendungen, die in den Bild Metadaten gespeicherten Namen der einzelnen Personen zu lesen.</span><span class="sxs-lookup"><span data-stu-id="38b78-125">This new property enables applications to read the individual's names stored in the image metadata.</span></span> <span data-ttu-id="38b78-126">WIC nutzt diese neuen Features, indem es Anwendungen ermöglicht, Personen zu lesen und zu schreiben, die Metadaten für digitale Fotos markieren.</span><span class="sxs-lookup"><span data-stu-id="38b78-126">WIC utilizes these new features by enabling applications to easily read and write people tagging metadata to digital photos.</span></span>

## <a name="people-tagging"></a><span data-ttu-id="38b78-127">Personen Tags</span><span class="sxs-lookup"><span data-stu-id="38b78-127">People Tagging</span></span>

<span data-ttu-id="38b78-128">WIC bietet Anwendungsentwicklern com-Komponenten, die Bilddaten und Bild Metadaten lesen.</span><span class="sxs-lookup"><span data-stu-id="38b78-128">WIC provides application developers with COM components which read image data as well as image metadata.</span></span> <span data-ttu-id="38b78-129">Zum Lesen und Schreiben von Metadaten, wie z. b. das neue Feature "People Tagging", stellt WIC die Schnittstellen [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) und [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) bereit.</span><span class="sxs-lookup"><span data-stu-id="38b78-129">For reading and writing metadata, such as the new people tagging feature, WIC provides the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) and [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interfaces.</span></span> <span data-ttu-id="38b78-130">Diese Schnittstellen ermöglichen es Anwendungen, die [Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md) zu verwenden, um Metadaten in die einzelnen Frames eines Bilds zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="38b78-130">These interfaces enable applications to use the [metadata query language](-wic-codec-metadataquerylanguage.md) to write metadata to the individual frames of an image.</span></span> <span data-ttu-id="38b78-131">Der folgende Abschnitt veranschaulicht das Lesen und Schreiben der People-Tagging-Metadaten in die Metadaten eines Images mithilfe von WIC-Abfrage Lesern und-Writern.</span><span class="sxs-lookup"><span data-stu-id="38b78-131">The following section demonstrates how to read and write the people-tagging metadata into an image's metadata by using WIC query readers and writers.</span></span>

### <a name="people-names"></a><span data-ttu-id="38b78-132">Personennamen</span><span class="sxs-lookup"><span data-stu-id="38b78-132">People Names</span></span>

<span data-ttu-id="38b78-133">Ein Teil der People-Tagging-Funktion ist die Möglichkeit, einfach eine Liste der Namen der im Image markierten Personen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38b78-133">Part of the people-tagging feature is the ability to simply get a list the names of the people tagged within the image.</span></span> <span data-ttu-id="38b78-134">Dieser Teil des Features wird von den metadatenhandlern [System. Photo. People Ames](../properties/props-system-photo-peoplenames.md) und WIC unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38b78-134">This part of the feature is supported by the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) and WIC's metadata handlers.</span></span> <span data-ttu-id="38b78-135">Die [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Schnittstelle wird in Verbindung mit der System. Photo. peoplenames-Eigenschaft verwendet, um die Namen der in einem Bild identifizierten Personen zu lesen und in den Bild Metadaten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="38b78-135">The [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) interface, in conjunction with the System.Photo.PeopleNames property, are used to read the names of people identified in an image and stored in the image metadata.</span></span>

<span data-ttu-id="38b78-136">Im folgenden Codebeispiel wird ein Abfrage Reader veranschaulicht, der aus einem Bild Rahmen abgerufen wurde, um die Metadaten eines Bilds nach markierten Namen der [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) -Eigenschaft abzufragen.</span><span class="sxs-lookup"><span data-stu-id="38b78-136">The following code example demonstrates a query reader obtained from an image frame to query an image's metadata for tagged names of the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



<span data-ttu-id="38b78-137">Der Abfrage Ausdruck "System. Photo. People Ames" fragt den Frame für die Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="38b78-137">The query expression "System.Photo.PeopleNames" queries the frame for the property.</span></span> <span data-ttu-id="38b78-138">Wenn die Metadaten für Personen Tags vorhanden sind und die Namen der Personen enthalten, wird der [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Wert auf VT \_ LPWSTR festgelegt, und der Datenwert enthält die Liste der markierten Namen.</span><span class="sxs-lookup"><span data-stu-id="38b78-138">If the people-tagging metadata exists and contains people's names, the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will be set to VT\_LPWSTR and the data value will contain the list of tagged names.</span></span> <span data-ttu-id="38b78-139">Weitere Informationen zum Lesen von Bild Metadaten finden Sie unter Übersicht über das [Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="38b78-139">For more information on reading image metadata, see [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="38b78-140">Das Abfragen des People Names-Tags ist nur nützlich, wenn das Image tatsächlich die People-Tagging-Metadaten enthält.</span><span class="sxs-lookup"><span data-stu-id="38b78-140">Querying for the people names tag is only useful if the image actually contains the people-tagging metadata.</span></span> <span data-ttu-id="38b78-141">Damit dies geschehen kann, muss eine Anwendung Sie zuerst schreiben.</span><span class="sxs-lookup"><span data-stu-id="38b78-141">For this to occur, an application must first have written it.</span></span> <span data-ttu-id="38b78-142">Um die Metadaten für Personennamen zu schreiben, verwenden Sie eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) und den expliziten XMP-Pfad der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="38b78-142">To write the people names metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="38b78-143">Im folgenden Codebeispiel wird die Verwendung eines Abfrage-Writers zum Schreiben eines Namens in den Abfrage Pfad veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="38b78-143">The following code example demonstrates using a query writer to write a name to the query path.</span></span>


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



<span data-ttu-id="38b78-144">Beachten Sie den Schritt zum Erstellen der XMP-Struktur, und legen Sie Sie unter fest `MPRI:Regions/{ulong=0}` .</span><span class="sxs-lookup"><span data-stu-id="38b78-144">Note the step constructing the XMP structure and setting it under `MPRI:Regions/{ulong=0}`.</span></span> <span data-ttu-id="38b78-145">Ohne diesen Schritt kann der WIC nicht ermitteln, wo er später platziert werden soll `PersonDisplayName` .</span><span class="sxs-lookup"><span data-stu-id="38b78-145">Without this step, the WIC can't identify where to place the `PersonDisplayName` later on.</span></span> <span data-ttu-id="38b78-146">Beachten Sie außerdem, dass der explizite Abfrage Pfad anstelle von [System. Photo. People Ames](-wic-photoprop-system-photo-peoplenames.md)verwendet wird, dessen metadatenrichtlinie das Schreiben von Metadaten nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38b78-146">Also note that the explicit query path is used instead of [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), whose metadata policy does not support writing metadata.</span></span>

### <a name="people-rectangles"></a><span data-ttu-id="38b78-147">Menschen Rechtecke</span><span class="sxs-lookup"><span data-stu-id="38b78-147">People Rectangles</span></span>

<span data-ttu-id="38b78-148">Die Namen der Personen sind jedoch nur Teil der People-Tagging-Funktion.</span><span class="sxs-lookup"><span data-stu-id="38b78-148">People's names however, are only part of the people-tagging feature.</span></span> <span data-ttu-id="38b78-149">Zusätzlich zum Speichern von Personennamen in den Metadaten unterstützt das Schema auch Regions Informationen, die den spezifischen Bereich (ein Rechteck) identifizieren, der im Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38b78-149">In addition to storing people's names in the metadata, the schema also supports region information that identifies the specific area (a rectangle) the person is shown in the image.</span></span>

<span data-ttu-id="38b78-150">Die Rechteck Informationen werden durch vier durch Trennzeichen getrennte Dezimalwerte dargestellt, z. b. "0,25, 0,25, 0,25, 0,25".</span><span class="sxs-lookup"><span data-stu-id="38b78-150">The rectangle information is represented by four comma-delimited decimal values, such as "0.25, 0.25, 0.25, 0.25".</span></span> <span data-ttu-id="38b78-151">Die ersten beiden Werte geben die obere linke Koordinate an. die letzten beiden geben die Höhe und Breite des Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="38b78-151">The first two values specify the top-left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="38b78-152">Die Dimensionen des Bilds zum Definieren von Menschen Rechtecke werden zu 1 normalisiert, was bedeutet, dass im Beispiel "0,25, 0,25, 0,25, 0,25" das Rechteck 1/4 der Entfernung von oben und 1/4 der Entfernung von der linken Seite des Bilds startet.</span><span class="sxs-lookup"><span data-stu-id="38b78-152">The dimensions of the image for the purposes of defining people rectangles are normalized to 1, which means that in the "0.25, 0.25, 0.25, 0.25" example, the rectangle starts 1/4 of the distance from the top and 1/4 of the distance from the left of the image.</span></span> <span data-ttu-id="38b78-153">Die Höhe und Breite des Rechtecks sind 1/4 der Größe ihrer jeweiligen Bild Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="38b78-153">Both the height and width of the rectangle are 1/4 of the size of their respective image dimensions.</span></span>

<span data-ttu-id="38b78-154">Die Rechteck Informationen, mit denen Einzelpersonen identifiziert werden, werden auf die gleiche Weise geschrieben wie die Namen von Personen in derselben Struktur.</span><span class="sxs-lookup"><span data-stu-id="38b78-154">The rectangle information that identifies individuals is written in the same way people's names are written, within the same structure.</span></span> <span data-ttu-id="38b78-155">Verwenden Sie zum Schreiben der Rechteck Metadaten eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) und den expliziten XMP-Pfad der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="38b78-155">To write the rectangle metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="38b78-156">Im folgenden Codebeispiel wird das vorherige Beispiel fortgesetzt, und es wird ein Rechteck hinzugefügt, das ' John Doe ' für die Metadaten des Bilds darstellt.</span><span class="sxs-lookup"><span data-stu-id="38b78-156">The following code example continues the previous example and adds a rectangle representing 'John Doe' to the image's metadata.</span></span> <span data-ttu-id="38b78-157">Beachten Sie, dass der gleiche `{ulong=0}` Index verwendet wird, um dieses Rechteck "John Doe" zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="38b78-157">Note that it uses the same `{ulong=0}` index to associate this rectangle with 'John Doe'.</span></span>


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a><span data-ttu-id="38b78-158">Schemareferenz</span><span class="sxs-lookup"><span data-stu-id="38b78-158">Schema Reference</span></span>

<span data-ttu-id="38b78-159">Die Microsoft XMP-Schemas für Personen Tags definieren einen Satz von Eigenschaften, um Einzelpersonen in digitalen Fotos zu markieren.</span><span class="sxs-lookup"><span data-stu-id="38b78-159">The Microsoft XMP schemas for people tagging define a set of properties to tag individuals in digital photos.</span></span>

<span data-ttu-id="38b78-160">In den folgenden Abschnitten werden die Schema Definitionen bereitgestellt, die für Personen Tags erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="38b78-160">The following sections provide the schema definitions needed for people tagging.</span></span> <span data-ttu-id="38b78-161">Nach Möglichkeit verwenden die Schema Definitionen die Konventionen, die von den [XMP-Spezifikationen (Extensible Metadata Platform) von Adobe](https://www.adobe.com/devnet/xmp/)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="38b78-161">Wherever possible, the schema definitions use the conventions provided by [Adobe's Extensible Metadata Platform (XMP) Specifications](https://www.adobe.com/devnet/xmp/).</span></span> <span data-ttu-id="38b78-162">Die Schema Definitionen in diesem Thema zeigen den XML-Namespace Uniform Resource Identifier (URI), der das Schema und das bevorzugte Schema Namespace-Präfix identifiziert, gefolgt von einer Tabelle, die alle für das Schema definierten Eigenschaften auflistet.</span><span class="sxs-lookup"><span data-stu-id="38b78-162">The schema definitions in this topic show the XML namespace Uniform Resource Identifier (URI) that identifies the schema and the preferred schema namespace prefix, followed by a table that lists all properties defined for the schema.</span></span> <span data-ttu-id="38b78-163">Jede Tabelle weist die folgenden Spalten auf:</span><span class="sxs-lookup"><span data-stu-id="38b78-163">Each table has the following columns:</span></span>

-   <span data-ttu-id="38b78-164">**Property** : der Name der Eigenschaft, einschließlich des bevorzugten Namespace Präfixes.</span><span class="sxs-lookup"><span data-stu-id="38b78-164">**Property** - The name of the property, including the preferred namespace prefix.</span></span>

-   <span data-ttu-id="38b78-165">**Werttyp** : der Werttyp der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="38b78-165">**Value type** - The value type of the property.</span></span> <span data-ttu-id="38b78-166">Das People-Tagging-Unterstützungs Schema verwendet nach Möglichkeit die XMP-Werttypen, einschließlich Datum und Text.</span><span class="sxs-lookup"><span data-stu-id="38b78-166">The people-tagging support schemas use the XMP value types whenever possible, including Date and Text.</span></span> <span data-ttu-id="38b78-167">Array Typen wird der Containertyp `alt` vorangestellt:, `bag` oder `seq` .</span><span class="sxs-lookup"><span data-stu-id="38b78-167">Array types are preceded by the container type: `alt`, `bag`, or `seq`.</span></span>

-   <span data-ttu-id="38b78-168">**Category** -Schema-Eigenschaften sind intern oder extern:</span><span class="sxs-lookup"><span data-stu-id="38b78-168">**Category** - Schema properties are internal or external:</span></span>

    -   <span data-ttu-id="38b78-169">Interne Metadaten müssen von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="38b78-169">Internal metadata must be set by the application.</span></span>

    -   <span data-ttu-id="38b78-170">Externe Metadaten müssen vom Benutzer festgelegt werden und sind unabhängig vom Inhalt des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="38b78-170">External metadata must be set by the user and is independent of the contents of the document.</span></span>

-   <span data-ttu-id="38b78-171">**Description** : die Beschreibung der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="38b78-171">**Description** - The description of the property.</span></span>

### <a name="microsoft-photo-12-schema"></a><span data-ttu-id="38b78-172">Microsoft-Foto 1,2-Schema</span><span class="sxs-lookup"><span data-stu-id="38b78-172">Microsoft Photo 1.2 Schema</span></span>

<span data-ttu-id="38b78-173">Das Microsoft Photo 1,2-Schema stellt einen Satz von Eigenschaften für Bildbereiche bereit.</span><span class="sxs-lookup"><span data-stu-id="38b78-173">The Microsoft Photo 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="38b78-174">Der Schema Namespace-URI ist `https://ns.microsoft.com/photo/1.2/` .</span><span class="sxs-lookup"><span data-stu-id="38b78-174">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/`.</span></span>
-   <span data-ttu-id="38b78-175">Das bevorzugte Schema Namespace-Präfix ist `MP` .</span><span class="sxs-lookup"><span data-stu-id="38b78-175">The preferred schema namespace prefix is `MP`.</span></span>



| <span data-ttu-id="38b78-176">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38b78-176">Property</span></span>      | <span data-ttu-id="38b78-177">Werttyp</span><span class="sxs-lookup"><span data-stu-id="38b78-177">Value type</span></span> | <span data-ttu-id="38b78-178">Category</span><span class="sxs-lookup"><span data-stu-id="38b78-178">Category</span></span> | <span data-ttu-id="38b78-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38b78-179">Description</span></span>                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b78-180">MP: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="38b78-180">MP:RegionInfo</span></span> | <span data-ttu-id="38b78-181">RegionInfo</span><span class="sxs-lookup"><span data-stu-id="38b78-181">RegionInfo</span></span> | <span data-ttu-id="38b78-182">Intern</span><span class="sxs-lookup"><span data-stu-id="38b78-182">Internal</span></span> | <span data-ttu-id="38b78-183">**erforderlich** : speichert den Stamm der People-Tagging-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="38b78-183">**required** : Stores the root of the people-tagging metadata.</span></span> <span data-ttu-id="38b78-184">Weitere Informationen finden Sie im folgenden Abschnitt des Microsoft Photo RegionInfo-Schemas.</span><span class="sxs-lookup"><span data-stu-id="38b78-184">See the Microsoft Photo RegionInfo Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-regioninfo-schema"></a><span data-ttu-id="38b78-185">Microsoft Photo RegionInfo-Schema</span><span class="sxs-lookup"><span data-stu-id="38b78-185">Microsoft Photo RegionInfo Schema</span></span>

<span data-ttu-id="38b78-186">Das Microsoft Photo RegionInfo 1,2-Schema stellt einen Satz von Eigenschaften für Regions Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="38b78-186">The Microsoft Photo RegionInfo 1.2 schema provides a set of properties for region info.</span></span>

-   <span data-ttu-id="38b78-187">Der Schema Namespace-URI ist `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .</span><span class="sxs-lookup"><span data-stu-id="38b78-187">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/RegionInfo#`.</span></span>
-   <span data-ttu-id="38b78-188">Das bevorzugte Schema Namespace-Präfix ist `MPRI` .</span><span class="sxs-lookup"><span data-stu-id="38b78-188">The preferred schema namespace prefix is `MPRI`.</span></span>



| <span data-ttu-id="38b78-189">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38b78-189">Property</span></span>              | <span data-ttu-id="38b78-190">Werttyp</span><span class="sxs-lookup"><span data-stu-id="38b78-190">Value type</span></span> | <span data-ttu-id="38b78-191">Category</span><span class="sxs-lookup"><span data-stu-id="38b78-191">Category</span></span> | <span data-ttu-id="38b78-192">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38b78-192">Description</span></span>                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b78-193">MPRI: dateregionsvalid</span><span class="sxs-lookup"><span data-stu-id="38b78-193">MPRI:DateRegionsValid</span></span> | <span data-ttu-id="38b78-194">Date</span><span class="sxs-lookup"><span data-stu-id="38b78-194">Date</span></span>       | <span data-ttu-id="38b78-195">Extern</span><span class="sxs-lookup"><span data-stu-id="38b78-195">External</span></span> | <span data-ttu-id="38b78-196">**optional** : Datum, an dem die letzte Region erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="38b78-196">**optional** : Date that the last region was created.</span></span>                                                          |
| <span data-ttu-id="38b78-197">MPRI: Regionen</span><span class="sxs-lookup"><span data-stu-id="38b78-197">MPRI:Regions</span></span>          | <span data-ttu-id="38b78-198">Behälter Bereich</span><span class="sxs-lookup"><span data-stu-id="38b78-198">bag Region</span></span> | <span data-ttu-id="38b78-199">Extern</span><span class="sxs-lookup"><span data-stu-id="38b78-199">External</span></span> | <span data-ttu-id="38b78-200">**erforderlich** : speichert die People-taggingregionen.</span><span class="sxs-lookup"><span data-stu-id="38b78-200">**required** : Stores the people tagging regions.</span></span> <span data-ttu-id="38b78-201">Weitere Informationen finden Sie im folgenden Abschnitt des Microsoft-Foto Regions Schemas.</span><span class="sxs-lookup"><span data-stu-id="38b78-201">See the Microsoft Photo Region Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-region-schema"></a><span data-ttu-id="38b78-202">Microsoft-Foto Regions Schema</span><span class="sxs-lookup"><span data-stu-id="38b78-202">Microsoft Photo Region Schema</span></span>

<span data-ttu-id="38b78-203">Das Microsoft Photo Region 1,2-Schema stellt einen Satz von Eigenschaften für Bildbereiche bereit.</span><span class="sxs-lookup"><span data-stu-id="38b78-203">The Microsoft Photo Region 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="38b78-204">Der Schema Namespace-URI ist `https://ns.microsoft.com/photo/1.2/t/Region#` .</span><span class="sxs-lookup"><span data-stu-id="38b78-204">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/Region#`.</span></span>
-   <span data-ttu-id="38b78-205">Das bevorzugte Schema Namespace-Präfix ist `MPReg` .</span><span class="sxs-lookup"><span data-stu-id="38b78-205">The preferred schema namespace prefix is `MPReg`.</span></span>



| <span data-ttu-id="38b78-206">Mpreg: Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38b78-206">MPReg:Property</span></span>          | <span data-ttu-id="38b78-207">Werttyp</span><span class="sxs-lookup"><span data-stu-id="38b78-207">Value type</span></span> | <span data-ttu-id="38b78-208">Category</span><span class="sxs-lookup"><span data-stu-id="38b78-208">Category</span></span> | <span data-ttu-id="38b78-209">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38b78-209">Description</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b78-210">Mpreg: persondisplayname</span><span class="sxs-lookup"><span data-stu-id="38b78-210">MPReg:PersonDisplayName</span></span> | <span data-ttu-id="38b78-211">Text</span><span class="sxs-lookup"><span data-stu-id="38b78-211">Text</span></span>       | <span data-ttu-id="38b78-212">Extern</span><span class="sxs-lookup"><span data-stu-id="38b78-212">External</span></span> | <span data-ttu-id="38b78-213">**erforderlich** : speichert den Namen der Person im angegebenen Rechteck.</span><span class="sxs-lookup"><span data-stu-id="38b78-213">**required** : Stores the name of the person in the given rectangle.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="38b78-214">Mpreg: Rechteck</span><span class="sxs-lookup"><span data-stu-id="38b78-214">MPReg:Rectangle</span></span>         | <span data-ttu-id="38b78-215">Text</span><span class="sxs-lookup"><span data-stu-id="38b78-215">Text</span></span>       | <span data-ttu-id="38b78-216">Extern</span><span class="sxs-lookup"><span data-stu-id="38b78-216">External</span></span> | <span data-ttu-id="38b78-217">**optional** : speichert das Rechteck, das die Person innerhalb des Fotos identifiziert.</span><span class="sxs-lookup"><span data-stu-id="38b78-217">**optional** : Stores the rectangle that identifies the person within the photo.</span></span> <span data-ttu-id="38b78-218">Das Rechteck wird als vier durch Trennzeichen getrennte Dezimalwerte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="38b78-218">The rectangle is stored as four comma-delimited decimal values.</span></span> <span data-ttu-id="38b78-219">Die ersten beiden Werte geben die obere linke Koordinate an. die letzten beiden geben die Höhe und Breite des Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="38b78-219">The first two values specify the top left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="38b78-220">Die Dezimalwerte müssen auf 1 normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="38b78-220">The decimal values must be normalized to 1.</span></span> |
| <span data-ttu-id="38b78-221">Mpreg: personemaildigest</span><span class="sxs-lookup"><span data-stu-id="38b78-221">MPReg:PersonEmailDigest</span></span> | <span data-ttu-id="38b78-222">Text</span><span class="sxs-lookup"><span data-stu-id="38b78-222">Text</span></span>       | <span data-ttu-id="38b78-223">Extern</span><span class="sxs-lookup"><span data-stu-id="38b78-223">External</span></span> | <span data-ttu-id="38b78-224">**optional** : speichert den SHA-1-verschlüsselten Nachrichten Hash der Live-e-Mail-Adresse der Person.</span><span class="sxs-lookup"><span data-stu-id="38b78-224">**optional** : Stores the SHA-1 encrypted message hash of the person's Live e-mail address.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="38b78-225">Mpreg: personliveidcid</span><span class="sxs-lookup"><span data-stu-id="38b78-225">MPReg:PersonLiveIdCID</span></span>   | <span data-ttu-id="38b78-226">Text</span><span class="sxs-lookup"><span data-stu-id="38b78-226">Text</span></span>       | <span data-ttu-id="38b78-227">Extern</span><span class="sxs-lookup"><span data-stu-id="38b78-227">External</span></span> | <span data-ttu-id="38b78-228">**optional** : speichert die signierte Dezimal Darstellung der Live-CID der Person, einer 64-Bit-Ganzzahl, die eine Live Identität öffentlich identifiziert.</span><span class="sxs-lookup"><span data-stu-id="38b78-228">**optional** :Stores the signed decimal representation of the person's Live CID, a 64-bit integer that publicly identifies a Live identity.</span></span>                                                                                                                                                                     |



 

### <a name="sample-metadata"></a><span data-ttu-id="38b78-229">Beispiel Metadaten</span><span class="sxs-lookup"><span data-stu-id="38b78-229">Sample Metadata</span></span>

<span data-ttu-id="38b78-230">Im folgenden finden Sie eine Darstellung der XMP-Metadaten für Personen Tags.</span><span class="sxs-lookup"><span data-stu-id="38b78-230">The following is a representation of the XMP metadata for people tagging.</span></span>

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a><span data-ttu-id="38b78-231">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38b78-231">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="38b78-232">**Licher**</span><span class="sxs-lookup"><span data-stu-id="38b78-232">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38b78-233">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="38b78-233">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="38b78-234">Übersicht über WIC-Metadaten</span><span class="sxs-lookup"><span data-stu-id="38b78-234">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="38b78-235">Übersicht über das Lesen und Schreiben von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="38b78-235">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="38b78-236">Übersicht über die Metadaten-Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="38b78-236">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
