---
title: Formate
description: Formate
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- SDK für Windows Media-Format, Eingaben
- Windows Media-Format-SDK, Streams
- Windows Media-Format-SDK, Ausgaben
- Windows Media-Format-SDK, Formate
- Advanced Systems Format (ASF), Eingaben
- ASF (Advanced Systems Format), Eingaben
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Advanced Systems Format (ASF), Ausgaben
- ASF (Advanced Systems Format), Ausgaben
- Advanced Systems Format (ASF), Formate
- ASF (Advanced Systems Format), Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310784"
---
# <a name="formats"></a><span data-ttu-id="67871-115">Formate</span><span class="sxs-lookup"><span data-stu-id="67871-115">Formats</span></span>

<span data-ttu-id="67871-116">Die Informationen in einem Format beschreiben alles, was Sie über einen bestimmten Medientyp wissen müssen.</span><span class="sxs-lookup"><span data-stu-id="67871-116">The information in a format describes everything you need to know about a particular type of media.</span></span> <span data-ttu-id="67871-117">Jedes Format weist einen Haupttyp auf, wie z. b. Audiodaten oder Video, und kann einen Untertyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="67871-117">Every format has a major type, like audio or video, and may have a subtype.</span></span> <span data-ttu-id="67871-118">Formate enthalten unterschiedliche Informationen auf Grundlage des Haupt Typs.</span><span class="sxs-lookup"><span data-stu-id="67871-118">Formats contain different information based on major type.</span></span> <span data-ttu-id="67871-119">Audioformate und Videoformate erfordern wesentlich mehr Informationen als andere Typen.</span><span class="sxs-lookup"><span data-stu-id="67871-119">Audio and video formats require much more information than other types.</span></span>

<span data-ttu-id="67871-120">Ebenso wie die Objekte des Windows Media SDK-SDK zwischen Eingabe Zahlen, streamnummern und Ausgabe Nummern (siehe [Eingaben, Streams und Ausgaben](inputs-streams-and-outputs.md)) unterscheiden, gibt es wichtige Unterschiede zwischen Eingabe Formaten, streamformaten und Ausgabeformaten.</span><span class="sxs-lookup"><span data-stu-id="67871-120">Just as the objects of the Windows Media Format SDK differentiate between input numbers, stream numbers, and output numbers (see [Inputs, Streams and Outputs](inputs-streams-and-outputs.md)), there are important distinctions between input formats, stream formats, and output formats.</span></span> <span data-ttu-id="67871-121">Diese Unterschiede werden hier beschrieben:</span><span class="sxs-lookup"><span data-stu-id="67871-121">These differences are described here:</span></span>

## <a name="input-formats"></a><span data-ttu-id="67871-122">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="67871-122">Input Formats</span></span>

<span data-ttu-id="67871-123">Ein Eingabeformat beschreibt die digitalen Medien, die Sie an das Writer-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="67871-123">An input format describes the digital media that you pass to the writer object.</span></span> <span data-ttu-id="67871-124">Wenn ein Datenstrom in einer ASF-Datei mit einem Codec komprimiert wird, unterstützt der Codec nur bestimmte Eingabeformate.</span><span class="sxs-lookup"><span data-stu-id="67871-124">If a stream in an ASF file is compressed with a codec, the codec will support only certain input formats.</span></span> <span data-ttu-id="67871-125">Wenn Sie die Windows Media Audio-und Video Codecs verwenden, können Sie die unterstützten Eingabeformate mithilfe des Writer-Objekts auflisten.</span><span class="sxs-lookup"><span data-stu-id="67871-125">When using the Windows Media Audio and Video codecs, you can enumerate the supported input formats using the writer object.</span></span> <span data-ttu-id="67871-126">Beim Schreiben einer Datei sind Sie dafür verantwortlich, ein Eingabeformat auszuwählen, das mit den Eingabemedien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="67871-126">When writing a file, you are responsible for selecting an input format that matches your input media.</span></span>

<span data-ttu-id="67871-127">Obwohl das Eingabemedien Format vom Codec unterstützt werden muss, mit dem die Daten komprimiert werden, müssen einige Eingabeformat Einstellungen nicht dem Streamformat entsprechen.</span><span class="sxs-lookup"><span data-stu-id="67871-127">Although the input media format must be supported by the codec that will compress the data, some input format settings need not match the stream format.</span></span> <span data-ttu-id="67871-128">Beispielsweise kann das Eingabeformat für einen Videostream eine Frame Größe aufweisen, die sich von der im Streamformat definierten Frame Größe unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="67871-128">For example, the input format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="67871-129">Der Codec führt Konvertierungen in diesen Fällen aus.</span><span class="sxs-lookup"><span data-stu-id="67871-129">The codec will perform conversions in these cases.</span></span>

## <a name="stream-formats"></a><span data-ttu-id="67871-130">Streamformate</span><span class="sxs-lookup"><span data-stu-id="67871-130">Stream Formats</span></span>

<span data-ttu-id="67871-131">Ein Streamformat beschreibt das Formular des Mediums, das in der ASF-Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="67871-131">A stream format describes the form of the media as it is stored in the ASF file.</span></span> <span data-ttu-id="67871-132">Das Datenstrom Format ist das im Profil beschriebene Format und kann mit dem Eingabeformat und dem Ausgabeformat identisch sein.</span><span class="sxs-lookup"><span data-stu-id="67871-132">The stream format is the format described in the profile, and may or may not be the same as the input format and output format.</span></span> <span data-ttu-id="67871-133">Wenn ein Codec zum Komprimieren der Daten in einem Stream verwendet wird, unterscheidet sich das Streamformat von den Eingabe-und Ausgabeformaten.</span><span class="sxs-lookup"><span data-stu-id="67871-133">If a codec is used to compress the data in a stream, the stream format will be different than the input and output formats.</span></span>

<span data-ttu-id="67871-134">Wenn Sie die Windows Media Audio-und Video Codecs verwenden, müssen Sie eine Liste der unterstützten Streamformate vom Codec abrufen, um sicherzustellen, dass Sie nicht versuchen, ein Format anzugeben, das der Code nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67871-134">When using the Windows Media Audio and Video codecs, you must obtain a list of supported stream formats from the codec to ensure that you are not attempting to specify a format that the code does not support.</span></span> <span data-ttu-id="67871-135">Einige Format Einstellungen (z. b. die Größe und die Farbtiefe eines Video Frames) müssen manuell konfiguriert werden, nachdem das Codec-Format abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="67871-135">Some format settings, such as the size and color depth of a video frame, must be configured manually after the codec format is retrieved.</span></span>

## <a name="output-formats"></a><span data-ttu-id="67871-136">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="67871-136">Output Formats</span></span>

<span data-ttu-id="67871-137">In einem Ausgabeformat werden die digitalen Medien beschrieben, die der Reader (oder der synchrone Reader) an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="67871-137">An output format describes the digital media that the reader (or synchronous reader) delivers to your application.</span></span> <span data-ttu-id="67871-138">Wenn ein Datenstrom in einer ASF-Datei mit einem Codec komprimiert wird, unterstützt der Codec nur bestimmte Ausgabeformate.</span><span class="sxs-lookup"><span data-stu-id="67871-138">If a stream in an ASF file is compressed with a codec, the codec will support only certain output formats.</span></span> <span data-ttu-id="67871-139">Wenn Sie die Windows Media Audio-und Video Codecs verwenden, können Sie die unterstützten Ausgabeformate mithilfe des Reader-Objekts auflisten.</span><span class="sxs-lookup"><span data-stu-id="67871-139">When using the Windows Media Audio and Video codecs, you can enumerate the supported output formats by using the reader object.</span></span> <span data-ttu-id="67871-140">Jedes der Windows Media-Codecs verfügt über ein Standardausgabeformat, aber Sie können ein beliebiges unterstütztes Ausgabeformat für die Beispiel Übermittlung auswählen.</span><span class="sxs-lookup"><span data-stu-id="67871-140">Each of the Windows Media codecs has a default output format, but you can select any supported output format for sample delivery.</span></span>

<span data-ttu-id="67871-141">Obwohl das Ausgabemedien Format vom Codec unterstützt werden muss, der die Daten komprimiert, müssen einige Ausgabe Formateinstellungen nicht dem Streamformat entsprechen.</span><span class="sxs-lookup"><span data-stu-id="67871-141">Although the output media format must be supported by the codec that compressed the data, some output format settings need not match the stream format.</span></span> <span data-ttu-id="67871-142">Das Ausgabeformat für einen Videostream kann z. b. eine Frame Größe aufweisen, die sich von der im Streamformat definierten Frame Größe unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="67871-142">For example, the output format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="67871-143">Der Codec führt Konvertierungen in diesen Fällen aus.</span><span class="sxs-lookup"><span data-stu-id="67871-143">The codec will perform conversions in these cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67871-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67871-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67871-145">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="67871-145">**Concepts**</span></span>](concepts.md)
</dt> </dl>

 

 




