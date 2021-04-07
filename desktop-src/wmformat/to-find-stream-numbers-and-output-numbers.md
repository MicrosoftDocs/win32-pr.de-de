---
title: So suchen Sie nach streamnummern und Ausgabe Nummern
description: So suchen Sie nach streamnummern und Ausgabe Nummern
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Advanced Systems Format (ASF), streamnummern
- ASF (Advanced Systems Format), Erstellen von Zahlen
- Advanced Systems Format (ASF), suchen nach Ausgabe Nummern
- ASF (Advanced Systems Format), suchen nach Ausgabe Nummern
- synchrone Reader, streamnummern
- synchrone Leser, suchen nach Ausgabe Nummern
- Streams, suchen nach Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723464"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a><span data-ttu-id="a1557-110">So suchen Sie nach streamnummern und Ausgabe Nummern</span><span class="sxs-lookup"><span data-stu-id="a1557-110">To Find Stream Numbers and Output Numbers</span></span>

<span data-ttu-id="a1557-111">Der synchrone Reader unterstützt den vereinfachten Wechsel zwischen Stream und Ausgabe Nummern für die Wiedergabe als der asynchrone Reader.</span><span class="sxs-lookup"><span data-stu-id="a1557-111">The synchronous reader supports more simplified switching between stream and output numbers for playback than the asynchronous reader.</span></span> <span data-ttu-id="a1557-112">Daher ist es wichtiger, dass Sie in der Lage sein können, zu ermitteln, welche streamnummern mit welchen ausgabezahlen gleich sind.</span><span class="sxs-lookup"><span data-stu-id="a1557-112">It is therefore more important to be able to find which stream numbers equate to which output numbers, or the other way around.</span></span>

<span data-ttu-id="a1557-113">Um die Ausgabe Nummer zu ermitteln, die einer Datenstrom Nummer entspricht, nennen Sie [**iwmsynkreader:: getoutputnumforstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span><span class="sxs-lookup"><span data-stu-id="a1557-113">To find the output number that corresponds to a stream number, call [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span></span>

<span data-ttu-id="a1557-114">Um die Datenstrom Nummer zu ermitteln, die einer Ausgabe Nummer entspricht, nennen Sie [ **iwmsynkreader:: getstreamnumforoutput** .](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span><span class="sxs-lookup"><span data-stu-id="a1557-114">To find the stream number that corresponds to an output number, call [**IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1557-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1557-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1557-116">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a1557-116">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="a1557-117">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="a1557-117">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="a1557-118">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="a1557-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




