---
description: Medienquellen Ereignisse
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Medienquellen Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363036"
---
# <a name="media-source-events"></a><span data-ttu-id="9ea57-103">Medienquellen Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9ea57-103">Media Source Events</span></span>

<span data-ttu-id="9ea57-104">In diesem Thema werden die Ereignisse aufgelistet, die von Medienquellen und Mediendaten strömen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ea57-104">This topic lists the events that are sent by media sources and media streams.</span></span> <span data-ttu-id="9ea57-105">Medienquellen können auch benutzerdefinierte, hier nicht aufgelistete Ereignisse senden.</span><span class="sxs-lookup"><span data-stu-id="9ea57-105">Media sources can also send custom events not listed here.</span></span>

## <a name="media-source-events"></a><span data-ttu-id="9ea57-106">Medienquellen Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9ea57-106">Media Source Events</span></span>



| <span data-ttu-id="9ea57-107">Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-107">Event</span></span>                                                                      | <span data-ttu-id="9ea57-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ea57-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ea57-109">Meendof Presentation-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-109">MEEndOfPresentation Event</span></span>](meendofpresentation.md)                       | <span data-ttu-id="9ea57-110">Die Präsentation wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="9ea57-110">The presentation ended.</span></span> <span data-ttu-id="9ea57-111">Alle Streams in der Präsentation haben das Ende des Streams erreicht.</span><span class="sxs-lookup"><span data-stu-id="9ea57-111">All streams in the presentation have reached the end of the stream.</span></span>      |
| [<span data-ttu-id="9ea57-112">Menewstream-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-112">MENewStream Event</span></span>](menewstream.md)                                       | <span data-ttu-id="9ea57-113">Es wurde ein neuer Datenstrom erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ea57-113">A new stream was created.</span></span> <span data-ttu-id="9ea57-114">Das Ereignis enthält einen Zeiger auf den Stream.</span><span class="sxs-lookup"><span data-stu-id="9ea57-114">The event contains a pointer to the stream.</span></span>                            |
| [<span data-ttu-id="9ea57-115">Mesourcecharakteristicschge-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-115">MESourceCharacteristicsChanged Event</span></span>](mesourcecharacteristicschanged.md) | <span data-ttu-id="9ea57-116">Die Merkmale der Quelle wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="9ea57-116">The characteristics of the source have changed.</span></span> <span data-ttu-id="9ea57-117">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="9ea57-117">(Optional.)</span></span>                                      |
| [<span data-ttu-id="9ea57-118">MESourceMetadataChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-118">MESourceMetadataChanged Event</span></span>](mesourcemetadatachanged.md)               | <span data-ttu-id="9ea57-119">Die Metadaten der Quelle wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="9ea57-119">The source's metadata has changed.</span></span> <span data-ttu-id="9ea57-120">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="9ea57-120">(Optional.)</span></span>                                                   |
| [<span data-ttu-id="9ea57-121">Mesourcepaused-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-121">MESourcePaused Event</span></span>](mesourcepaused.md)                                 | <span data-ttu-id="9ea57-122">Die Quelle wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="9ea57-122">The source was paused.</span></span> <span data-ttu-id="9ea57-123">Nicht alle Quellen unterstützen das Anhalten.</span><span class="sxs-lookup"><span data-stu-id="9ea57-123">Not all sources support pausing.</span></span>                                          |
| [<span data-ttu-id="9ea57-124">Mesourceratechanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-124">MESourceRateChanged Event</span></span>](mesourceratechanged.md)                       | <span data-ttu-id="9ea57-125">Die Wiedergabe Rate der Quelle wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="9ea57-125">The source's playback rate has changed.</span></span> <span data-ttu-id="9ea57-126">(Optional; gilt, wenn die Quelle Raten Kontrolle unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="9ea57-126">(Optional; applies if the source supports rate control.)</span></span> |
| [<span data-ttu-id="9ea57-127">Mesourceratechangerequnost-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-127">MESourceRateChangeRequested Event</span></span>](mesourceratechangerequested.md)       | <span data-ttu-id="9ea57-128">Die Quelle fordert eine neue Wiedergabe Rate an.</span><span class="sxs-lookup"><span data-stu-id="9ea57-128">The source is requesting a new playback rate.</span></span> <span data-ttu-id="9ea57-129">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="9ea57-129">(Optional.)</span></span>                                        |
| [<span data-ttu-id="9ea57-130">Mesourceseeked-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-130">MESourceSeeked Event</span></span>](mesourceseeked.md)                                 | <span data-ttu-id="9ea57-131">Die Quelle wurde im Seeding angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ea57-131">The source was seeked.</span></span> <span data-ttu-id="9ea57-132">Nicht alle Quellen unterstützen Suchvorgänge.</span><span class="sxs-lookup"><span data-stu-id="9ea57-132">Not all sources support seeking.</span></span>                                          |
| [<span data-ttu-id="9ea57-133">Mesourcestarted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-133">MESourceStarted Event</span></span>](mesourcestarted.md)                               | <span data-ttu-id="9ea57-134">Die Quelle wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="9ea57-134">The source was started.</span></span>                                                                          |
| [<span data-ttu-id="9ea57-135">Mesourcestpt-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-135">MESourceStopped Event</span></span>](mesourcestopped.md)                               | <span data-ttu-id="9ea57-136">Die Quelle wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="9ea57-136">The source was stopped.</span></span>                                                                          |
| [<span data-ttu-id="9ea57-137">Meupdatedstream-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-137">MEUpdatedStream Event</span></span>](meupdatedstream.md)                               | <span data-ttu-id="9ea57-138">Ein vorhandener Stream wurde Seeding oder neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="9ea57-138">An existing stream was seeked or re-started.</span></span> <span data-ttu-id="9ea57-139">Das Ereignis enthält einen Zeiger auf den Stream.</span><span class="sxs-lookup"><span data-stu-id="9ea57-139">The event contains a pointer to the stream.</span></span>         |



 

## <a name="media-stream-events"></a><span data-ttu-id="9ea57-140">Medienstrom Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9ea57-140">Media Stream Events</span></span>



| <span data-ttu-id="9ea57-141">Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-141">Event</span></span>                                                    | <span data-ttu-id="9ea57-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ea57-142">Description</span></span>                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ea57-143">Meendof Stream-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-143">MEEndOfStream Event</span></span>](meendofstream.md)                 | <span data-ttu-id="9ea57-144">Der Stream wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="9ea57-144">The stream ended.</span></span>                                                                                                              |
| [<span data-ttu-id="9ea57-145">Meerror-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-145">MEError Event</span></span>](meerror.md)                             | <span data-ttu-id="9ea57-146">Beim Streaming ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9ea57-146">An error has occurred during streaming.</span></span> <span data-ttu-id="9ea57-147">Verwenden Sie dieses Ereignis für Fehler, die nicht mit einem der anderen hier aufgeführten Ereignisse verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="9ea57-147">Use this event for errors that are not related to any of the other events listed here.</span></span> |
| [<span data-ttu-id="9ea57-148">Memediasample-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-148">MEMediaSample Event</span></span>](memediasample.md)                 | <span data-ttu-id="9ea57-149">Der Stream hat ein neues Beispiel generiert.</span><span class="sxs-lookup"><span data-stu-id="9ea57-149">The stream has generated a new sample.</span></span>                                                                                         |
| [<span data-ttu-id="9ea57-150">Mestreamformatchanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-150">MEStreamFormatChanged Event</span></span>](mestreamformatchanged.md) | <span data-ttu-id="9ea57-151">Der Medientyp wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="9ea57-151">The media type has changed.</span></span> <span data-ttu-id="9ea57-152">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="9ea57-152">(Optional.)</span></span>                                                                                        |
| [<span data-ttu-id="9ea57-153">Mestreampaused-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-153">MEStreamPaused Event</span></span>](mestreampaused.md)               | <span data-ttu-id="9ea57-154">Der Stream wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="9ea57-154">The stream was paused.</span></span>                                                                                                         |
| [<span data-ttu-id="9ea57-155">Mestreamseeked-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-155">MEStreamSeeked Event</span></span>](mestreamseeked.md)               | <span data-ttu-id="9ea57-156">Der Stream wurde im Seeding angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ea57-156">The stream was seeked.</span></span>                                                                                                         |
| [<span data-ttu-id="9ea57-157">Mestreamstarted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-157">MEStreamStarted Event</span></span>](mestreamstarted.md)             | <span data-ttu-id="9ea57-158">Der Stream wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="9ea57-158">The stream was started.</span></span>                                                                                                        |
| [<span data-ttu-id="9ea57-159">Mestreambeendete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-159">MEStreamStopped Event</span></span>](mestreamstopped.md)             | <span data-ttu-id="9ea57-160">Der Stream wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="9ea57-160">The stream was stopped.</span></span>                                                                                                        |
| [<span data-ttu-id="9ea57-161">Mestreamthinmode-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-161">MEStreamThinMode Event</span></span>](mestreamthinmode.md)           | <span data-ttu-id="9ea57-162">Der thiningmodus wurde gestartet oder beendet.</span><span class="sxs-lookup"><span data-stu-id="9ea57-162">Thinning mode has started or stopped.</span></span> <span data-ttu-id="9ea57-163">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="9ea57-163">(Optional.)</span></span>                                                                              |
| [<span data-ttu-id="9ea57-164">Mestreamtick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ea57-164">MEStreamTick Event</span></span>](mestreamtick.md)                   | <span data-ttu-id="9ea57-165">Der Stream weist eine Lücke auf.</span><span class="sxs-lookup"><span data-stu-id="9ea57-165">There is a gap in the stream.</span></span> <span data-ttu-id="9ea57-166">(Optional.)</span><span class="sxs-lookup"><span data-stu-id="9ea57-166">(Optional.)</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="9ea57-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ea57-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ea57-168">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="9ea57-168">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



