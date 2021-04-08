---
title: So suchen Sie nach Zeit mithilfe des synchronen Readers
description: So suchen Sie nach Zeit mithilfe des synchronen Readers
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Advanced Systems Format (ASF), Suche nach Zeit
- ASF (Advanced Systems Format), Suche nach Zeit
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, suchen nach Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723560"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a><span data-ttu-id="96580-108">So suchen Sie nach Zeit mithilfe des synchronen Readers</span><span class="sxs-lookup"><span data-stu-id="96580-108">To Seek By Time Using the Synchronous Reader</span></span>

<span data-ttu-id="96580-109">Um mithilfe des synchronen Readers nach Daten zu suchen, geben Sie einen Bereich für die Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="96580-109">To seek for data using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="96580-110">Ein Bereich wird durch eine Start Präsentationszeit und eine Dauer, beide in 100-Nanosecond-Einheiten, definiert.</span><span class="sxs-lookup"><span data-stu-id="96580-110">A range is defined by a starting presentation time and a duration, both in 100-nanosecond units.</span></span>

<span data-ttu-id="96580-111">Führen Sie die folgenden Schritte aus, um mithilfe des synchronen Readers mithilfe des synchronen Readers Daten in einer ASF-Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="96580-111">To seek data in an ASF file by presentation time using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="96580-112">Geben Sie eine Startzeit und die Dauer für die Beispiel Übermittlung an, indem Sie [**iwmsyncreader:: abge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="96580-112">Specify a starting time and duration for sample delivery by calling [**IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span></span> <span data-ttu-id="96580-113">Diese Methode erfordert nicht, dass Sie eine Datenstrom Nummer angeben, da die Präsentations Zeiten der einzelnen Datenströme bereits synchronisiert sein sollten.</span><span class="sxs-lookup"><span data-stu-id="96580-113">This method does not require you to specify a stream number because the presentation times of each stream should already be synchronized.</span></span>
2.  <span data-ttu-id="96580-114">Beginnen Sie mit dem Abrufen von Beispielen mit Aufrufen von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="96580-114">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="96580-115">Fahren Sie wie gewohnt mit dem synchronen Reader fort.</span><span class="sxs-lookup"><span data-stu-id="96580-115">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96580-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96580-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96580-117">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="96580-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="96580-118">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="96580-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




