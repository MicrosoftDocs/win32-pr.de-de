---
title: Auswählen von Bitraten
description: Auswählen von Bitraten
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- Profile, auswählen von Bitraten
- Profile, Bitraten
- Codecs, auswählen von Bitraten
- Codecs, Bitraten
- Profile, auswählen von Bitraten
- Codecs, auswählen von Bitraten
- Bitraten, auswählen
- Bitraten, profile
- Bitraten, Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309160"
---
# <a name="selecting-bit-rates"></a><span data-ttu-id="26b8c-112">Auswählen von Bitraten</span><span class="sxs-lookup"><span data-stu-id="26b8c-112">Selecting Bit Rates</span></span>

<span data-ttu-id="26b8c-113">Bei Dateien, die über ein Netzwerk gestreamt werden, müssen Sie sorgfältig überlegen, welche Bitraten Sie verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="26b8c-113">For files that will be streamed over a network, you must consider carefully what bit rates you should use.</span></span> <span data-ttu-id="26b8c-114">In den meisten Fällen können Sie die Bitraten aller Streams in einer Datei hinzufügen, um eine allgemeine Vorstellung von der verfügbaren Bandbreite zu erhalten, die zum Streamen der Datei erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="26b8c-114">Under most circumstances you can add the bit rates of all of the streams in a file together to get a general idea of the available bandwidth required to stream the file.</span></span> <span data-ttu-id="26b8c-115">Eine bestimmte Menge an mehr Aufwand ist jedoch auch für jeden Stream erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26b8c-115">However, a certain amount of overhead is also required for each stream.</span></span> <span data-ttu-id="26b8c-116">Dieser mehr Aufwand wird in der folgenden Tabelle zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="26b8c-116">This overhead is summarized in the following table.</span></span>



| <span data-ttu-id="26b8c-117">Bitraten Bereich (Kbit/s)</span><span class="sxs-lookup"><span data-stu-id="26b8c-117">Bit-rate range (Kbps)</span></span> | <span data-ttu-id="26b8c-118">Zusätzliche Bandbreite für mehr Aufwand erforderlich (Kbit/s)</span><span class="sxs-lookup"><span data-stu-id="26b8c-118">Additional bandwidth required for overhead (Kbps)</span></span> |
|-----------------------|---------------------------------------------------|
| <span data-ttu-id="26b8c-119">10 – 16</span><span class="sxs-lookup"><span data-stu-id="26b8c-119">10 – 16</span></span>               | <span data-ttu-id="26b8c-120">3</span><span class="sxs-lookup"><span data-stu-id="26b8c-120">3</span></span>                                                 |
| <span data-ttu-id="26b8c-121">17 – 30</span><span class="sxs-lookup"><span data-stu-id="26b8c-121">17 – 30</span></span>               | <span data-ttu-id="26b8c-122">4</span><span class="sxs-lookup"><span data-stu-id="26b8c-122">4</span></span>                                                 |
| <span data-ttu-id="26b8c-123">31 – 45</span><span class="sxs-lookup"><span data-stu-id="26b8c-123">31 – 45</span></span>               | <span data-ttu-id="26b8c-124">5</span><span class="sxs-lookup"><span data-stu-id="26b8c-124">5</span></span>                                                 |
| <span data-ttu-id="26b8c-125">46 – 70</span><span class="sxs-lookup"><span data-stu-id="26b8c-125">46 – 70</span></span>               | <span data-ttu-id="26b8c-126">6</span><span class="sxs-lookup"><span data-stu-id="26b8c-126">6</span></span>                                                 |
| <span data-ttu-id="26b8c-127">71 – 225</span><span class="sxs-lookup"><span data-stu-id="26b8c-127">71 – 225</span></span>              | <span data-ttu-id="26b8c-128">7</span><span class="sxs-lookup"><span data-stu-id="26b8c-128">7</span></span>                                                 |
| <span data-ttu-id="26b8c-129">>225</span><span class="sxs-lookup"><span data-stu-id="26b8c-129">>225</span></span>               | <span data-ttu-id="26b8c-130">9</span><span class="sxs-lookup"><span data-stu-id="26b8c-130">9</span></span>                                                 |



 

<span data-ttu-id="26b8c-131">Der für einen Datenstrom erforderliche normale Aufwand nimmt keine Dateneinheiten Erweiterungen in Betracht.</span><span class="sxs-lookup"><span data-stu-id="26b8c-131">The normal overhead required for a stream does not take data unit extensions into account.</span></span> <span data-ttu-id="26b8c-132">Jede dateneinheits Erweiterung fügt der Größe des Beispiels hinzu, an das Sie angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="26b8c-132">Every data unit extension adds to the size of the sample to which it is attached.</span></span> <span data-ttu-id="26b8c-133">Abhängig vom Typ der dateneinheits Erweiterung kann dadurch die Bitrate für den Stream erheblich erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="26b8c-133">Depending upon the type of data unit extension, this can greatly increase the bit rate for the stream.</span></span>

<span data-ttu-id="26b8c-134">Sie müssen auch Bedenken, dass die theoretische maximale Bandbreite, die über eine Netzwerkverbindung verfügbar ist, keine praktische Zielbitrate ist.</span><span class="sxs-lookup"><span data-stu-id="26b8c-134">You must also consider that the theoretical maximum bandwidth available over a network connection is not a practical target bit rate.</span></span> <span data-ttu-id="26b8c-135">Die durchschnittliche verfügbare Bandbreite für eine beliebige Verbindung ist aufgrund des Netzwerkverkehrs und vieler anderer Faktoren eine kurze Bandbreitenkapazität für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="26b8c-135">The average available bandwidth for any given connection falls well short of the bandwidth capacity of the connection, because of network traffic and many other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26b8c-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26b8c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26b8c-137">**Entwerfen von Profilen**</span><span class="sxs-lookup"><span data-stu-id="26b8c-137">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> </dl>

 

 




