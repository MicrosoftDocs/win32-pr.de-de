---
description: Die Windows Media Audio-und Video Codecs sind eine Auflistung von Objekten, die Sie verwenden können, um digitale Mediendaten zu komprimieren und zu komprimieren.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Windows Media-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353636"
---
# <a name="windows-media-codecs"></a><span data-ttu-id="8cae8-103">Windows Media-Codecs</span><span class="sxs-lookup"><span data-stu-id="8cae8-103">Windows Media Codecs</span></span>

<span data-ttu-id="8cae8-104">Die Windows Media Audio-und Video Codecs sind eine Auflistung von Objekten, die Sie verwenden können, um digitale Mediendaten zu komprimieren und zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="8cae8-104">The Windows Media Audio and Video codecs are a collection of objects that you can use to compress and decompress digital media data.</span></span> <span data-ttu-id="8cae8-105">Jeder Codec besteht aus zwei Objekten, einem Encoder und einem Decoder.</span><span class="sxs-lookup"><span data-stu-id="8cae8-105">Each codec consists of two objects, an encoder and a decoder.</span></span> <span data-ttu-id="8cae8-106">In diesem Teil der Dokumentation wird beschrieben, wie die Funktionen des Windows Media Audio und der Video Codecs verwendet werden, um komprimierte Datenströme zu erzeugen und zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="8cae8-106">This part of the documentation describes how to use the features of the Windows Media Audio and Video codecs to produce and consume compressed data streams.</span></span>

> [!Note]  
> <span data-ttu-id="8cae8-107">Diese Dokumentation richtet sich hauptsächlich an Entwickler, die Windows Media-Codecs in Ihren C++-basierten Medienanwendungen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8cae8-107">This documentation is primarily for developers who want to use Windows Media codecs in their C++-based media applications.</span></span> <span data-ttu-id="8cae8-108">Eine technische Übersicht über die Features der Windows Media-Codecs finden Sie unter [Informationen zu Windows Media Codecs](about-the-windows-media-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="8cae8-108">For a technical overview of the features of the Windows Media codecs, see [About the Windows Media Codecs](about-the-windows-media-codecs.md).</span></span>

 

<span data-ttu-id="8cae8-109">Der Begriff " *Codec* " ist eine Zusammenstellung der Begriffe "Kompressor" und "Debug".</span><span class="sxs-lookup"><span data-stu-id="8cae8-109">The term *codec* is an amalgamation of the terms compressor and decompressor.</span></span> <span data-ttu-id="8cae8-110">Ein Codec wird normalerweise als Paar von COM-Objekten implementiert: einer für Codierungs Inhalte und ein anderer zum Decodieren von Inhalt.</span><span class="sxs-lookup"><span data-stu-id="8cae8-110">A codec is usually implemented as a pair of COM objects: one for encoding content, and another for decoding content.</span></span> <span data-ttu-id="8cae8-111">In einigen Fällen belegen die COM-Objekte dieselbe dynamisch verknüpfte Bibliothek (dll).</span><span class="sxs-lookup"><span data-stu-id="8cae8-111">In some cases the COM objects occupy the same dynamically linked library (DLL).</span></span>

<span data-ttu-id="8cae8-112">Jedes Codec-Objekt implementiert zwei separate, aber ähnliche Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="8cae8-112">Every codec object implements two separate but similar interfaces:</span></span>



| <span data-ttu-id="8cae8-113">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8cae8-113">Interface</span></span>                              | <span data-ttu-id="8cae8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cae8-114">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="8cae8-115">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="8cae8-115">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="8cae8-116">Kompatibel mit Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8cae8-116">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="8cae8-117">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="8cae8-117">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="8cae8-118">Kompatibel mit DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8cae8-118">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="8cae8-119">Es gibt nicht nur verschiedene Codecs für Audiodaten und Videos, sondern auch verschiedene Codecs für verschiedene Arten von Inhalten, die Sie möglicherweise in eine Audiodatei oder Videodatei einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="8cae8-119">Not only are there different codecs for audio and for video, but also different codecs for different kinds of content that you might want to put into an audio or video file.</span></span> <span data-ttu-id="8cae8-120">Die Algorithmen, die zum Komprimieren und decoden von Daten für gesprochene Wörter verwendet werden, unterscheiden sich von den Algorithmen zum Komprimieren und decoden von Musikdaten.</span><span class="sxs-lookup"><span data-stu-id="8cae8-120">The algorithms used to compress and decompress data for spoken words differ from the algorithms used to compress and decompress music data.</span></span>

## <a name="codec-descriptions"></a><span data-ttu-id="8cae8-121">Codec-Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="8cae8-121">Codec Descriptions</span></span>

<span data-ttu-id="8cae8-122">In der folgenden Tabelle werden die vorgesehenen Verwendungen der Windows Media Codecs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8cae8-122">The following table describes the intended uses of the Windows Media codecs.</span></span>



| <span data-ttu-id="8cae8-123">Codec</span><span class="sxs-lookup"><span data-stu-id="8cae8-123">Codec</span></span>                                                                     | <span data-ttu-id="8cae8-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cae8-124">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cae8-125">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="8cae8-125">Windows Media Audio</span></span>](windowsmediaaudioencoder.md)                       | <span data-ttu-id="8cae8-126">Ein Audiocodec, der drei Kategorien von codiertem Inhalt unterstützt: Standard, Professional und Lossless.</span><span class="sxs-lookup"><span data-stu-id="8cae8-126">An audio codec that supports three categories of encoded content: Standard, Professional, and Lossless.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="8cae8-127">Windows Media Audio Stimme</span><span class="sxs-lookup"><span data-stu-id="8cae8-127">Windows Media Audio Voice</span></span>](windowsmediaaudiovoiceencoder.md)            | <span data-ttu-id="8cae8-128">Audiocodec, der für die Codierung der menschlichen Stimme bei hohen Komprimierungs Verhältnissen optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="8cae8-128">Audio codec optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="8cae8-129">Dies ist der bevorzugte Codec für Streams, die größtenteils aus gesprochenen Wörtern bestehen.</span><span class="sxs-lookup"><span data-stu-id="8cae8-129">This is the preferred codec for streams consisting mostly of spoken words.</span></span> <span data-ttu-id="8cae8-130">Für Inhalte, die gemischt Musik und Sprache sind, kann dieser Codec den verwendeten Codierungs Algorithmus dynamisch ändern, um eine optimale Qualität zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="8cae8-130">For content that is mixed music and speech, this codec can dynamically change the encoding algorithm used, to get optimal quality.</span></span> |
| [<span data-ttu-id="8cae8-131">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="8cae8-131">Windows Media Video 9</span></span>](windowsmediavideo9encoder.md)                    | <span data-ttu-id="8cae8-132">Ein Videocodec, der vier Kategorien von codiertem Inhalt unterstützt: einfaches Profil, Hauptprofil, erweitertes Profil und Image.</span><span class="sxs-lookup"><span data-stu-id="8cae8-132">A video codec that supports four categories of encoded content: Simple Profile, Main Profile, Advanced Profile, and Image..</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="8cae8-133">Windows Media Video 9-Bildschirm</span><span class="sxs-lookup"><span data-stu-id="8cae8-133">Windows Media Video 9 Screen</span></span>](usingthewindowsmediavideo9screencodec.md) | <span data-ttu-id="8cae8-134">Videocodec, der für die Codierung sequenzieller Screenshots von Computermonitoren optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="8cae8-134">Video codec optimized for encoding sequential screen shots from computer monitors.</span></span> <span data-ttu-id="8cae8-135">Dieser Codec wird häufig für Software Schulungen oder-Unterstützung verwendet, indem Überwachungs Images aufgezeichnet werden, während Computeranwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cae8-135">This codec is often used for software training or support by recording monitor images while computer applications are being used.</span></span>                                                                         |



 

<span data-ttu-id="8cae8-136">Die neuesten Versionen der Codec-Objekte ermöglichen auch den Zugriff auf einige Legacy-Codecs, einschließlich Windows Media Video 7 und 8, Windows Media Screen 7, ältere Microsoft MPEG-4-Codecs und Microsoft ISO MPEG-4-Codecs.</span><span class="sxs-lookup"><span data-stu-id="8cae8-136">The most recent versions of the codec objects also enable access to some legacy codecs, including Windows Media Video 7 and 8, Windows Media Screen 7, the older Microsoft MPEG-4 codecs, and the Microsoft ISO MPEG-4 codecs.</span></span>

> [!Note]  
> <span data-ttu-id="8cae8-137">In dieser Dokumentation werden diese veralteten Codecs nicht behandelt. Es werden nur die aktuellen Versionen von Codecs behandelt.</span><span class="sxs-lookup"><span data-stu-id="8cae8-137">This documentation does not cover these legacy codecs; it covers only the current versions of codecs.</span></span>

 

<span data-ttu-id="8cae8-138">Verwenden Sie für ältere Codecs dieselben Prozeduren wie bei der Verwendung der aktuellen Codecs. Beachten Sie jedoch, dass nicht alle Funktionen in allen Codecs unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8cae8-138">For older codecs, use the same procedures as when using the current codecs; however, remember that not all features are supported in all codecs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8cae8-139">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8cae8-139">In this section</span></span>

-   [<span data-ttu-id="8cae8-140">Informationen zu Windows Media-Codecs</span><span class="sxs-lookup"><span data-stu-id="8cae8-140">About the Windows Media Codecs</span></span>](about-the-windows-media-codecs.md)
-   [<span data-ttu-id="8cae8-141">Verwenden der Codec-und DSP-Objekte</span><span class="sxs-lookup"><span data-stu-id="8cae8-141">Using the Codec and DSP Objects</span></span>](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [<span data-ttu-id="8cae8-142">Codierungs Methoden</span><span class="sxs-lookup"><span data-stu-id="8cae8-142">Encoding Methods</span></span>](encodingmethods.md)
-   [<span data-ttu-id="8cae8-143">Codec-Implementierung</span><span class="sxs-lookup"><span data-stu-id="8cae8-143">Codec Implementation</span></span>](codecimplementation.md)
-   [<span data-ttu-id="8cae8-144">Das Leaky Bucket-Puffer Modell</span><span class="sxs-lookup"><span data-stu-id="8cae8-144">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
-   [<span data-ttu-id="8cae8-145">Arbeiten mit Codec-DMOS</span><span class="sxs-lookup"><span data-stu-id="8cae8-145">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
-   [<span data-ttu-id="8cae8-146">Arbeiten mit Codec-MFTs</span><span class="sxs-lookup"><span data-stu-id="8cae8-146">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
-   [<span data-ttu-id="8cae8-147">Arbeiten mit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="8cae8-147">Working with Audio</span></span>](workingwithaudio.md)
-   [<span data-ttu-id="8cae8-148">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="8cae8-148">Working with Video</span></span>](workingwithvideo.md)
-   [<span data-ttu-id="8cae8-149">Speichern von komprimierten Medien in AVI-Dateien</span><span class="sxs-lookup"><span data-stu-id="8cae8-149">Storing Compressed Media in AVI Files</span></span>](storingcompressedmediainavifiles.md)
-   [<span data-ttu-id="8cae8-150">Verwenden der VBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="8cae8-150">Using VBR Encoding</span></span>](usingvbrencoding.md)
-   [<span data-ttu-id="8cae8-151">Verwenden von Two-Pass Codierung</span><span class="sxs-lookup"><span data-stu-id="8cae8-151">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
-   [<span data-ttu-id="8cae8-152">Codierungs Statistiken werden erhalten</span><span class="sxs-lookup"><span data-stu-id="8cae8-152">Getting Encoding Statistics</span></span>](gettingencodingstatistics.md)
-   [<span data-ttu-id="8cae8-153">Verwenden von Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="8cae8-153">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
-   [<span data-ttu-id="8cae8-154">Codec-und DSP-IPropertyBag-Konstanten</span><span class="sxs-lookup"><span data-stu-id="8cae8-154">Codec and DSP IPropertyBag Constants</span></span>](codecanddspproperties.md)
-   [<span data-ttu-id="8cae8-155">Inhaltsverzeichnis (Inhaltsverzeichnis)</span><span class="sxs-lookup"><span data-stu-id="8cae8-155">Table of Contents Parser</span></span>](toc-parser.md)
-   [<span data-ttu-id="8cae8-156">FAQ zu Windows Media Codec</span><span class="sxs-lookup"><span data-stu-id="8cae8-156">Windows Media Codec FAQ</span></span>](frequentlyaskedquestions.md)

## <a name="related-topics"></a><span data-ttu-id="8cae8-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8cae8-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cae8-158">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="8cae8-158">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

<span data-ttu-id="8cae8-159">[Medientechnologien für Windows](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8cae8-159">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>
</dt> </dl>

 

 
