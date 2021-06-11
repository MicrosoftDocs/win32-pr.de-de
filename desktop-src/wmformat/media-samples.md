---
title: Medienbeispiele (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über Medienbeispiele im Windows Media Format 11 SDK. Ein Medienbeispiel ist ein Objekt, das eine sortierte Liste von null oder mehr Puffern enthält.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK, Medienbeispiele
- Windows Media Format SDK, Beispiele
- Advanced Systems Format (ASF), Medienbeispiele
- ASF (Advanced Systems Format), Medienbeispiele
- Advanced Systems Format (ASF), Beispiele
- ASF (Advanced Systems Format), Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b8d264aa23e80f1e692f28789c2f2e631ef3ed8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989073"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="12020-110">Medienbeispiele (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="12020-110">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="12020-111">Ein Medienbeispiel oder Beispiel ist ein Block digitaler Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="12020-111">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="12020-112">Ein Beispiel ist die grundlegende Einheit, die durch das Lesen und Schreiben von Objekten des Windows Media Format SDK bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="12020-112">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="12020-113">Der Inhalt eines einzelnen Beispiels wird durch den Medientyp vorgegeben, der dem Beispiel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="12020-113">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="12020-114">Für Videos stellt jedes Beispiel einen einzelnen Frame dar.</span><span class="sxs-lookup"><span data-stu-id="12020-114">For video, each sample represents a single frame.</span></span> <span data-ttu-id="12020-115">Für Audiodaten wird die Datenmenge in einem einzelnen Beispiel in dem Profil festgelegt, das zum Erstellen der ASF-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12020-115">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="12020-116">Beispiele können unkomprimierte Daten enthalten, oder sie können komprimierte Daten enthalten. In diesem Fall werden sie *als Streambeispiele* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="12020-116">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="12020-117">Beim Erstellen einer ASF-Datei übergeben Sie Beispiele an den Writer.</span><span class="sxs-lookup"><span data-stu-id="12020-117">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="12020-118">Der Writer koordiniert die Komprimierung der Stichproben mit dem entsprechenden Codec und ordnet die komprimierten Daten im Datenabschnitt der ASF-Datei an.</span><span class="sxs-lookup"><span data-stu-id="12020-118">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="12020-119">Bei der Wiedergabe liest der Reader die komprimierten Daten, dekomprimiert sie und stellt die rekonstruierten unkomprimierten Daten als Ausgabebeispiele bereit.</span><span class="sxs-lookup"><span data-stu-id="12020-119">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="12020-120">Alle vom Windows Media Format SDK verwendeten Beispiele werden im Pufferobjekt gekapselt, dessen Arbeitsspeicher automatisch von den SDK-Laufzeitkomponenten zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="12020-120">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="12020-121">Sie können bei Bedarf auch eigene Puffer zuordnen, indem Sie erweiterte Features des Writers und Readers verwenden.</span><span class="sxs-lookup"><span data-stu-id="12020-121">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="12020-122">**Hinweis** Der Begriff Sample wird in diesem SDK verwendet, um auf ein Medienbeispiel und nicht auf ein Audiobeispiel zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="12020-122">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="12020-123">Bei der Audiocodierung bezieht sich ein Beispiel auf einen einzelnen codierten Audiowert.</span><span class="sxs-lookup"><span data-stu-id="12020-123">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="12020-124">In der Regel wird die Qualität codierter Audiodaten durch eine Reihe von Stichproben pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="12020-124">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="12020-125">Beispielsweise wird cd quality sound mit 44.100 Stichproben pro Sekunde aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="12020-125">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="12020-126">Dieser Wert wird häufig mit der Hz-Notation abgekürzt, sodass 44.100 Stichproben pro Sekunde 44.100 Hz oder 44,1 kHz betragen würden.</span><span class="sxs-lookup"><span data-stu-id="12020-126">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12020-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12020-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12020-128">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="12020-128">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="12020-129">**INSSBuffer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="12020-129">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="12020-130">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="12020-130">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




