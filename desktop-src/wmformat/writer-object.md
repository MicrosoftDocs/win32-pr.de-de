---
title: Writer-Objekt
description: Writer-Objekt
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows Media-Format-SDK, Writer-Objekte
- Advanced Systems Format (ASF), Writer-Objekte
- ASF (Advanced Systems Format), Writer-Objekte
- Objekte, Writer-Objekte
- Writer-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724123"
---
# <a name="writer-object"></a><span data-ttu-id="2033f-108">Writer-Objekt</span><span class="sxs-lookup"><span data-stu-id="2033f-108">Writer Object</span></span>

<span data-ttu-id="2033f-109">Das Writer-Objekt wird verwendet, um digitale Mediendateien mit der Dateistruktur Advanced Systems Format (ASF) zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="2033f-109">The writer object is used to write digital media files using the advanced systems format (ASF) file structure.</span></span> <span data-ttu-id="2033f-110">Beim Schreiben einer digitalen Mediendatei werden viele interne Schritte für den Writer ausgeführt, mit denen die Komprimierung, die packetisierung und Multiplexing koordiniert werden.</span><span class="sxs-lookup"><span data-stu-id="2033f-110">The process of writing a digital media file involves many steps internal to the writer, which coordinates compression, packetization, and multiplexing.</span></span>

<span data-ttu-id="2033f-111">Das Writer-Objekt enthält Schnittstellen für die Ausgabe in Dateien oder ein Netzwerk, unterstützt eine Rückruf Schnittstelle und kann ein oder mehrere Eingabemedien-Eigenschaften Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="2033f-111">The writer object includes interfaces for output to files or a network, supports one callback interface, and can create one or more input media properties objects.</span></span>

<span data-ttu-id="2033f-112">Das Writer-Objekt wird von der [**wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)-Funktion erstellt, mit der ein Zeiger auf eine **iwmwriter** -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="2033f-112">The writer object is created by the function [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), which sets a pointer to an **IWMWriter** interface.</span></span> <span data-ttu-id="2033f-113">Die anderen Schnittstellen des Writer-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2033f-113">The other interfaces of the writer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="2033f-114">Die folgenden Schnittstellen werden vom Writer-Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2033f-114">The following interfaces are supported by the writer object.</span></span>



| <span data-ttu-id="2033f-115">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2033f-115">Interface</span></span>                                          | <span data-ttu-id="2033f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2033f-116">Description</span></span>                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2033f-117">**Iwmdrmwriter**</span><span class="sxs-lookup"><span data-stu-id="2033f-117">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | <span data-ttu-id="2033f-118">Stellt Methoden zum Generieren von [*DRM*](wmformat-glossary.md) -Schlüsseln bereit.</span><span class="sxs-lookup"><span data-stu-id="2033f-118">Provides methods to generate [*DRM*](wmformat-glossary.md) keys.</span></span>                                                                                                |
| [<span data-ttu-id="2033f-119">**IWMDRMWriter2**</span><span class="sxs-lookup"><span data-stu-id="2033f-119">**IWMDRMWriter2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | <span data-ttu-id="2033f-120">Konfiguriert das Writer-Objekt zum Schreiben einer Datei, die einen vorverschlüsselten Stream enthält, der dem Windows Media DRM 10 for Network Devices-Protokoll entspricht.</span><span class="sxs-lookup"><span data-stu-id="2033f-120">Configures the writer object to write a file containing a pre-encrypted stream that conforms to the Windows Media DRM 10 for Network Devices protocol.</span></span>                                                    |
| [<span data-ttu-id="2033f-121">**Iwmheaderinfo**</span><span class="sxs-lookup"><span data-stu-id="2033f-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | <span data-ttu-id="2033f-122">Verwaltet die Spezifikation und den Abruf von Header Informationen, z. b. Metadaten, [*Marker*](wmformat-glossary.md)usw.</span><span class="sxs-lookup"><span data-stu-id="2033f-122">Manages the specification and retrieval of header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                                           |
| [<span data-ttu-id="2033f-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="2033f-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | <span data-ttu-id="2033f-124">Verwaltet das Auflisten der verfügbaren Codec-Informationen.</span><span class="sxs-lookup"><span data-stu-id="2033f-124">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="2033f-125">Erbt alle Methoden von **iwmheaderinfo**.</span><span class="sxs-lookup"><span data-stu-id="2033f-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                            |
| [<span data-ttu-id="2033f-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="2033f-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | <span data-ttu-id="2033f-127">Verwaltet das Auflisten der verfügbaren Codec-Informationen.</span><span class="sxs-lookup"><span data-stu-id="2033f-127">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="2033f-128">Erbt alle Methoden von **iwmheaderinfo** und **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="2033f-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>                                                                     |
| [<span data-ttu-id="2033f-129">**Iwmwatermarkinfo**</span><span class="sxs-lookup"><span data-stu-id="2033f-129">**IWMWatermarkInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | <span data-ttu-id="2033f-130">Bietet Zugriff auf Informationen über Wasserzeichen Systeme, die auf dem System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2033f-130">Provides access to information about watermarking systems present on the system.</span></span>                                                                                                                          |
| [<span data-ttu-id="2033f-131">**Iwmwriter**</span><span class="sxs-lookup"><span data-stu-id="2033f-131">**IWMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | <span data-ttu-id="2033f-132">Startet und beendet das Schreiben von ASF-Dateien. Es enthält Methoden zum Zuordnen von Puffern, festlegen und Abrufen von Eingabe Eigenschaften, Festlegen von Profilen und Ausgabe Dateinamen und Entsperren des Writers.</span><span class="sxs-lookup"><span data-stu-id="2033f-132">Starts and stops the writing of ASF files; it includes methods for allocating buffers, setting and retrieving input properties, setting profiles and output file names, and unlocking the writer.</span></span>         |
| [<span data-ttu-id="2033f-133">**Iwmschreibadvanced**</span><span class="sxs-lookup"><span data-stu-id="2033f-133">**IWMWriterAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | <span data-ttu-id="2033f-134">Fügt angegebene Sink-Objekte hinzu, ruft Sie ab und entfernt Sie. Ruft Statistiken, die Anzahl der senken und die Uhrzeit ab, zu der der Writer arbeitet. und führt andere erweiterte Funktionen aus.</span><span class="sxs-lookup"><span data-stu-id="2033f-134">Adds, gets, and removes specified sink objects; retrieves statistics, number of sinks, and the clock time the writer is working to; and performs other advanced functions.</span></span>                                |
| [<span data-ttu-id="2033f-135">**IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="2033f-135">**IWMWriterAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | <span data-ttu-id="2033f-136">Bietet einige erweiterte Funktionen, insbesondere für die Handhabung von Deinterlacing-Videos.</span><span class="sxs-lookup"><span data-stu-id="2033f-136">Provides some advanced functionality, particularly for handling deinterlaced video.</span></span> <span data-ttu-id="2033f-137">Erbt alle Methoden von **iwmschreiteradvanced**.</span><span class="sxs-lookup"><span data-stu-id="2033f-137">Inherits all of the methods of **IWMWriterAdvanced**.</span></span>                                                                 |
| [<span data-ttu-id="2033f-138">**IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="2033f-138">**IWMWriterAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | <span data-ttu-id="2033f-139">Bietet zusätzliche Writer-Funktionen, einschließlich der Möglichkeit, ausführliche Writer-Statistiken zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2033f-139">Provides additional writer functionality, including the ability to get detailed writer statistics.</span></span> <span data-ttu-id="2033f-140">Erbt alle Methoden von **iwmschreiteradvanced** und **IWMWriterAdvanced2**.</span><span class="sxs-lookup"><span data-stu-id="2033f-140">Inherits all of the methods of **IWMWriterAdvanced** and **IWMWriterAdvanced2**.</span></span>                       |
| [<span data-ttu-id="2033f-141">**Iwmbeschreiterpostview**</span><span class="sxs-lookup"><span data-stu-id="2033f-141">**IWMWriterPostView**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | <span data-ttu-id="2033f-142">Verwaltet einige erweiterte Schreibfunktionen im Zusammenhang mit Postview-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="2033f-142">Manages some advanced writing functionality related to postviewing samples.</span></span> <span data-ttu-id="2033f-143">Bei der nach Anzeige wird die Ausgabe, normalerweise von einem Encoder, angezeigt, um zu überprüfen, ob der Codierungs-/Decodierungs Prozess ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="2033f-143">Postviewing is viewing the output, usually from an encoder, to check that the encoding/decoding process is working correctly.</span></span> |
| [<span data-ttu-id="2033f-144">**IWMWriterPreprocess**</span><span class="sxs-lookup"><span data-stu-id="2033f-144">**IWMWriterPreprocess**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | <span data-ttu-id="2033f-145">Verwaltet Vorverarbeitungs Durchläufen, die vom Writer erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2033f-145">Manages preprocessing passes made by the writer.</span></span> <span data-ttu-id="2033f-146">Vorverarbeitungs Durchläufen werden verwendet, um die Qualität der codierten Ausgabe zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="2033f-146">Preprocessing passes are used to improve the quality of encoded output.</span></span>                                                                                  |



 

<span data-ttu-id="2033f-147">Die folgende Rückruf Schnittstelle muss von der Anwendung implementiert werden, um den Fortschritt der Post Ansicht zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="2033f-147">The following callback interface must be implemented by the application to track the progress of postviewing.</span></span>



| <span data-ttu-id="2033f-148">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2033f-148">Interface</span></span>                                                      | <span data-ttu-id="2033f-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2033f-149">Description</span></span>                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2033f-150">**Iwmschreiterpostviewcallback**</span><span class="sxs-lookup"><span data-stu-id="2033f-150">**IWMWriterPostViewCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | <span data-ttu-id="2033f-151">Verwaltet, wie unkomprimierte Beispiele vom Writer-Objekt empfangen werden, um die Vorschau der Vorgänge des Codecs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2033f-151">Manages how uncompressed samples are received from the writer object to preview what the codec is doing.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2033f-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2033f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2033f-153">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="2033f-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="2033f-154">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="2033f-154">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




