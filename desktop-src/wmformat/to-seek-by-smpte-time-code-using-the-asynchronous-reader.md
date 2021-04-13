---
title: So suchen Sie nach SMPTE-Zeit Code mithilfe des asynchronen Readers
description: So suchen Sie nach SMPTE-Zeit Code mithilfe des asynchronen Readers
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Advanced Systems Format (ASF), Suche nach SMPTE-Zeit Codes
- ASF (Advanced Systems Format), Suche nach SMPTE-Zeit Codes
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), SMPTE-Zeit Codes
- ASF (Advanced Systems Format), SMPTE-Zeit Codes
- asynchrone Leser, Suche nach SMPTE-Zeit Codes
- asynchrone Leser, SMPTE-Zeit Codes
- SMPTE-Zeit Codes, suchen
- SMPTE-Zeit Codes, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389840"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a><span data-ttu-id="9857c-113">So suchen Sie nach SMPTE-Zeit Code mithilfe des asynchronen Readers</span><span class="sxs-lookup"><span data-stu-id="9857c-113">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>

<span data-ttu-id="9857c-114">Das Reader-Objekt kann basierend auf dem SMPTE-Zeit Code, der einem Videostream zugeordnet ist, zu einem Punkt in einer Datei suchen.</span><span class="sxs-lookup"><span data-stu-id="9857c-114">The reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="9857c-115">Zeit Code Daten werden in [**WMT-Zeit \_ Code \_ Erweiterungs \_ Daten**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) Strukturen gekapselt, die an Videobeispiele als Dateneinheiten Erweiterungen angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9857c-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="9857c-116">SMPTE-Zeit Codes werden durch einen Bereich und einen Zeit Code in diesem Bereich definiert.</span><span class="sxs-lookup"><span data-stu-id="9857c-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="9857c-117">Ein Bereich ist eine fortlaufende Reihe von Zeit Codes.</span><span class="sxs-lookup"><span data-stu-id="9857c-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="9857c-118">Jedes Mal, wenn Code durch Stunden, Minuten, Sekunden und Frames definiert wird.</span><span class="sxs-lookup"><span data-stu-id="9857c-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="9857c-119">Führen Sie die folgenden Schritte aus, um mithilfe des asynchronen Readers Daten in einer ASF-Datei nach SMPTE-Zeit Code zu suchen.</span><span class="sxs-lookup"><span data-stu-id="9857c-119">To seek data in an ASF file by SMPTE time code using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="9857c-120">Abrufen eines Zeigers auf die [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9857c-120">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="9857c-121">Legen Sie den Start Zeit Code und die Dauer fest, indem Sie [**IWMReaderAdvanced3:: startatposition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9857c-121">Set the starting time code and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="9857c-122">Sie müssen die streamnummer eines Videodaten Stroms angeben, der nach Zeit Code indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9857c-122">You must specify the stream number of a video stream that is indexed by time code.</span></span> <span data-ttu-id="9857c-123">Der Reader synchronisiert den Rest der Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt damit, Ausgabe Beispiele bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9857c-123">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="9857c-124">Behandeln Sie die Beispiele wie in der Implementierung der **iwmreadercallback:: onsample** -Methode.</span><span class="sxs-lookup"><span data-stu-id="9857c-124">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9857c-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9857c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9857c-126">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="9857c-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="9857c-127">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="9857c-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="9857c-128">**SMPTE-Zeit Code Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="9857c-128">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> </dl>

 

 




