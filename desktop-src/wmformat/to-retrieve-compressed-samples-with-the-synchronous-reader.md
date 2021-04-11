---
title: So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab
description: So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Advanced Systems Format (ASF), Abrufen von komprimierten Beispielen
- ASF (Advanced Systems Format), Abrufen von komprimierten Beispielen
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), komprimierte Beispiele
- ASF (Advanced Systems Format), komprimierte Beispiele
- synchrone Leser, Abrufen komprimierter Beispiele
- synchrone Reader, komprimierte Beispiele
- komprimierte Beispiele, Abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101258"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a><span data-ttu-id="706ab-112">So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab</span><span class="sxs-lookup"><span data-stu-id="706ab-112">To Retrieve Compressed Samples with the Synchronous Reader</span></span>

<span data-ttu-id="706ab-113">Ebenso wie der asynchrone Reader kann der synchrone Reader auch komprimierte Beispiele abrufen.</span><span class="sxs-lookup"><span data-stu-id="706ab-113">Like the asynchronous reader, the synchronous reader can also retrieve compressed samples.</span></span> <span data-ttu-id="706ab-114">Komprimierte Beispiele sollten beim Kopieren von Streams aus einer Datei in eine andere verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="706ab-114">Compressed samples should be used when copying streams from one file to another.</span></span>

<span data-ttu-id="706ab-115">Das Windows Media-Format-SDK stellt keine Methoden zum Decodieren von Daten bereit, nachdem es aus einer ASF-Datei extrahiert wurde.</span><span class="sxs-lookup"><span data-stu-id="706ab-115">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="706ab-116">Wenn Sie komprimierte Beispiele erhalten und diese später dekomprimieren möchten, müssen Sie dazu ihren eigenen Code bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="706ab-116">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="706ab-117">Eine Möglichkeit, diese Einschränkung zu umgehen, besteht darin, die komprimierten Beispiele in eine neue ASF-Datei zu schreiben und Sie dann in normale, nicht komprimierte Beispiele zu lesen.</span><span class="sxs-lookup"><span data-stu-id="706ab-117">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="706ab-118">Um komprimierte Beispiele mit dem synchronen Reader zu erhalten, nennen Sie [**iwmsynkreader:: abtreadstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) vor oder während der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="706ab-118">To receive compressed samples with the synchronous reader, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) before or during playback.</span></span> <span data-ttu-id="706ab-119">Übergeben Sie "true" für die *Komprimierung*.</span><span class="sxs-lookup"><span data-stu-id="706ab-119">Pass true for *fCompressed*.</span></span>

> [!Note]  
> <span data-ttu-id="706ab-120">Bildstreams sind für die komprimierte Datenstrom Übermittlung ungültig.</span><span class="sxs-lookup"><span data-stu-id="706ab-120">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="706ab-121">Wenn Sie einen Bildstream aus einer Datei in einen anderen kopieren, funktioniert er nicht in der neuen Datei.</span><span class="sxs-lookup"><span data-stu-id="706ab-121">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="706ab-122">Um einen Bildstream aus einer Datei in eine Datei zu kopieren, rufen Sie die Abbild Datenstrom Beispiele nach Ausgabe Nummer ab, und fügen Sie Sie in die neue Datei ein, als ob Sie einen neuen Bildstream einschließen</span><span class="sxs-lookup"><span data-stu-id="706ab-122">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="706ab-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="706ab-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="706ab-124">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="706ab-124">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




