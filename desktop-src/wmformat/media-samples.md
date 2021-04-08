---
title: Medien Beispiele (Windows Media-Format 11 SDK)
description: Medien Beispiele
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media-Format-SDK, Medien Beispiele
- Windows Media-Format-SDK, Beispiele
- Advanced Systems Format (ASF), Medien Beispiele
- ASF (Advanced Systems Format), Medien Beispiele
- Advanced Systems Format (ASF), Beispiele
- ASF (Advanced Systems Format), Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103949360"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="4bb5f-109">Medien Beispiele (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="4bb5f-109">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="4bb5f-110">Ein Medien Beispiel (oder ein Beispiel) ist ein Block digitaler Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-110">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="4bb5f-111">Ein Beispiel ist die grundlegende Einheit, die durch das Lesen und Schreiben von Objekten des Windows Media Format SDK manipuliert wird.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-111">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="4bb5f-112">Der Inhalt einer einzelnen Stichprobe wird durch den Medientyp vorgegeben, der mit dem Beispiel verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-112">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="4bb5f-113">Jedes Beispiel stellt einen einzelnen Frame dar.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-113">For video, each sample represents a single frame.</span></span> <span data-ttu-id="4bb5f-114">Für Audiodaten wird die Menge der Daten in einer einzelnen Stichprobe im Profil festgelegt, das zum Erstellen der ASF-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-114">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="4bb5f-115">Beispiele können nicht komprimierte Daten enthalten, oder Sie können komprimierte Daten enthalten. in diesem Fall werden Sie als *streambeispiele* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-115">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="4bb5f-116">Wenn Sie eine ASF-Datei erstellen, übergeben Sie Beispiele an den Writer.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-116">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="4bb5f-117">Der Writer koordiniert die Komprimierung der Beispiele mit dem entsprechenden Codec und ordnet die komprimierten Daten im Data-Abschnitt der ASF-Datei an.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-117">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="4bb5f-118">Bei der Wiedergabe liest der Reader die komprimierten Daten, dekomprimiert ihn und stellt die rekonstruierten unkomprimierten Daten als Ausgabe Beispiele zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-118">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="4bb5f-119">Alle vom Windows Media-Format-SDK verwendeten Beispiele sind in einem Puffer Objekt gekapselt, dessen Speicher automatisch von den SDK-Laufzeitkomponenten zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-119">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="4bb5f-120">Sie können bei Bedarf auch Ihre eigenen Puffer zuordnen, indem Sie erweiterte Funktionen von Writer und Reader verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-120">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="4bb5f-121">**Hinweis** Der Begriff Sample wird in diesem SDK verwendet, um auf ein Medien Beispiel zu verweisen, nicht auf ein Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-121">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="4bb5f-122">Bei der Audiocodierung bezieht sich ein Beispiel auf einen einzelnen codierten Audiowert.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-122">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="4bb5f-123">In der Regel wird die Qualität der codierten Audiodaten durch eine Anzahl von Stichproben pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-123">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="4bb5f-124">Beispielsweise wird CD Quality Sound bei 44.100-Stichproben pro Sekunde aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-124">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="4bb5f-125">Dieser Wert wird in der Regel mit der Hz-Notation abgekürzt, 44.100-Stichproben pro Sekunde wären also 44.100 Hz oder 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="4bb5f-125">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bb5f-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4bb5f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bb5f-127">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="4bb5f-127">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="4bb5f-128">**Inssbuffer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4bb5f-128">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="4bb5f-129">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="4bb5f-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




