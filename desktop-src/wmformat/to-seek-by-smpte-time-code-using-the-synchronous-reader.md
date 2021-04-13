---
title: So suchen Sie nach SMPTE-Zeit Code mithilfe des synchronen Readers
description: So suchen Sie nach SMPTE-Zeit Code mithilfe des synchronen Readers
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Advanced Systems Format (ASF), Suche nach SMPTE-Zeit Codes
- ASF (Advanced Systems Format), Suche nach SMPTE-Zeit Codes
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), SMPTE-Zeit Codes
- ASF (Advanced Systems Format), SMPTE-Zeit Codes
- synchrone Reader, Suche nach SMPTE-Zeit Codes
- synchrone Reader, SMPTE-Zeit Codes
- SMPTE-Zeit Codes, suchen
- SMPTE-Zeit Codes, synchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314327"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a><span data-ttu-id="48888-113">So suchen Sie nach SMPTE-Zeit Code mithilfe des synchronen Readers</span><span class="sxs-lookup"><span data-stu-id="48888-113">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>

<span data-ttu-id="48888-114">Das synchrone Reader-Objekt kann basierend auf dem SMPTE-Zeit Code, der einem Videostream zugeordnet ist, zu einem Punkt in einer Datei suchen.</span><span class="sxs-lookup"><span data-stu-id="48888-114">The synchronous reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="48888-115">Zeit Code Daten werden in [**WMT-Zeit \_ Code \_ Erweiterungs \_ Daten**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) Strukturen gekapselt, die an Videobeispiele als Dateneinheiten Erweiterungen angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="48888-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="48888-116">SMPTE-Zeit Codes werden durch einen Bereich und einen Zeit Code in diesem Bereich definiert.</span><span class="sxs-lookup"><span data-stu-id="48888-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="48888-117">Ein Bereich ist eine fortlaufende Reihe von Zeit Codes.</span><span class="sxs-lookup"><span data-stu-id="48888-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="48888-118">Jedes Mal, wenn Code durch Stunden, Minuten, Sekunden und Frames definiert wird.</span><span class="sxs-lookup"><span data-stu-id="48888-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="48888-119">Führen Sie die folgenden Schritte aus, um mithilfe des synchronen Readers Daten in einer ASF-Datei nach SMPTE-Zeit Code zu suchen.</span><span class="sxs-lookup"><span data-stu-id="48888-119">To seek data in an ASF file by SMPTE time code using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="48888-120">Legen Sie den Start-und Endzeit Code für die Beispiel Übermittlung durch Aufrufen von [**iwmsyncreader:: setrangebyframe**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)fest.</span><span class="sxs-lookup"><span data-stu-id="48888-120">Set the starting time code and ending time code for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="48888-121">Sie müssen die streamnummer eines Videodaten Stroms angeben, der nach Zeit Code indiziert ist.</span><span class="sxs-lookup"><span data-stu-id="48888-121">You must specify the stream number of a video stream indexed by time code.</span></span> <span data-ttu-id="48888-122">Der synchrone Reader synchronisiert den Rest der Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams.</span><span class="sxs-lookup"><span data-stu-id="48888-122">The synchronous reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream.</span></span>
2.  <span data-ttu-id="48888-123">Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="48888-123">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="48888-124">Fahren Sie wie gewohnt mit dem synchronen Reader fort.</span><span class="sxs-lookup"><span data-stu-id="48888-124">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48888-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48888-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48888-126">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="48888-126">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="48888-127">**SMPTE-Zeit Code Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="48888-127">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> <dt>

[<span data-ttu-id="48888-128">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="48888-128">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




