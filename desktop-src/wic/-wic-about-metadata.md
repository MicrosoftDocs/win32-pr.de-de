---
description: In diesem Thema wird die von der Windows Imaging Component (WIC) bereitgestellte Abbild Erstellung für Metadatenunterstützung eingeführt.
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Übersicht über WIC-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557743"
---
# <a name="wic-metadata-overview"></a><span data-ttu-id="c6e6b-103">Übersicht über WIC-Metadaten</span><span class="sxs-lookup"><span data-stu-id="c6e6b-103">WIC Metadata Overview</span></span>

<span data-ttu-id="c6e6b-104">In diesem Thema wird die von der Windows Imaging Component (WIC) bereitgestellte Abbild Erstellung für Metadatenunterstützung eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-104">This topic introduces the imaging metadata support provided by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="c6e6b-105">Er bietet eine Einführung in das Lesen und Schreiben von Bild Metadaten, die Metadatenabfragesprache und die Erweiterbarkeit von metadatenhandlern.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-105">It provides an introduction to reading and writing image metadata, the metadata query language, and metadata handler extensibility.</span></span>

<span data-ttu-id="c6e6b-106">Bild Metadaten sind Daten, die in eine Bilddatei eingebettet sind, die zusätzliche Informationen zum Bild bereitstellt, z. b. das Gerät, das zum Erfassen des Bilds oder der Abmessungen des Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-106">Image metadata is data embedded inside an image file that provides additional information about the image, such as the device used to capture the image or the dimensions of the image.</span></span> <span data-ttu-id="c6e6b-107">Obwohl Sie in der Bilddatei selbst enthalten ist, sind diese Metadaten nicht Teil der Renderingdaten.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-107">Although it is contained within the image file itself, this metadata is not part of the rendering data.</span></span> <span data-ttu-id="c6e6b-108">WIC stellt Schnittstellen bereit, die es Ihnen ermöglichen, diese Metadaten für verschiedene gängige Metadatenformate zu lesen und zu schreiben, z. b. erweiterbare metadatenplattform (XMP), austauschbare Bilddatei (EXIF) und PNG-Textdaten (Text).</span><span class="sxs-lookup"><span data-stu-id="c6e6b-108">WIC provides interfaces that enable you to read and write this metadata for several common metadata formats including Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF), and Png Textual Data (tEXt).</span></span>

<span data-ttu-id="c6e6b-109">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c6e6b-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c6e6b-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c6e6b-110">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="c6e6b-111">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="c6e6b-112">Lesen von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="c6e6b-112">Reading Image Metadata</span></span>](#reading-image-metadata)
-   [<span data-ttu-id="c6e6b-113">Schreiben von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="c6e6b-113">Writing Image Metadata</span></span>](#writing-image-metadata)
-   [<span data-ttu-id="c6e6b-114">Metadatenerweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="c6e6b-114">Metadata Extensibility</span></span>](#metadata-extensibility)
-   [<span data-ttu-id="c6e6b-115">Unterstützte Metadatenformate</span><span class="sxs-lookup"><span data-stu-id="c6e6b-115">Supported Metadata Formats</span></span>](#supported-metadata-formats)
-   [<span data-ttu-id="c6e6b-116">Metadatenkomponentenübersicht</span><span class="sxs-lookup"><span data-stu-id="c6e6b-116">Metadata Component Summary</span></span>](#metadata-component-summary)
-   [<span data-ttu-id="c6e6b-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6e6b-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="c6e6b-118">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c6e6b-118">Prerequisites</span></span>

<span data-ttu-id="c6e6b-119">Um dieses Thema zu verstehen, sollten Sie mit den WIC-Encodern und-decoderschnittstellen und den zugehörigen COM-Komponenten (Related Component Object Model) vertraut sein, wie in der [Übersicht über Windows Imaging Component](-wic-about-windows-imaging-codec.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-119">To understand this topic, you should be familiar with the WIC encoder and decoder interfaces and their related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="c6e6b-120">Außerdem ist es hilfreich, eine allgemeine Vertrautheit mit einigen der heute verwendeten Abbild Erstellungs Metadatenformate zu haben.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-120">It also helps to have a general familiarity with some of the imaging metadata formats in use today.</span></span>

## <a name="introduction"></a><span data-ttu-id="c6e6b-121">Einführung</span><span class="sxs-lookup"><span data-stu-id="c6e6b-121">Introduction</span></span>

<span data-ttu-id="c6e6b-122">Metadaten stellen erweiterte Informationen zu einem Bild bereit.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-122">Metadata provides extended information about an image.</span></span> <span data-ttu-id="c6e6b-123">Diese Informationen können auf verschiedene Weise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-123">This information can be used in several ways.</span></span> <span data-ttu-id="c6e6b-124">Ein Image kann Metadaten enthalten, wie z. b. eine Beschreibung, eine Bewertung, kategorietags und Copyright Informationen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-124">An image might contain metadata such as a description, rating, category tags, and copyright information.</span></span> <span data-ttu-id="c6e6b-125">Der Zugriff auf die Metadaten erleichtert das Ausführen von Aufgaben wie z. b. Asset Management, Datei Speicherort oder die Bestimmung von Copyright Informationen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-125">Accessing the metadata makes it easier to perform tasks such as asset management, file location, or determining copyright information.</span></span> <span data-ttu-id="c6e6b-126">Beispielsweise können Sie mit der Windows-Fotogalerie in Windows Vista den Bildern Beschreibungen und kategorietags hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-126">For example, the Windows Photo Gallery in Windows Vista enables you to add descriptions and category tags to images.</span></span> <span data-ttu-id="c6e6b-127">Dies ermöglicht eine bessere Auffindbarkeit von Bildern und eine bequeme Möglichkeit zum Kategorisieren von Bildern.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-127">This allows for better discoverability of images and a convenient way to categorize images.</span></span> <span data-ttu-id="c6e6b-128">Mithilfe der WIC-APIs und der allgemeinen Metadatenformate können Anwendungen diese Art von Metadaten problemlos in oder aus Bildern schreiben oder lesen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-128">Using the WIC APIs and common metadata formats, applications can easily write or read this type of metadata to or from images.</span></span>

<span data-ttu-id="c6e6b-129">Das folgende Diagramm veranschaulicht den Inhalt einer JPEG-Datei, die eingebettete Metadatenblöcke und Metadatenelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-129">The following diagram illustrates the contents of a JPEG file that includes embedded metadata blocks and metadata items.</span></span>

![JPEG-Bild mit Bewertungs Metadaten](graphics/jpeg.png)

<span data-ttu-id="c6e6b-131">In diesem Beispiel Bild werden die Metadaten in die Bilddatei innerhalb eines Bild Rahmens eingebettet.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-131">In this example image, the metadata is embedded in the image file within an image frame.</span></span> <span data-ttu-id="c6e6b-132">Das JPEG-Format unterstützt nicht mehrere Bild Rahmen, sodass die Metadaten konzeptionell mit diesem einzelnen Frame verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-132">The JPEG format does not support multiple image frames, so the metadata is conceptually attached to this single frame.</span></span> <span data-ttu-id="c6e6b-133">Bei Formaten, die mehrere Frames unterstützen (z. b. TIFF), können Metadaten an jeden Bildframe angefügt werden, wie in diesem Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-133">Formats that support multiple frames, such as TIFF, may have metadata attached to each image frame as this diagram shows.</span></span> <span data-ttu-id="c6e6b-134">Obwohl es heute nicht üblich und nicht von den Codecs für Native Images unterstützt wird, können einige Bildformate auch Metadaten außerhalb eines Bild Rahmens unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-134">Though not common today and not supported by the native image codecs, some image formats may also support metadata outside of an image frame.</span></span> <span data-ttu-id="c6e6b-135">WIC ist flexibel genug, um sowohl Metadaten und Metadaten auf Frame-Ebene außerhalb des einzelnen Frames eines Bilds zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-135">WIC is flexible enough to handle both frame-level metadata and metadata outside of an image's individual frame.</span></span>

## <a name="reading-image-metadata"></a><span data-ttu-id="c6e6b-136">Lesen von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="c6e6b-136">Reading Image Metadata</span></span>

<span data-ttu-id="c6e6b-137">Die WIC-APIs stellen COM-Komponenten bereit, die es Anwendungen erleichtern, Bild Metadaten zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-137">The WIC APIs provide COM components that make it easy for applications to read and write image metadata.</span></span>

<span data-ttu-id="c6e6b-138">Die primäre Methode zum Lesen von Metadaten ist die Verwendung eines Metadatenabfrage-Readers ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) für den Zugriff auf bestimmte Metadatenelemente.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-138">The primary way to read metadata is to use a metadata query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) to access specific metadata items.</span></span> <span data-ttu-id="c6e6b-139">Die Komponente für die Metadatenabfrage-Reader wird durch den Codec implementiert, und der Zugriff auf die decoderebene oder über einzelne Bild Rahmen ist die gängigste Methode.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-139">The metadata query reader component is implemented by the codec and can be accessed at the decoder level or through individual image frames, which is the more common method.</span></span> <span data-ttu-id="c6e6b-140">Der folgende Code zeigt, wie Sie mithilfe der **GetMetadataQueryReader** -Methode des Abfrage Readers auf einen Abfrage Reader für einen einzelnen Frame zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-140">The following code demonstrates how to access a query reader for an individual frame by using the query reader's **GetMetadataQueryReader** method.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="c6e6b-141">Ein Abfrage Reader stellt Methoden zum Abrufen von Informationen über bestimmte Metadaten und eine Möglichkeit zum Angeben eines abzurufenden Metadatenelements bereit.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-141">A query reader provides methods to obtain information about specific metadata, and a means to specify a metadata item to retrieve.</span></span> <span data-ttu-id="c6e6b-142">Im folgenden Code wird ein Abfrage Ausdruck verwendet, um ein bestimmtes Metadatenelement im IFD-Block (App1 geschachteltes Image Dateiverzeichnis) anzufordern.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-142">The following code uses a query expression to request a specific metadata item within the App1 nested image file directory (IFD) block.</span></span> <span data-ttu-id="c6e6b-143">Dies erfolgt mithilfe der **GetMetadataByName** -Methode des Abfrage Readers.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-143">This is done by using the query reader's **GetMetadataByName** method.</span></span> <span data-ttu-id="c6e6b-144">Der folgende Code veranschaulicht die Verwendung des Abfrage Readers zum Abrufen des microsoftphoto-Bewertungs Werts.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-144">The following code demonstrates using the query reader to obtain the MicrosoftPhoto rating value.</span></span>


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



<span data-ttu-id="c6e6b-145">Die Variable pwzratingquery im vorherigen Beispiel ist die Abfrage Zeichenfolge für den Zugriff auf das Metadatenelement microsoftphoto-Bewertung.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-145">The pwzRatingQuery variable in the preceding example is the query string to access the metadata item MicrosoftPhoto rating.</span></span> <span data-ttu-id="c6e6b-146">Diese Zeichenfolge wird mithilfe der Metadatenabfrage-Sprache erstellt.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-146">This string is created by using the metadata query language.</span></span> <span data-ttu-id="c6e6b-147">Um diese Zeichenfolge zu erstellen, sind Kenntnisse über das Metadatenformat und die Metadatenabfrage Sprache erforderlich, um einzelne Metadatenelemente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-147">To create this string, knowledge of the metadata format and the metadata query language is needed to retrieve individual metadata items.</span></span> <span data-ttu-id="c6e6b-148">Weitere Informationen zur Metadatenabfragesprache finden Sie in der [Übersicht über die metadatenquery-Sprache](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="c6e6b-148">For more information about the metadata query language, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

<span data-ttu-id="c6e6b-149">Im Hintergrund verwendet ein Abfrage Leser einen metadatenreader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)), um auf die vom Abfrage Ausdruck beschriebenen Metadaten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-149">Behind the scenes, a query reader uses a metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) to access the metadata described by the query expression.</span></span> <span data-ttu-id="c6e6b-150">Zusätzlich zur Verwendung eines Abfrage Readers können Sie auch direkt auf einen metadatenreader zugreifen, um Metadaten zu lesen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-150">In addition to using a query reader, you can also access a metadata reader directly to read metadata.</span></span> <span data-ttu-id="c6e6b-151">Sie können einen metadatenleser vom Decoder oder einzelnen Frames abrufen, indem Sie eine [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)-Schnittstelle (Block Reader) Abfragen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-151">You can obtain a metadata reader from the decoder or individual frames by querying for a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) interface.</span></span>

## <a name="writing-image-metadata"></a><span data-ttu-id="c6e6b-152">Schreiben von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="c6e6b-152">Writing Image Metadata</span></span>

<span data-ttu-id="c6e6b-153">Der Prozess zum Schreiben von Metadaten ähnelt der Vorgehensweise zum Lesen, mit der Ausnahme, dass ein Metadatenabfrage-Writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-153">The process of writing metadata is similar to the way it is read except that a metadata query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used.</span></span> <span data-ttu-id="c6e6b-154">Die Query Writer-Schnittstelle wird vom Bild Encoder implementiert, und wie im Abfrage Reader erfolgt der Zugriff auf Metadaten sowohl im Encoder als auch in einzelnen Frames (abhängig von der Unterstützung des Bildformats).</span><span class="sxs-lookup"><span data-stu-id="c6e6b-154">The query writer interface is implemented by the image encoder and, as in the query reader, metadata is accessed both on the encoder and on individual frames (depending on image format support).</span></span>

<span data-ttu-id="c6e6b-155">Der folgende Code veranschaulicht, wie Sie einen Abfrage-Writer von einem encoderframe abrufen und den zuvor gelesenen Bewertungs Wert entfernen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-155">The following code demonstrates how to obtain a query writer from an encoder frame and remove the rating value that was previously read.</span></span>


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



<span data-ttu-id="c6e6b-156">Eine andere Möglichkeit zum Schreiben von Metadaten ist das schnelle Aktualisieren von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-156">Another way to write metadata is through fast metadata updates.</span></span> <span data-ttu-id="c6e6b-157">Die schnelle metadatencodierung ist eine Möglichkeit zum Schreiben von Bild Metadaten, ohne eine Bilddatei erneut codieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-157">Fast metadata encoding is a way to write image metadata without having to re-encode an image file.</span></span> <span data-ttu-id="c6e6b-158">Dies erfolgt durch das Schreiben neuer Metadateninformationen in einen aufgefüllten Bereich des metadatenformats.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-158">This is done by writing new metadata information to a padded region of the metadata format.</span></span> <span data-ttu-id="c6e6b-159">Der fast Metadata Encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) wird aus der komponentenfactory abgerufen, basierend auf dem Image Decoder.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-159">The fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) is obtained from the component factory, based on the image decoder.</span></span> <span data-ttu-id="c6e6b-160">Der schnelle metadatenencoder erhält dann einen Abfrage-Writer, der zum Schreiben der Metadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-160">The fast metadata encoder then obtains a query writer that is used to write the metadata.</span></span> <span data-ttu-id="c6e6b-161">Schließlich führt der schnelle Encoder einen Commit für die Änderung aus.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-161">Finally, the fast encoder commits the change.</span></span>

<span data-ttu-id="c6e6b-162">Der folgende Code veranschaulicht, wie Sie einen schnellen metadatenencoder abrufen und ihn verwenden, um den Wert für die Erstellung von mikrosoftrating zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-162">The following code demonstrates how to obtain a fast metadata encoder and use it to write the MicrosoftRating value.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

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



<span data-ttu-id="c6e6b-163">Nicht alle Metadatenformate unterstützen schnelle Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-163">Not all metadata formats support fast metadata.</span></span> <span data-ttu-id="c6e6b-164">Informationen dazu, welche nativ unterstützten Formate eine schnelle metadatencodierung unterstützen, finden Sie in der Tabelle im Abschnitt [unterstützte Metadatenformate](#supported-metadata-formats) weiter unten in diesem Dokument.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-164">To see which natively supported formats support fast metadata encoding, see the table in the [Supported Metadata Formats](#supported-metadata-formats) section later in this document.</span></span>

<span data-ttu-id="c6e6b-165">Im Hintergrund verwendet ein Abfrage Schreiber einen metadatenwriter ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)), um die vom Abfrage Ausdruck beschriebenen Metadaten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-165">Behind the scenes, a query writer uses a metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) to write the metadata described by the query expression.</span></span> <span data-ttu-id="c6e6b-166">Zusätzlich zur Verwendung eines Abfrage Readers können Sie auch direkt auf einen metadatenwriter zugreifen, um Metadaten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-166">In addition to using a query reader, you can also access a metadata writer directly to write metadata.</span></span> <span data-ttu-id="c6e6b-167">Sie können einen metadatenwriter vom Decoder oder einzelnen Frames abrufen, indem Sie Abfragen für eine blockwriter-Schnittstelle ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-167">You can obtain a metadata writer from the decoder or individual frames using querying for a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) interface.</span></span>

## <a name="metadata-extensibility"></a><span data-ttu-id="c6e6b-168">Metadatenerweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="c6e6b-168">Metadata Extensibility</span></span>

<span data-ttu-id="c6e6b-169">Wie bereits erwähnt, stellt WIC mehrere Metadatenhandler bereit, um Metadaten für gängige Metadatenformate zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-169">As mentioned previously, WIC provides several metadata handlers to read and write metadata for common metadata formats.</span></span> <span data-ttu-id="c6e6b-170">Es gibt jedoch einige Metadatenformate, die nicht nativ unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-170">However, there are some metadata formats that are not natively supported.</span></span> <span data-ttu-id="c6e6b-171">Daher stellt WIC APIs zum Erstellen zusätzlicher Metadatenhandler bereit, mit denen die Metadatenunterstützung in andere Formate erweitert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-171">Therefore, WIC provides APIs for creating additional metadata handlers that can extend metadata support to other formats.</span></span>

<span data-ttu-id="c6e6b-172">Um andere Metadatenformate vollständig zu unterstützen, müssen zwei Arten von Handlern entwickelt werden – ein metadatenleser zum Lesen von Metadaten und ein metadatenwriter zum Schreiben von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-172">To fully support other metadata formats, two types of handlers must be developed — a metadata reader to read metadata and a metadata writer to write metadata.</span></span> <span data-ttu-id="c6e6b-173">Obwohl diese beiden Handler in der Regel in Paaren für ein bestimmtes Format implementiert werden, ist dies nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-173">Although these two handlers are usually implemented in pairs for a specific format, that is not a requirement.</span></span> <span data-ttu-id="c6e6b-174">Es gibt möglicherweise Fälle, in denen nur die Lesefähigkeit oder nur die Schreibfähigkeit erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-174">There might be some cases in which only the read ability or only the write ability is needed.</span></span>

<span data-ttu-id="c6e6b-175">Weitere Informationen zur Erweiterbarkeit von Metadaten mithilfe der WIC-APIs finden Sie in der [Übersicht über die metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md).</span><span class="sxs-lookup"><span data-stu-id="c6e6b-175">For more information on metadata extensibility using the WIC APIs, see the [Metadata Extensibility Overview](-wic-codec-metadatahandlers.md).</span></span>

## <a name="supported-metadata-formats"></a><span data-ttu-id="c6e6b-176">Unterstützte Metadatenformate</span><span class="sxs-lookup"><span data-stu-id="c6e6b-176">Supported Metadata Formats</span></span>

<span data-ttu-id="c6e6b-177">WIC bietet Unterstützung für verschiedene gängige Metadatenformate.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-177">WIC provides support for several common metadata formats.</span></span> <span data-ttu-id="c6e6b-178">In der folgenden Tabelle werden die unterstützten Metadatenformate, ihre Versionen, die Bildformate aufgelistet, die das Metadatenformat unterstützen, und ob das Metadatenformat eine schnelle metadatencodierung unterstützt</span><span class="sxs-lookup"><span data-stu-id="c6e6b-178">The following table lists the supported metadata formats, their versions, the image formats that support the metadata format, and whether the metadata format supports fast metadata encoding.</span></span> <span data-ttu-id="c6e6b-179">Weitere Informationen zur schnellen metadatencodierung finden Sie weiter oben in diesem Dokument im Abschnitt [Schreiben von Image Metadaten](#writing-image-metadata) .</span><span class="sxs-lookup"><span data-stu-id="c6e6b-179">For more information about fast metadata encoding, see the [Writing Image Metadata](#writing-image-metadata) section earlier in this document.</span></span>



| <span data-ttu-id="c6e6b-180">Unterstützte Metadatenformate</span><span class="sxs-lookup"><span data-stu-id="c6e6b-180">Supported metadata formats</span></span> | <span data-ttu-id="c6e6b-181">Metadatenspezifikations Version</span><span class="sxs-lookup"><span data-stu-id="c6e6b-181">Metadata specification version</span></span> | <span data-ttu-id="c6e6b-182">Unterstützung für Bildformate</span><span class="sxs-lookup"><span data-stu-id="c6e6b-182">Image format support</span></span> | <span data-ttu-id="c6e6b-183">Unterstützt die schnelle metadatencodierung</span><span class="sxs-lookup"><span data-stu-id="c6e6b-183">Supports fast metadata encoding</span></span> |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| <span data-ttu-id="c6e6b-184">App0</span><span class="sxs-lookup"><span data-stu-id="c6e6b-184">App0</span></span>                       | <span data-ttu-id="c6e6b-185">Jspf 1,02</span><span class="sxs-lookup"><span data-stu-id="c6e6b-185">JFIF 1.02</span></span>                      | <span data-ttu-id="c6e6b-186">JPEG</span><span class="sxs-lookup"><span data-stu-id="c6e6b-186">JPEG</span></span>                 | <span data-ttu-id="c6e6b-187">Nein</span><span class="sxs-lookup"><span data-stu-id="c6e6b-187">No</span></span>                              |
| <span data-ttu-id="c6e6b-188">App1</span><span class="sxs-lookup"><span data-stu-id="c6e6b-188">App1</span></span>                       | <span data-ttu-id="c6e6b-189">Jspf 1,02</span><span class="sxs-lookup"><span data-stu-id="c6e6b-189">JFIF 1.02</span></span>                      | <span data-ttu-id="c6e6b-190">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-190">JPEG, TIFF</span></span>           | <span data-ttu-id="c6e6b-191">Nein</span><span class="sxs-lookup"><span data-stu-id="c6e6b-191">No</span></span>                              |
| <span data-ttu-id="c6e6b-192">App13</span><span class="sxs-lookup"><span data-stu-id="c6e6b-192">App13</span></span>                      | <span data-ttu-id="c6e6b-193">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c6e6b-193">Unknown</span></span>                        | <span data-ttu-id="c6e6b-194">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-194">JPEG, TIFF</span></span>           | <span data-ttu-id="c6e6b-195">Nein</span><span class="sxs-lookup"><span data-stu-id="c6e6b-195">No</span></span>                              |
| <span data-ttu-id="c6e6b-196">IFD</span><span class="sxs-lookup"><span data-stu-id="c6e6b-196">IFD</span></span>                        | <span data-ttu-id="c6e6b-197">TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="c6e6b-197">TIFF 6.0</span></span>                       | <span data-ttu-id="c6e6b-198">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-198">JPEG, TIFF</span></span>           | <span data-ttu-id="c6e6b-199">Ja</span><span class="sxs-lookup"><span data-stu-id="c6e6b-199">Yes</span></span>                             |
| <span data-ttu-id="c6e6b-200">UNB</span><span class="sxs-lookup"><span data-stu-id="c6e6b-200">IRB</span></span>                        | <span data-ttu-id="c6e6b-201">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c6e6b-201">Unknown</span></span>                        | <span data-ttu-id="c6e6b-202">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-202">JPEG, TIFF</span></span>           | <span data-ttu-id="c6e6b-203">Nein</span><span class="sxs-lookup"><span data-stu-id="c6e6b-203">No</span></span>                              |
| <span data-ttu-id="c6e6b-204">EXIF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-204">Exif</span></span>                       | <span data-ttu-id="c6e6b-205">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="c6e6b-205">Exif 2.2</span></span>                       | <span data-ttu-id="c6e6b-206">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-206">JPEG, TIFF</span></span>           | <span data-ttu-id="c6e6b-207">Ja</span><span class="sxs-lookup"><span data-stu-id="c6e6b-207">Yes</span></span>                             |
| <span data-ttu-id="c6e6b-208">XMP</span><span class="sxs-lookup"><span data-stu-id="c6e6b-208">XMP</span></span>                        | <span data-ttu-id="c6e6b-209">XMP 1,0 (September 2005)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-209">XMP 1.0 (Sept 2005)</span></span>            | <span data-ttu-id="c6e6b-210">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-210">JPEG, TIFF</span></span>           | <span data-ttu-id="c6e6b-211">Ja</span><span class="sxs-lookup"><span data-stu-id="c6e6b-211">Yes</span></span>                             |
| <span data-ttu-id="c6e6b-212">GPS</span><span class="sxs-lookup"><span data-stu-id="c6e6b-212">GPS</span></span>                        | <span data-ttu-id="c6e6b-213">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="c6e6b-213">Exif 2.2</span></span>                       | <span data-ttu-id="c6e6b-214">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-214">JPEG, TIFF</span></span>           | <span data-ttu-id="c6e6b-215">Ja</span><span class="sxs-lookup"><span data-stu-id="c6e6b-215">Yes</span></span>                             |
| <span data-ttu-id="c6e6b-216">IPTC</span><span class="sxs-lookup"><span data-stu-id="c6e6b-216">IPTC</span></span>                       | <span data-ttu-id="c6e6b-217">IPTC 4,0</span><span class="sxs-lookup"><span data-stu-id="c6e6b-217">IPTC 4.0</span></span>                       | <span data-ttu-id="c6e6b-218">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e6b-218">JPEG, TIFF</span></span>           | <span data-ttu-id="c6e6b-219">Ja</span><span class="sxs-lookup"><span data-stu-id="c6e6b-219">Yes</span></span>                             |
| <span data-ttu-id="c6e6b-220">Text</span><span class="sxs-lookup"><span data-stu-id="c6e6b-220">tEXt</span></span>                       | <span data-ttu-id="c6e6b-221">PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="c6e6b-221">PNG 1.2</span></span>                        | <span data-ttu-id="c6e6b-222">PNG</span><span class="sxs-lookup"><span data-stu-id="c6e6b-222">PNG</span></span>                  | <span data-ttu-id="c6e6b-223">Nein</span><span class="sxs-lookup"><span data-stu-id="c6e6b-223">No</span></span>                              |



 

> [!Note]  
> <span data-ttu-id="c6e6b-224">IPTC unterstützt nur dann den Befehl "f", wenn die Blöcke vergrößert werden, da IPTC keine Auffüll Zeichen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-224">IPTC only supports FME if the blocks grow in size, as IPTC does not support padding.</span></span>

 

## <a name="metadata-component-summary"></a><span data-ttu-id="c6e6b-225">Metadatenkomponentenübersicht</span><span class="sxs-lookup"><span data-stu-id="c6e6b-225">Metadata Component Summary</span></span>

<span data-ttu-id="c6e6b-226">In der folgenden Tabelle werden die WIC-Schnittstellen beschrieben, die Metadaten unterstützen, sowie die entsprechenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-226">The following table describes the WIC interfaces that support metadata, and their corresponding components.</span></span> <span data-ttu-id="c6e6b-227">Diese Komponenten ermöglichen den Zugriff auf die Metadaten eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-227">These components provide the access to an image's metadata.</span></span> <span data-ttu-id="c6e6b-228">Weitere Informationen zu diesen Komponenten finden Sie unter Übersicht über die [Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="c6e6b-228">For more information about these components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6e6b-229">Komponente</span><span class="sxs-lookup"><span data-stu-id="c6e6b-229">Component</span></span></th>
<th><span data-ttu-id="c6e6b-230">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6e6b-230">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6e6b-231">Bitmap-Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-231">Bitmap Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-232">Liest einen Bildstream und erzeugt eine verwendbare Bitmapquelle.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-232">Reads an image stream and produces a usable bitmap source.</span></span> <span data-ttu-id="c6e6b-233">Ist einem Containerformat zugeordnet, z. b. Tagged Image File Format (TIFF) oder Joint Photographic Experts Group (JPEG).</span><span class="sxs-lookup"><span data-stu-id="c6e6b-233">Associated with a container format such as Tagged Image File Format (TIFF) or Joint Photographic Experts Group (JPEG).</span></span></li>
<li><span data-ttu-id="c6e6b-234">Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> -Schnittstelle, um alle Metadatenblöcke im Datenstrom des Decoders aufzulisten, die sich nicht in einem Frame befinden.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-234">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the decoder's data stream that are not inside a frame.</span></span></li>
<li><span data-ttu-id="c6e6b-235">Macht einen Abfrage Reader zum Lesen der Metadaten verfügbar, die dem Bild zugeordnet sind, das sich nicht in einem Frame befindet.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-235">Exposes a query reader to read the metadata associated with the image that is not inside a frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6e6b-236">Bitmap-Frame-Decodierung (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-236">Bitmap Frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-237">Greift auf einzelne Frames aus dem Bildstream zu, der vom Decoder gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-237">Accesses individual frames from the image stream held by the decoder.</span></span></li>
<li><span data-ttu-id="c6e6b-238">Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> -Schnittstelle, um alle Metadatenblöcke im Datenstrom des Frames aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-238">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the frame's data stream.</span></span></li>
<li><span data-ttu-id="c6e6b-239">Macht einen Abfrage Reader zum Lesen der mit dem Frame verknüpften Metadaten mithilfe von Abfrage Ausdrücken verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-239">Exposes a query reader to read the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6e6b-240">Bitmap-Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>iwicbitmapcoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-240">Bitmap Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-241">Schreibt eine Bitmap-Quelle in einen Bildstream.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-241">Writes a bitmap source to an image stream.</span></span> <span data-ttu-id="c6e6b-242">Einem Containerformat wie TIFF oder JPEG zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-242">Associated with a container format such as TIFF or JPEG.</span></span></li>
<li><span data-ttu-id="c6e6b-243">Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> -Schnittstelle zum Erstellen einer Liste von metadatenblöcken, die in den Datenstream des Encoders geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-243">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the data stream of the encoder.</span></span></li>
<li><span data-ttu-id="c6e6b-244">Macht mithilfe von Abfrage Ausdrücken einen Abfrage Schreiber zum Schreiben der Metadaten verfügbar, die dem Image zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-244">Exposes a query writer to write the metadata associated with the image, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6e6b-245">Bitma-Frame Codierung (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>iwicbitmapframecocode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-245">Bitma Frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-246">Erstellt einen Frame, der in den vom Encoder gehaltenen Stream codiert wird.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-246">Creates a frame that will be encoded into the stream held by the encoder.</span></span></li>
<li><span data-ttu-id="c6e6b-247">Implementiert eine <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> -Schnittstelle zum Erstellen einer Liste von metadatenblöcken, die in den Datenstrom des Frames geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-247">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the frame's data stream.</span></span></li>
<li><span data-ttu-id="c6e6b-248">Macht einen Abfrage-Writer zum Schreiben der mit dem Frame verknüpften Metadaten mithilfe von Abfrage Ausdrücken verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-248">Exposes a query writer to write the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c6e6b-249">In der folgenden Tabelle werden die WIC-Metadatenkomponenten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-249">The following table describes the WIC metadata components.</span></span> <span data-ttu-id="c6e6b-250">Diese Komponenten ermöglichen es Ihnen, die Metadaten in einem Bild zu lesen und zu schreiben, das von den in der vorherigen Tabelle aufgeführten Komponenten verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-250">These components enable you to read and write the metadata in an image exposed by the components listed in the previous table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6e6b-251">Komponente</span><span class="sxs-lookup"><span data-stu-id="c6e6b-251">Component</span></span></th>
<th><span data-ttu-id="c6e6b-252">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6e6b-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6e6b-253">Metadatenabfrage-Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-253">Metadata Query Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-254">Nimmt eine Abfrage Zeichenfolge und navigiert die zugrunde liegende Metadatenhierarchie, um Metadaten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-254">Takes a query string and navigates the underlying metadata hierarchy to get metadata.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6e6b-255">Metadatenabfrage-Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-255">Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-256">Nimmt eine Abfrage Zeichenfolge und navigiert die zugrunde liegende Metadatenhierarchie, um Metadaten zu erhalten, festzulegen und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-256">Takes a query string and navigates the underlying metadata hierarchy to get, set, and remove metadata.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6e6b-257">Metadatenblockreader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-257">Metadata Block Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-258">Verwaltet eine schreibgeschützte Auflistung von <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> -Objekten am Anfang der Metadatenhierarchie und ermöglicht die Enumeration aller Metadatenblöcke.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-258">Manages a read-only collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> objects at the top of the metadata hierarchy and enables enumeration of all metadata blocks.</span></span></li>
<li><span data-ttu-id="c6e6b-259">Wird von einem Bitmap-Decoder und einem decodierten BitmapFrame implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-259">Implemented by a bitmap decoder and a decoded bitmap frame.</span></span></li>
<li><span data-ttu-id="c6e6b-260">Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Codecs implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-260">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6e6b-261">Metadatenblockwriter (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-261">Metadata Block Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-262">Verwaltet eine Lese-und Schreib Auflistung von <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> -Objekten am Anfang der Metadatenhierarchie.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-262">Manages a read and write collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> objects at the top of the metadata hierarchy.</span></span></li>
<li><span data-ttu-id="c6e6b-263">Wird von einem Bitmap-Encoder und einem Bitmap-Frame codieren implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-263">Implemented by a bitmap encoder and a bitmap frame encode.</span></span></li>
<li><span data-ttu-id="c6e6b-264">Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Codecs implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-264">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6e6b-265">Metadatenleser (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-265">Metadata Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-266">Analysiert einen Datenstrom von Metadaten und verwaltet eine schreibgeschützte Auflistung der Metadatenelemente.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-266">Parses a stream of metadata and manages a read-only collection of the metadata items.</span></span> <span data-ttu-id="c6e6b-267">Zugeordnet mit einem Metadatenformat wie "EXIF", "IFD" und "XMP".</span><span class="sxs-lookup"><span data-stu-id="c6e6b-267">Associated with a metadata format such as EXIF, IFD, and XMP.</span></span></li>
<li><span data-ttu-id="c6e6b-268">Fungiert als Wörterbuch und gibt einen Wert zurück, wenn ein Format und ein ID-Paar angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-268">Acts as a dictionary, returning a value when given a format and ID pair.</span></span></li>
<li><span data-ttu-id="c6e6b-269">Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Metadatentypen implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-269">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6e6b-270">Metadatenwriter (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c6e6b-270">Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-271">Analysiert und serialisiert einen Datenstrom von Metadaten und verwaltet eine Lese-/schreibeigenauflistung von Metadatenelementen.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-271">Parses and serializes a stream of metadata and manages a read/write collection of metadata items.</span></span></li>
<li><span data-ttu-id="c6e6b-272">Wird von Komponentenentwicklern von Drittanbietern für benutzerdefinierte Metadatentypen implementiert.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-272">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6e6b-273">Schneller metadatenencoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6e6b-273">Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span></span></td>
<td><ul>
<li><span data-ttu-id="c6e6b-274">Macht Semantik zum Schreiben in einer Metadatenhierarchie verfügbar, die Metadaten an einem Ort aktualisiert, ohne das Bild neu zu codieren.</span><span class="sxs-lookup"><span data-stu-id="c6e6b-274">Exposes semantics for writing on a metadata hierarchy that will update metadata in place without re-encoding the image.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c6e6b-275">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6e6b-275">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c6e6b-276">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c6e6b-276">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c6e6b-277">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="c6e6b-277">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="c6e6b-278">Übersicht über die Metadaten-Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="c6e6b-278">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="c6e6b-279">Übersicht über das Lesen und Schreiben von Bild Metadaten</span><span class="sxs-lookup"><span data-stu-id="c6e6b-279">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="c6e6b-280">Übersicht über die metadatenerweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="c6e6b-280">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="c6e6b-281">Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="c6e6b-281">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



