---
title: Reader-Antwort auf ASF-Features
description: Reader-Antwort auf ASF-Features
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media-Format-SDK, Leser Antworten auf ASF-Features
- Advanced Systems Format (ASF), Leser Antworten auf Features
- ASF (Advanced Systems Format), Reader-Antworten auf Features
- Antworten von Antworten auf ASF-Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339203"
---
# <a name="reader-response-to-asf-features"></a><span data-ttu-id="b510c-107">Reader-Antwort auf ASF-Features</span><span class="sxs-lookup"><span data-stu-id="b510c-107">Reader Response to ASF Features</span></span>

<span data-ttu-id="b510c-108">Die meisten der besonderen Features der ASF-Datei können in Dateien so festgelegt werden, dass Sie mit benutzerdefinierten Spielanwendungen interagieren, die für die Handhabung vorgesehen sind</span><span class="sxs-lookup"><span data-stu-id="b510c-108">Most of the special ASF file features can be set in files to interact with custom playing applications designed to handle them.</span></span> <span data-ttu-id="b510c-109">Einige der Features verfügen jedoch über integrierte Unterstützung im Reader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b510c-109">However, some of the features have built-in support in the reader object.</span></span>

<span data-ttu-id="b510c-110">Das Reader-Objekt wählt automatisch Streams aus Sätzen aus, die sich durch die Bitrate gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="b510c-110">The reader object will automatically select streams from sets that are mutually exclusive by bit rate.</span></span> <span data-ttu-id="b510c-111">Dieser Sonderfall wird als mehrfache Bitrate (Multiple Bitrate, MBR) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b510c-111">This special case is referred to as multiple bit rate (MBR).</span></span> <span data-ttu-id="b510c-112">Der vom Reader auswählt Stream basiert auf der Bitrate des Streams.</span><span class="sxs-lookup"><span data-stu-id="b510c-112">The stream the reader selects is based on the bit rate of the stream.</span></span> <span data-ttu-id="b510c-113">Die streamnummer und die Reihenfolge, in der Sie dem gegenseitigen Ausschluss Objekt hinzugefügt wurde, sind für die automatische Auswahl irrelevant.</span><span class="sxs-lookup"><span data-stu-id="b510c-113">The stream number and the order in which it was added to the mutual exclusion object are irrelevant to the automatic selection.</span></span> <span data-ttu-id="b510c-114">Wenn eine Datei mehr als einen Satz von Streams enthält, die sich gegenseitig von der Bitrate ausschließen, wählt der Reader Streams basierend auf der Berechnung der optimalen Nutzung der verfügbaren Bandbreite aus.</span><span class="sxs-lookup"><span data-stu-id="b510c-114">If a file includes more than one set of streams mutually exclusive by bit rate, the reader will select streams based on calculating the best use of the available bandwidth.</span></span>

<span data-ttu-id="b510c-115">Der sprachbasierte gegenseitige Ausschluss wird vor der Wiedergabe mithilfe einer Ausgabe Einstellung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b510c-115">Language-based mutual exclusion is set using an output setting, before playback.</span></span> <span data-ttu-id="b510c-116">Wenn Sie sowohl den sprach-als auch den Bitrate-basierten gegenseitigen Ausschluss kombinieren, sollten Sie die Bitrate-basierten, sich gegenseitig exklusiven Datenströme nach Sprache gruppieren und dann die Gruppen nach Sprache ausschließen.</span><span class="sxs-lookup"><span data-stu-id="b510c-116">If you combine both language and bit-rate-based mutual exclusion, you should group the bit-rate-based mutually exclusive streams by language and then make the groups mutually exclusive by language.</span></span> <span data-ttu-id="b510c-117">Der Reader prüft zuerst die Sprache und bestimmt dann, welche Bitrate verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b510c-117">The reader will check the language first, and then determine which bit rate to use.</span></span>

<span data-ttu-id="b510c-118">Die streampriorisierung wird mithilfe eines Arrays von Datensätzen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b510c-118">Stream prioritization is set using an array of records.</span></span> <span data-ttu-id="b510c-119">Die Datensätze im Array sind in absteigender Reihenfolge der Priorität.</span><span class="sxs-lookup"><span data-stu-id="b510c-119">The records in the array are in descending order of priority.</span></span> <span data-ttu-id="b510c-120">Der letzte Datenstrom im Array ist der erste, der vom Reader gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b510c-120">The last stream in the array is the first that will be dropped by the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b510c-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b510c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b510c-122">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="b510c-122">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="b510c-123">**Gegenseitiger Ausschluss**</span><span class="sxs-lookup"><span data-stu-id="b510c-123">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="b510c-124">**Streampriorisierung**</span><span class="sxs-lookup"><span data-stu-id="b510c-124">**Stream Prioritization**</span></span>](stream-prioritization.md)
</dt> </dl>

 

 




