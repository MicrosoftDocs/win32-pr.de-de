---
description: Geben Sie-1 im Vergleich zu
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Type-1 im Vergleich zu Type-2 DV AVI-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959939"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a><span data-ttu-id="6e079-103">Type-1 im Vergleich zu Type-2 DV AVI-Dateien</span><span class="sxs-lookup"><span data-stu-id="6e079-103">Type-1 vs. Type-2 DV AVI Files</span></span>

<span data-ttu-id="6e079-104">DV-Kameras liefern überlappende Audiovideo. jeder Frame des Videos enthält auch die Audioinformationen.</span><span class="sxs-lookup"><span data-stu-id="6e079-104">DV cameras produce interleaved audio-video; each frame of video also contains the audio information.</span></span> <span data-ttu-id="6e079-105">Wenn Sie DV-Daten in einer AVI-Datei speichern, haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="6e079-105">If you save DV data to an AVI file, you have a choice:</span></span>

-   <span data-ttu-id="6e079-106">Speichern Sie die verschachtelten Daten als einen Datenstrom in der AVI-Datei.</span><span class="sxs-lookup"><span data-stu-id="6e079-106">Store the interleaved data as one stream in the AVI file.</span></span> <span data-ttu-id="6e079-107">Dies wird als Type-1-Datei bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6e079-107">This is known as a type-1 file.</span></span>
-   <span data-ttu-id="6e079-108">Teilen Sie die verschachtelten Daten in separate Audiodaten und Videostreams auf.</span><span class="sxs-lookup"><span data-stu-id="6e079-108">Split the interleaved data into separate audio and video streams.</span></span> <span data-ttu-id="6e079-109">Dies wird als Type-2-Datei bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6e079-109">This is known as a type-2 file.</span></span>

<span data-ttu-id="6e079-110">Bei der Video Erfassung, bei der der maximale Durchsatz entscheidend ist, ist es besser, eine Type-1-Datei zu verwenden, da Type-2-Dateien redundante Audiodaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="6e079-110">For video capture, where maximum throughput is crucial, it is better to use a type-1 file, because type-2 files carry redundant audio data.</span></span> <span data-ttu-id="6e079-111">(Der Videostream enthält immer noch die Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="6e079-111">(The video stream still has the audio data.</span></span> <span data-ttu-id="6e079-112">Die Audiodaten werden einfach ausgeblendet, indem der Stream als Video gekennzeichnet wird.) Außerdem erfordert das Schreiben einer Type-2-Datei eine zusätzliche Prozessorzeit, um den verschachtelten Stream aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="6e079-112">The audio is simply hidden by labeling the stream as video.) Also, writing a type-2 file requires some additional processor time to split the interleaved stream.</span></span>

<span data-ttu-id="6e079-113">Allerdings sind Typ-1-Dateien für die Echtzeitbearbeitung weniger effizient.</span><span class="sxs-lookup"><span data-stu-id="6e079-113">On the other hand, type-1 files are less efficient for real-time editing.</span></span> <span data-ttu-id="6e079-114">Die Anwendung muss die Audiodatei aus dem überlappenden Datenstrom extrahieren, die Änderungen vornehmen und die Daten erneut interaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6e079-114">The application must extract the audio from the interleaved stream, make the edits, and interleave the data again.</span></span> <span data-ttu-id="6e079-115">Außerdem ist das Type-1-Format nicht mit Microsoft® Video für Windows® (Vfw) kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6e079-115">Also, the type-1 format is not compatible with Microsoft® Video for Windows® (VFW).</span></span> <span data-ttu-id="6e079-116">DirectShow kann beide Dateitypen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6e079-116">DirectShow can handle both types of files.</span></span>

<span data-ttu-id="6e079-117">Eine Type-2-Datei kann mit dem [DV-Muxer](dv-muxer-filter.md) -Filter in Typ-1 konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e079-117">A type-2 file can be converted to type-1 using the [DV Muxer](dv-muxer-filter.md) filter.</span></span> <span data-ttu-id="6e079-118">Eine Type-1-Datei kann mit dem [DV-Splitter](dv-splitter-filter.md) Filter in Typ-2 konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="6e079-118">A type-1 file can be converted to type-2 using the [DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="6e079-119">Das folgende Diagramm veranschaulicht den Unterschied zwischen den beiden Formaten.</span><span class="sxs-lookup"><span data-stu-id="6e079-119">The following diagram illustrates the difference between the two formats.</span></span>

![Konvertierung zwischen Typ-1 und Typ-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a><span data-ttu-id="6e079-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e079-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e079-122">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6e079-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6e079-123">DV-Daten im AVI-Datei Format</span><span class="sxs-lookup"><span data-stu-id="6e079-123">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



