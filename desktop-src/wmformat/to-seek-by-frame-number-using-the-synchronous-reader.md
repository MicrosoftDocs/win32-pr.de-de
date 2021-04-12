---
title: So suchen Sie nach Frame Nummer mithilfe des synchronen Readers
description: So suchen Sie nach Frame Nummer mithilfe des synchronen Readers
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Advanced Systems Format (ASF), Suche nach Frame Nummern
- ASF (Advanced Systems Format), Suche nach Frame Nummern
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, suchen nach Frame Nummern
- Videostreams, suchen nach Frame Nummern
- Videostreams, synchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314267"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a><span data-ttu-id="1553d-110">So suchen Sie nach Frame Nummer mithilfe des synchronen Readers</span><span class="sxs-lookup"><span data-stu-id="1553d-110">To Seek By Frame Number Using the Synchronous Reader</span></span>

<span data-ttu-id="1553d-111">Zum Suchen nach Daten nach Frame Nummer mithilfe des synchronen Readers geben Sie einen Bereich für die Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="1553d-111">To seek for data by frame number using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="1553d-112">Ein Bereich wird durch eine Start Rahmennummer in einem bestimmten Videostream und eine Anzahl von Frames definiert.</span><span class="sxs-lookup"><span data-stu-id="1553d-112">A range is defined by a starting frame number in a specific video stream and a number of frames to play.</span></span>

<span data-ttu-id="1553d-113">Führen Sie die folgenden Schritte aus, um mithilfe des synchronen Readers Daten in einer ASF-Datei nach Frame Nummer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1553d-113">To seek data in an ASF file by frame number using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="1553d-114">Legen Sie die Start Frame Nummer und die Anzahl der Frames für die Beispiel Übermittlung durch Aufrufen von [**iwmsyncreader:: setrangebyframe**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe)fest.</span><span class="sxs-lookup"><span data-stu-id="1553d-114">Set the starting frame number and number of frames to read for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="1553d-115">Sie müssen die streamnummer eines Frame indizierten Videostreams angeben.</span><span class="sxs-lookup"><span data-stu-id="1553d-115">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="1553d-116">Der Reader synchronisiert den Rest der Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt damit, Ausgabe Beispiele bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1553d-116">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
2.  <span data-ttu-id="1553d-117">Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="1553d-117">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="1553d-118">Fahren Sie wie gewohnt mit dem synchronen Reader fort.</span><span class="sxs-lookup"><span data-stu-id="1553d-118">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1553d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1553d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1553d-120">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1553d-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="1553d-121">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="1553d-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




