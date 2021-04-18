---
title: Zuweisen von Ausgabeformaten
description: Zuweisen von Ausgabeformaten
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media-Format-SDK, Zuweisen von Ausgabeformaten
- Advanced Systems Format (ASF), Zuweisen von Ausgabeformaten
- ASF (Advanced Systems Format), Zuweisen von Ausgabeformaten
- Advanced Systems Format (ASF), Ausgabe Nummern und Formate
- ASF (Advanced Systems Format), Ausgabe Nummern und Formate
- ausgabezahlen und Formate, zuweisen
- Codecs, Ausgabe Nummern und Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106337833"
---
# <a name="assigning-output-formats"></a><span data-ttu-id="289c6-110">Zuweisen von Ausgabeformaten</span><span class="sxs-lookup"><span data-stu-id="289c6-110">Assigning Output Formats</span></span>

<span data-ttu-id="289c6-111">Einige Codecs können digitale Mediendaten in mehrere nicht komprimierte Formate decoeinigen.</span><span class="sxs-lookup"><span data-stu-id="289c6-111">Some codecs can decompress digital media data into several uncompressed formats.</span></span> <span data-ttu-id="289c6-112">Sie können alle unterstützten Formate für eine bestimmte Ausgabe mit dem asynchronen Reader oder dem synchronen Reader finden.</span><span class="sxs-lookup"><span data-stu-id="289c6-112">You can find all of the supported formats for a specific output using either the asynchronous reader or the synchronous reader.</span></span>

<span data-ttu-id="289c6-113">Um alle verfügbaren Formate für eine Ausgabe zu überprüfen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="289c6-113">To examine all of the available formats for an output, perform the following steps.</span></span> <span data-ttu-id="289c6-114">Diese Prozeduren sind sowohl für den asynchronen Reader als auch für den synchronen Reader identisch.</span><span class="sxs-lookup"><span data-stu-id="289c6-114">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="289c6-115">Wenn Schnittstellennamen unterschiedlich sind, werden die synchronen Reader-Methoden nach den Methoden des asynchronen Readers in Klammern aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="289c6-115">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="289c6-116">Erstellen Sie ein Reader-Objekt, und laden Sie eine Datei zum Lesen.</span><span class="sxs-lookup"><span data-stu-id="289c6-116">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="289c6-117">Weitere Informationen finden Sie unter so [Erstellen Sie einen Reader und öffnen eine Datei](to-create-a-reader-and-open-a-file.md) (oder [zum Erstellen eines synchronen Readers und Öffnen einer Datei](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="289c6-117">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="289c6-118">Bestimmen Sie die Ausgabe, für die Sie die verfügbaren Formate suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="289c6-118">Determine the output for which you want to find the available formats.</span></span> <span data-ttu-id="289c6-119">Wenn Sie nicht bereits wissen, welche Ausgabe Sie verwenden möchten, können Sie die Ausgaben in der Datei mithilfe der Prozeduren in identifizieren, [um Ausgabe Nummern zu identifizieren](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="289c6-119">If you don't already know which output you want to use, you can identify the outputs in the file using the procedures in [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="289c6-120">Rufen Sie die Gesamtanzahl der verfügbaren Formate für die gewünschte Ausgabe ab, indem Sie [**iwmreader:: getoutputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (oder [**iwmsyncreader:: getoutputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="289c6-120">Retrieve the total number of available formats for the desired output by calling [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (or [**IWMSyncReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span></span>
4.  <span data-ttu-id="289c6-121">Durchlaufen Sie die verfügbaren Formate nacheinander, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="289c6-121">Loop through the available formats one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="289c6-122">Rufen Sie die [**iwmoutputmediadie**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) -Schnittstelle für das aktuelle Ausgabeformat durch Aufrufen von [**iwmreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (oder [**iwmsyncreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)) ab.</span><span class="sxs-lookup"><span data-stu-id="289c6-122">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output format by calling [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (or [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span></span>
    -   <span data-ttu-id="289c6-123">Rufen Sie die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für das Ausgabeformat ab, indem Sie zwei Aufrufe an [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)durchführen.</span><span class="sxs-lookup"><span data-stu-id="289c6-123">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output format by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="289c6-124">Führen Sie den ersten-Befehl aus, um die Größe der Struktur abzurufen, und weisen Sie dann Arbeitsspeicher zu, und übergeben Sie einen Zeiger auf den zugeordneten Speicher im zweiten-Befehl.</span><span class="sxs-lookup"><span data-stu-id="289c6-124">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span>
    -   <span data-ttu-id="289c6-125">Suchen Sie den Medien Untertyp des Ausgabeformats in **WM \_ Media \_ Type. Untertyp**.</span><span class="sxs-lookup"><span data-stu-id="289c6-125">Find the media subtype of the output format in **WM\_MEDIA\_TYPE.subtype**.</span></span>
    -   <span data-ttu-id="289c6-126">Wenn es sich bei dem aktuellen Untertyp um das Format handelt, das Sie für die Ausgabe verwenden möchten, brechen Sie die Schleife aus.</span><span class="sxs-lookup"><span data-stu-id="289c6-126">For video, if the current subtype is the format you want to use for output, break out of the loop.</span></span> <span data-ttu-id="289c6-127">Andernfalls wechseln Sie zur nächsten Iterationen.</span><span class="sxs-lookup"><span data-stu-id="289c6-127">Otherwise go to the next iteration.</span></span>

        <span data-ttu-id="289c6-128">Für Audiodaten müssen Sie die Werte in der **WaveFormatEx** -Struktur hinsichtlich ihrer Anforderungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="289c6-128">For audio, you must check the values in the **WAVEFORMATEX** structure against your requirements.</span></span> <span data-ttu-id="289c6-129">**WM \_ \_Medientyp. pbformat** verweist auf die **WaveFormatEx** -Struktur für Audioausgaben.</span><span class="sxs-lookup"><span data-stu-id="289c6-129">**WM\_MEDIA\_TYPE.pbFormat** points to the **WAVEFORMATEX** structure for audio outputs.</span></span>

5.  <span data-ttu-id="289c6-130">Wenn Sie die gewünschte Ausgabe gefunden haben, legen Sie Sie für die Verwendung mit dem Reader fest, indem Sie [**iwmreader:: SetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) Eigenschaften (oder [**iwmsyncreader:: SetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)Eigenschaften) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="289c6-130">When you have found the output desired, set it for use with the reader by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (or [**IWMSyncReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span></span> <span data-ttu-id="289c6-131">Sie müssen einen Zeiger an die **iwmoutputmedia-** Schnittstelle übergeben, die im ersten Schritt der Schleife abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="289c6-131">You must pass a pointer to the **IWMOutputMediaProps** interface obtained in the first step of the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="289c6-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="289c6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="289c6-133">**Iwmmedia-Eigenschaften Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="289c6-133">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="289c6-134">**Iwmoutputmediadie-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="289c6-134">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="289c6-135">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="289c6-135">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="289c6-136">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="289c6-136">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="289c6-137">**Arbeiten mit Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="289c6-137">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




