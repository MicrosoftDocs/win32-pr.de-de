---
description: Die cvideotransformfilter-Klasse ist hauptsächlich als Basisklasse für AVI-dedaemon-Filter konzipiert.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Cvideotransformfilter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860515"
---
# <a name="cvideotransformfilter-class"></a><span data-ttu-id="025fa-103">Cvideotransformfilter-Klasse</span><span class="sxs-lookup"><span data-stu-id="025fa-103">CVideoTransformFilter class</span></span>

![cvideotransformfilter-Klassenhierarchie](images/vtsip01.png)

<span data-ttu-id="025fa-105">Die- `CVideoTransformFilter` Klasse ist hauptsächlich als Basisklasse für AVI-Dekompressor-Filter konzipiert.</span><span class="sxs-lookup"><span data-stu-id="025fa-105">The `CVideoTransformFilter` class is designed primarily as a base class for AVI decompressor filters.</span></span> <span data-ttu-id="025fa-106">Diese Klasse fügt der [**ctransformfilter**](ctransformfilter.md) -Klasse Unterstützung für die Qualitätskontrolle hinzu.</span><span class="sxs-lookup"><span data-stu-id="025fa-106">This class adds support for quality control to the [**CTransformFilter**](ctransformfilter.md) class.</span></span> <span data-ttu-id="025fa-107">Die **Receive** -Methode des Filters kann festlegen, ob Frames auf der Grundlage von Qualitäts Meldungen vom Renderer und Leistungsmessungen, die der Filter beim Streaming sammelt, gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="025fa-107">The filter's **Receive** method can decide to drop frames, based on quality messages from the renderer and performance measurements that the filter collects while it is streaming.</span></span>

<span data-ttu-id="025fa-108">Wenn der Filter einen Frame löscht, werden die Frames so lange gelöscht, bis der nächste Keyframe erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="025fa-108">If the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="025fa-109">Bei MPEG-Streams unterscheidet der Filter nicht zwischen B-Frames und P-Frames.</span><span class="sxs-lookup"><span data-stu-id="025fa-109">For MPEG streams, the filter does not distinguish between B frames and P frames.</span></span>



| <span data-ttu-id="025fa-110">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="025fa-110">Protected Member Variables</span></span>                                                      | <span data-ttu-id="025fa-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="025fa-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="025fa-112">**m \_ bqualitychanged**</span><span class="sxs-lookup"><span data-stu-id="025fa-112">**m\_bQualityChanged**</span></span>](cvideotransformfilter-m-bqualitychanged.md)           | <span data-ttu-id="025fa-113">Gibt an, ob der Filter Frames gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="025fa-113">Indicates whether the filter has dropped frames.</span></span>                                               |
| [<span data-ttu-id="025fa-114">**m \_ bskipping**</span><span class="sxs-lookup"><span data-stu-id="025fa-114">**m\_bSkipping**</span></span>](cvideotransformfilter-m-bskipping.md)                       | <span data-ttu-id="025fa-115">Gibt an, ob der Filter derzeit Frames löscht.</span><span class="sxs-lookup"><span data-stu-id="025fa-115">Indicates whether the filter is currently dropping frames.</span></span>                                     |
| [<span data-ttu-id="025fa-116">**m \_ itravgdecode**</span><span class="sxs-lookup"><span data-stu-id="025fa-116">**m\_itrAvgDecode**</span></span>](cvideotransformfilter-m-itravgdecode.md)                 | <span data-ttu-id="025fa-117">Die durchschnittliche Zeitspanne, die zum Decodieren eines Frames benötigt wurde.</span><span class="sxs-lookup"><span data-stu-id="025fa-117">Average length of time it has taken to decode a frame.</span></span>                                         |
| [<span data-ttu-id="025fa-118">**m \_ itrlate**</span><span class="sxs-lookup"><span data-stu-id="025fa-118">**m\_itrLate**</span></span>](cvideotransformfilter-m-itrlate.md)                           | <span data-ttu-id="025fa-119">Gibt an, wie spät die Stichproben am Renderer eintreffen.</span><span class="sxs-lookup"><span data-stu-id="025fa-119">Indicates how late the samples are arriving at the renderer.</span></span>                                   |
| [<span data-ttu-id="025fa-120">**m \_ nframessincekeyframe**</span><span class="sxs-lookup"><span data-stu-id="025fa-120">**m\_nFramesSinceKeyFrame**</span></span>](cvideotransformfilter-m-nframessincekeyframe.md) | <span data-ttu-id="025fa-121">Die Anzahl der Frames, die der Filter seit dem letzten Keyframe empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="025fa-121">The number of frames that the filter has received since the last key frame.</span></span>                    |
| [<span data-ttu-id="025fa-122">**m \_ nkeyframeperiod**</span><span class="sxs-lookup"><span data-stu-id="025fa-122">**m\_nKeyFramePeriod**</span></span>](cvideotransformfilter-m-nkeyframeperiod.md)           | <span data-ttu-id="025fa-123">Das größte beobachtete Intervall zwischen Keyframes.</span><span class="sxs-lookup"><span data-stu-id="025fa-123">The largest observed interval between key frames.</span></span>                                              |
| [<span data-ttu-id="025fa-124">**m \_ nwaitforkey**</span><span class="sxs-lookup"><span data-stu-id="025fa-124">**m\_nWaitForKey**</span></span>](cvideotransformfilter-m-nwaitforkey.md)                   | <span data-ttu-id="025fa-125">Die aktuelle maximale Anzahl der zu löschenden Delta Frames.</span><span class="sxs-lookup"><span data-stu-id="025fa-125">The current maximum number of delta frames to drop.</span></span>                                            |
| [<span data-ttu-id="025fa-126">**m \_ tdecodestart**</span><span class="sxs-lookup"><span data-stu-id="025fa-126">**m\_tDecodeStart**</span></span>](cvideotransformfilter-m-tdecodestart.md)                 | <span data-ttu-id="025fa-127">Die Zeitspanne, die zum Decodieren des neuesten Beispiels benötigt wurde.</span><span class="sxs-lookup"><span data-stu-id="025fa-127">Length of time that it took to decode the most recent sample.</span></span>                                  |
| <span data-ttu-id="025fa-128">Geschützte Methoden</span><span class="sxs-lookup"><span data-stu-id="025fa-128">Protected Methods</span></span>                                                               | <span data-ttu-id="025fa-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="025fa-129">Description</span></span>                                                                                    |
| [<span data-ttu-id="025fa-130">**Abbruch Wiedergabe**</span><span class="sxs-lookup"><span data-stu-id="025fa-130">**AbortPlayback**</span></span>](cvideotransformfilter-abortplayback.md)                    | <span data-ttu-id="025fa-131">Wird verwendet, um einen Streamingfehler zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="025fa-131">Used to signal a streaming error.</span></span>                                                              |
| [<span data-ttu-id="025fa-132">**Alterquality**</span><span class="sxs-lookup"><span data-stu-id="025fa-132">**AlterQuality**</span></span>](cvideotransformfilter-alterquality.md)                      | <span data-ttu-id="025fa-133">Benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="025fa-133">Notifies the filter that a quality change is requested.</span></span>                                        |
| [<span data-ttu-id="025fa-134">**Medizinisch**</span><span class="sxs-lookup"><span data-stu-id="025fa-134">**Receive**</span></span>](cvideotransformfilter-receive.md)                                | <span data-ttu-id="025fa-135">Empfängt ein Medien Beispiel, verarbeitet es und stellt ein Ausgabe Beispiel für den downstreamfilter bereit.</span><span class="sxs-lookup"><span data-stu-id="025fa-135">Receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> |
| [<span data-ttu-id="025fa-136">**Schuldskipframe**</span><span class="sxs-lookup"><span data-stu-id="025fa-136">**ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)                | <span data-ttu-id="025fa-137">Bestimmt, ob der Filter eine angegebene Stichprobe löschen soll.</span><span class="sxs-lookup"><span data-stu-id="025fa-137">Determines whether the filter should drop a specified sample.</span></span>                                  |
| [<span data-ttu-id="025fa-138">**Startstreaming**</span><span class="sxs-lookup"><span data-stu-id="025fa-138">**StartStreaming**</span></span>](cvideotransformfilter-startstreaming.md)                  | <span data-ttu-id="025fa-139">Wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="025fa-139">Called when the filter switches to the paused state.</span></span>                                           |
| <span data-ttu-id="025fa-140">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="025fa-140">Public Methods</span></span>                                                                  | <span data-ttu-id="025fa-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="025fa-141">Description</span></span>                                                                                    |
| [<span data-ttu-id="025fa-142">**Cvideotransformfilter**</span><span class="sxs-lookup"><span data-stu-id="025fa-142">**CVideoTransformFilter**</span></span>](cvideotransformfilter-cvideotransformfilter.md)    | <span data-ttu-id="025fa-143">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="025fa-143">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="025fa-144">**Endflush**</span><span class="sxs-lookup"><span data-stu-id="025fa-144">**EndFlush**</span></span>](cvideotransformfilter-endflush.md)                              | <span data-ttu-id="025fa-145">Beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="025fa-145">Ends a flush operation.</span></span>                                                                        |



 

 

 



