---
title: So liefern Sie komprimierte Beispiele mit dem asynchronen Reader
description: So liefern Sie komprimierte Beispiele mit dem asynchronen Reader
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Advanced Systems Format (ASF), Bereitstellung von komprimierten Beispielen
- ASF (Advanced Systems Format), Bereitstellung von komprimierten Beispielen
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), komprimierte Beispiele
- ASF (Advanced Systems Format), komprimierte Beispiele
- asynchrone Leser, Bereitstellung von komprimierten Beispielen
- asynchrone Leser, komprimierte Beispiele
- komprimierte Beispiele, Bereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723536"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a><span data-ttu-id="66629-112">So liefern Sie komprimierte Beispiele mit dem asynchronen Reader</span><span class="sxs-lookup"><span data-stu-id="66629-112">To Deliver Compressed Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="66629-113">Der asynchrone Reader kann komprimierte Beispiele aus Streams in ASF-Dateien bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="66629-113">The asynchronous reader can deliver compressed samples from streams in ASF files.</span></span> <span data-ttu-id="66629-114">Anwendungen stellen in der Regel komprimierte Beispiele bereit, wenn Sie einen Stream aus einer Datei in eine andere kopieren.</span><span class="sxs-lookup"><span data-stu-id="66629-114">Applications usually deliver compressed samples when copying a stream from one file to another.</span></span> <span data-ttu-id="66629-115">Es ist nicht empfehlenswert, Daten, die aus einem komprimierten Stream rekonstruiert wurden, erneut zu komprimieren, da die Daten beim Codierungs Vorgang verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="66629-115">It is not advisable to recompress data that has been reconstructed from a compressed stream, because data is lost in the encoding process.</span></span> <span data-ttu-id="66629-116">Digitale Medien, die mehr als einmal komprimiert werden, haben eine spürbare Abnahme der Qualität.</span><span class="sxs-lookup"><span data-stu-id="66629-116">Digital media that has been compressed more than once will have a noticeable decrease in quality.</span></span>

<span data-ttu-id="66629-117">Das Windows Media-Format-SDK stellt keine Methoden zum Decodieren von Daten bereit, nachdem es aus einer ASF-Datei extrahiert wurde.</span><span class="sxs-lookup"><span data-stu-id="66629-117">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="66629-118">Wenn Sie komprimierte Beispiele erhalten und diese später dekomprimieren möchten, müssen Sie dazu ihren eigenen Code bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="66629-118">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="66629-119">Eine Möglichkeit, diese Einschränkung zu umgehen, besteht darin, die komprimierten Beispiele in eine neue ASF-Datei zu schreiben und Sie dann in normale, nicht komprimierte Beispiele zu lesen.</span><span class="sxs-lookup"><span data-stu-id="66629-119">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="66629-120">Um komprimierte Beispiele mit dem asynchronen Reader zu erhalten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="66629-120">To receive compressed samples with the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="66629-121">Implementieren Sie den " [**iwmreadercallbackadvanced:: onstreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) "-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="66629-121">Implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback.</span></span> <span data-ttu-id="66629-122">Dieser Rückruf ist im Grunde identisch mit [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , mit dem Unterschied, dass er Beispiele nach streamnummer liefert und die Beispiele weiterhin komprimiert sind.</span><span class="sxs-lookup"><span data-stu-id="66629-122">This callback is basically identical in function to [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it delivers samples by stream number and the samples are still compressed.</span></span>
2.  <span data-ttu-id="66629-123">Rufen Sie vor dem Starten der Wiedergabe einen Zeiger auf die [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) -Schnittstelle des Reader-Objekts ab, indem Sie **iwmreader:: QueryInterface** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="66629-123">Before starting playback, obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="66629-124">Konfigurieren Sie den Reader so, dass komprimierte Beispiele für den gewünschten Stream durch Aufrufen von [**iwmreaderadvanced:: setreceivestreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="66629-124">Configure the reader to deliver compressed samples for the desired stream by calling [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span></span>
4.  <span data-ttu-id="66629-125">Wiederholen Sie Schritt 3 für jeden Stream, für den eine komprimierte Beispiel Übermittlung gewünscht ist.</span><span class="sxs-lookup"><span data-stu-id="66629-125">Repeat step 3 for each stream for which compressed sample delivery is desired.</span></span>

> [!Note]  
> <span data-ttu-id="66629-126">Bildstreams sind für die komprimierte Datenstrom Übermittlung ungültig.</span><span class="sxs-lookup"><span data-stu-id="66629-126">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="66629-127">Wenn Sie einen Bildstream aus einer Datei in einen anderen kopieren, funktioniert er nicht in der neuen Datei.</span><span class="sxs-lookup"><span data-stu-id="66629-127">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="66629-128">Um einen Bildstream aus einer Datei in eine Datei zu kopieren, rufen Sie die Abbild Datenstrom Beispiele nach Ausgabe Nummer ab, und fügen Sie Sie in die neue Datei ein, als ob Sie einen neuen Bildstream einschließen</span><span class="sxs-lookup"><span data-stu-id="66629-128">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="66629-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66629-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66629-130">**Iwmreadercallbackadvanced-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="66629-130">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="66629-131">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="66629-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




