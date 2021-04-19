---
description: In diesem Thema wird beschrieben, wie die Sequencer-Quelle verwendet wird.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Verwenden der Sequencer-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356574"
---
# <a name="using-the-sequencer-source"></a><span data-ttu-id="6706b-103">Verwenden der Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="6706b-103">Using the Sequencer Source</span></span>

<span data-ttu-id="6706b-104">In diesem Thema wird beschrieben, wie die [Sequencer-Quelle](sequencer-source.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6706b-104">This topic describes how to use the [Sequencer Source](sequencer-source.md).</span></span> <span data-ttu-id="6706b-105">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6706b-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="6706b-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6706b-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="6706b-107">Hinzufügen von Topologien</span><span class="sxs-lookup"><span data-stu-id="6706b-107">Adding Topologies</span></span>](#adding-topologies)
-   [<span data-ttu-id="6706b-108">Löschen von Topologien</span><span class="sxs-lookup"><span data-stu-id="6706b-108">Deleting Topologies</span></span>](#deleting-topologies)
-   [<span data-ttu-id="6706b-109">Überspringen zu einem Segment</span><span class="sxs-lookup"><span data-stu-id="6706b-109">Skipping to a Segment</span></span>](#skipping-to-a-segment)
-   [<span data-ttu-id="6706b-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6706b-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="6706b-111">Eine allgemeine Übersicht über die Sequencer-Quelle finden Sie unter [Informationen zur Sequencer-Quelle](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="6706b-111">For a general overview of the sequencer source, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

## <a name="overview"></a><span data-ttu-id="6706b-112">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6706b-112">Overview</span></span>

<span data-ttu-id="6706b-113">Die Sequencer-Quelle macht die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6706b-113">The sequencer source exposes the following interfaces.</span></span>



| <span data-ttu-id="6706b-114">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6706b-114">Interface</span></span>                                                                        | <span data-ttu-id="6706b-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6706b-115">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6706b-116">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="6706b-116">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | <span data-ttu-id="6706b-117">Macht Funktionen der generischen Medienquelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6706b-117">Exposes generic media source functionality.</span></span>                                        |
| [<span data-ttu-id="6706b-118">**IMF sequencersource**</span><span class="sxs-lookup"><span data-stu-id="6706b-118">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | <span data-ttu-id="6706b-119">Ermöglicht es der Anwendung, Topologien hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6706b-119">Enables the application to add or remove topologies.</span></span>                               |
| [<span data-ttu-id="6706b-120">**Imfmediasourcetopologyprovider**</span><span class="sxs-lookup"><span data-stu-id="6706b-120">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | <span data-ttu-id="6706b-121">Ruft die nächste Topologie in die Warteschlange für die Medien Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="6706b-121">Retrieves the next topology to queue on the Media Session.</span></span>                         |
| [<span data-ttu-id="6706b-122">**Imfmediasourcepresentationprovider**</span><span class="sxs-lookup"><span data-stu-id="6706b-122">**IMFMediaSourcePresentationProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | <span data-ttu-id="6706b-123">Wird von der Medien Sitzung zum Beenden von Segmenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="6706b-123">Used by the Media Session to end segments.</span></span> <span data-ttu-id="6706b-124">Diese Schnittstelle wird von Anwendungen nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6706b-124">Applications do not use this interface.</span></span> |
| [<span data-ttu-id="6706b-125">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="6706b-125">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | <span data-ttu-id="6706b-126">Fragt die Sequencer-Quelle für [Dienst Schnittstellen](service-interfaces.md)ab.</span><span class="sxs-lookup"><span data-stu-id="6706b-126">Queries the sequencer source for [Service Interfaces](service-interfaces.md).</span></span>     |



 

<span data-ttu-id="6706b-127">Führen Sie die folgenden Schritte aus, um eine Sequenz von Medienquellen wiederzugeben:</span><span class="sxs-lookup"><span data-stu-id="6706b-127">To play a sequence of media sources, perform the following steps:</span></span>

1.  <span data-ttu-id="6706b-128">Um die Sequencer-Quelle zu erstellen, rufen Sie die [**mfkreatesequencersource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="6706b-128">To create the sequencer source, call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function.</span></span>
2.  <span data-ttu-id="6706b-129">Erstellen Sie für jedes Segment eine Wiedergabe Topologie, wie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6706b-129">For each segment, create a playback topology, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span> <span data-ttu-id="6706b-130">Um der Präsentation die Topologie hinzuzufügen, nennen Sie [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="6706b-130">To add the topology to the presentation, call [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span>
3.  <span data-ttu-id="6706b-131">Bevor Sie die Wiedergabe starten, müssen Sie [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Sequencer-Quelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6706b-131">Before starting playback, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the sequencer source.</span></span> <span data-ttu-id="6706b-132">Diese Methode gibt einen Zeiger auf einen Präsentations Deskriptor für das erste Segment zurück.</span><span class="sxs-lookup"><span data-stu-id="6706b-132">This method returns a pointer to a presentation descriptor for the first segment.</span></span> <span data-ttu-id="6706b-133">Um die diesem Segment zugeordnete Topologie abzurufen, nennen Sie **QueryInterface** in der Sequencer-Quelle für die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6706b-133">To get the topology associated with this segment, call **QueryInterface** on the sequencer source for the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface.</span></span> <span data-ttu-id="6706b-134">Übergeben Sie den Präsentations Deskriptor an die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6706b-134">Pass the presentation descriptor to the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="6706b-135">Diese Methode gibt einen Zeiger auf die Topologie zurück.</span><span class="sxs-lookup"><span data-stu-id="6706b-135">This method returns a pointer to the topology.</span></span>
4.  <span data-ttu-id="6706b-136">Übergeben Sie die Topologie für das erste Segment an die Medien Sitzung, indem Sie die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode der Medien Sitzung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6706b-136">Pass the topology for the first segment to the Media Session, by calling the Media Session's [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>
5.  <span data-ttu-id="6706b-137">Wiedergabe durch Aufrufen von [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)starten.</span><span class="sxs-lookup"><span data-stu-id="6706b-137">Start playback by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>
6.  <span data-ttu-id="6706b-138">Wenn die Sequencer-Quelle für das vorab Ausführen des nächsten Segments bereit ist, sendet Sie ein [menewpresentation](menewpresentation.md) -Ereignis, dessen Ereignisdaten ein [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstellen Zeiger ist.</span><span class="sxs-lookup"><span data-stu-id="6706b-138">When the sequencer source is ready to preroll the next segment, it sends an [MENewPresentation](menewpresentation.md) event whose event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface pointer.</span></span> <span data-ttu-id="6706b-139">Rufen Sie die Topologie für das Segment ab, indem Sie [**getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) für die Sequencer-Quelle aufrufen, und legen Sie die Topologie für die Medien Sitzung fest, indem Sie [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6706b-139">Again, get the topology for the segment by calling [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the sequencer source, and set the topology on the Media Session by calling [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="6706b-140">Die Medienquelle muss nicht neu gestartet werden. Er wird automatisch bis zum nächsten Segment durchgespielt.</span><span class="sxs-lookup"><span data-stu-id="6706b-140">It is not necessary to re-start the media source; it will automatically play through to the next segment.</span></span>
7.  <span data-ttu-id="6706b-141">Bevor die Anwendung beendet wird, fahren Sie die Sequencer-Quelle durch Aufrufen von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)herunter.</span><span class="sxs-lookup"><span data-stu-id="6706b-141">Before the application quits, shut down the sequencer source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>

<span data-ttu-id="6706b-142">Der folgende Code zeigt, wie Sie die Topologie erhalten und in der Medien Sitzung festlegen:</span><span class="sxs-lookup"><span data-stu-id="6706b-142">The following code shows how to get the topology and set it on the Media Session:</span></span>


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="6706b-143">Ein umfassendes Codebeispiel finden Sie unter [Beispielcode für die Sequencer-Quelle](sequencer-source-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="6706b-143">For a complete code example, see [Sequencer Source Example Code](sequencer-source-example-code.md).</span></span>

## <a name="adding-topologies"></a><span data-ttu-id="6706b-144">Hinzufügen von Topologien</span><span class="sxs-lookup"><span data-stu-id="6706b-144">Adding Topologies</span></span>

<span data-ttu-id="6706b-145">Die Sequencer-Quelle verwaltet zwei Listen von Topologien: die *Eingabeliste* und die *vorab Liste*.</span><span class="sxs-lookup"><span data-stu-id="6706b-145">The sequencer source maintains two lists of topologies: the *input list* and the *preroll list*.</span></span>

<span data-ttu-id="6706b-146">Die Eingabeliste ist eine Auflistung von Topologien, die Wiedergabelisten Segmenten entsprechen, in der Reihenfolge, in der Sie durch die Anwendung hinzugefügt wurden, indem [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6706b-146">The input list is a collection of topologies corresponding to playlist segments, in the order that they were added by the application by calling [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span> <span data-ttu-id="6706b-147">Diese Methode weist jeder Topologie einen eindeutigen *Segment Bezeichner* des Typs **MF sequencerelementid** zu.</span><span class="sxs-lookup"><span data-stu-id="6706b-147">This method assigns each topology a unique *segment identifier* of the type **MFSequencerElementId**.</span></span> <span data-ttu-id="6706b-148">Der Segment Bezeichner wird als Attribut für alle Knoten der Quell Topologie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6706b-148">The segment identifier is set as an attribute for all source topology nodes.</span></span> <span data-ttu-id="6706b-149">Eine Anwendung kann den Segment Bezeichner von einem Quellknoten mit dem [Element "MF \_ toponode \_ Sequence \_ elementId](mf-toponode-sequence-elementid-attribute.md) " erhalten.</span><span class="sxs-lookup"><span data-stu-id="6706b-149">An application can get the segment identifier from a source node by using the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute.</span></span> <span data-ttu-id="6706b-150">Die Eingabeliste kann doppelte Topologien aufweisen, wenn die Anwendung **appendtopology** mehrmals in derselben Topologie aufrief. Sie werden jedoch durch Ihre eindeutigen Segment Bezeichner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6706b-150">The input list can have duplicate topologies if the application called **AppendTopology** on the same topology more than once; however, they are identified by their unique segment identifiers.</span></span>

<span data-ttu-id="6706b-151">Die ein Vorlauf ausgeführt-Liste ist eine Auflistung von Eingabe Listen Topologien, die zur Vorbereitung der Wiedergabe initialisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6706b-151">The preroll list is a collection of input list topologies that have been initialized in preparation for playback.</span></span> <span data-ttu-id="6706b-152">Dies ermöglicht es der Medien Sitzung, nahtlos zur nächsten Topologie zu wechseln, wenn die aktive Topologie endet.</span><span class="sxs-lookup"><span data-stu-id="6706b-152">This enables the Media Session to transition to the next topology seamlessly when the active topology ends.</span></span> <span data-ttu-id="6706b-153">Die Anwendung kann keine Topologien direkt aus der ein Vorlauf ausgeführt-Liste hinzufügen oder entfernen. Sie wird von der Sequencer-Quelle generiert, wenn eine Topologie aus der Eingabeliste für die Wiedergabe ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="6706b-153">The application cannot directly add or remove topologies from the preroll list; it is generated by the sequencer source when a topology from the input list is selected for playback.</span></span> <span data-ttu-id="6706b-154">Dies bewirkt, dass die Sequencer-Quelle die nächste Topologie aus der Eingabeliste der ein Vorlauf ausgeführt-Liste hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="6706b-154">This causes the sequencer source to add the next topology from the input list to the preroll list.</span></span> <span data-ttu-id="6706b-155">Danach löst die Sequencer-Quelle das Ereignis " [menewpresentation](menewpresentation.md) " asynchron aus und übergibt den Präsentations Deskriptor für die ein Vorlauf ausgeführt-Topologie als Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="6706b-155">After doing so, the sequencer source asynchronously raises the [MENewPresentation](menewpresentation.md) event and passes the presentation descriptor for the preroll topology as event data.</span></span> <span data-ttu-id="6706b-156">Die Anwendung muss dieses Ereignis überwachen, indem Sie die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle der Medien Sitzung verwendet und die ein Vorlauf ausgeführt-Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="6706b-156">The application must listen for this event by using the Media Session's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface and queue the preroll topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="6706b-157">Dies muss erfolgen, bevor die Wiedergabe der aktiven Topologie in der Medien Sitzung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6706b-157">This must be done before the Media Session completes playback of the active topology.</span></span> <span data-ttu-id="6706b-158">Die **settopologie** informiert die Medien Sitzung über die nächste Topologie, die Sie wiedergeben muss, nachdem die Wiedergabe der aktiven Topologie beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6706b-158">**SetTopology** informs the Media Session about the next topology that it must play after playback of the active topology has ended.</span></span> <span data-ttu-id="6706b-159">Um eine nahtlose treansition sicherzustellen, muss die Anwendung **settopology** aufzurufen, bevor die Medien Sitzung die Wiedergabe der vorherigen Topologie abschließt.</span><span class="sxs-lookup"><span data-stu-id="6706b-159">To ensure a seamless treansition, the application must call **SetTopology** before the Media Session completes playing the previous topology.</span></span> <span data-ttu-id="6706b-160">Andernfalls besteht eine Lücke zwischen den Segmenten.</span><span class="sxs-lookup"><span data-stu-id="6706b-160">Otherwise, there will be a gap between the segments.</span></span>

<span data-ttu-id="6706b-161">Das [menewpresentation](menewpresentation.md) -Ereignis wird ausgelöst, solange eine Topologie vorhanden ist, die der aktiven Topologie folgt.</span><span class="sxs-lookup"><span data-stu-id="6706b-161">The [MENewPresentation](menewpresentation.md) event is raised as long as there is a topology following the active topology.</span></span> <span data-ttu-id="6706b-162">Folglich wird dieses Ereignis nicht ausgelöst, wenn die Eingabeliste nur eine Topologie enthält oder wenn es sich bei der aktiven Topologie um das letzte in der Eingabeliste handelt.</span><span class="sxs-lookup"><span data-stu-id="6706b-162">Consequently, if the input list contains only one topology, or if the active topology is the last one in the input list, this event is not raised.</span></span>

<span data-ttu-id="6706b-163">Die vorab Liste ist mit der Eingabeliste synchronisiert und wird jedes Mal aktualisiert, wenn der Eingabeliste eine Topologie hinzugefügt oder aus ihr gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6706b-163">The preroll list is synchronized with the input list and is refreshed each time a topology is added to or deleted from the input list.</span></span>

## <a name="deleting-topologies"></a><span data-ttu-id="6706b-164">Löschen von Topologien</span><span class="sxs-lookup"><span data-stu-id="6706b-164">Deleting Topologies</span></span>

<span data-ttu-id="6706b-165">Um eine Topologie aus der Sequencer-Quelle zu entfernen, muss eine Anwendung die [**imfsequencersource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) -Methode abrufen und den Segment Bezeichner angeben.</span><span class="sxs-lookup"><span data-stu-id="6706b-165">To remove a topology from the sequencer source, an application must call the [**IMFSequencerSource::DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) method and specify the segment identifier.</span></span>

<span data-ttu-id="6706b-166">Bevor [**deletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology)aufgerufen wird, muss die Anwendung sicherstellen, dass die Medien Sitzung nicht die Topologie verwendet, die von der Anwendung gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="6706b-166">Before calling [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), the application must make sure that Media Session is not using the topology that the application wants to delete.</span></span> <span data-ttu-id="6706b-167">Zu diesem Zweck müssen die beiden folgenden Punkte auftreten, bevor die Anwendung **deletetopology** aufruft:</span><span class="sxs-lookup"><span data-stu-id="6706b-167">To do this, both of the following must occur before the application calls **DeleteTopology**:</span></span>

-   <span data-ttu-id="6706b-168">Das [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis mit der "MF \_ topostatus" \_ wurde für die Topologie empfangen, um sicherzustellen, dass die Wiedergabe der Medien Sitzung abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="6706b-168">[MESessionTopologyStatus](mesessiontopologystatus.md) event with MF\_TOPOSTATUS\_ENDED is received for the topology to ensure that Media Session has completed playback.</span></span>

-   <span data-ttu-id="6706b-169">[Mesessiontopologystatus](mesessiontopologystatus.md) mit \_ der von MF topostatus \_ gestartete \_ Quelle wird für die nächste Topologie empfangen, um sicherzustellen, dass die Medien Sitzung mit der nächsten Topologie begonnen hat. das [mesessionend](mesessionended.md) -Ereignis wird empfangen, um sicherzustellen, dass die Medien Sitzung mit der letzten Topologie in der Sequencer-Quelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6706b-169">[MESessionTopologyStatus](mesessiontopologystatus.md) with MF\_TOPOSTATUS\_STARTED\_SOURCE is received for the next topology to ensure that the Media Session has started playing the next topology, [MESessionEnded](mesessionended.md) event is received to ensure that Media Session is done with the last topology in the sequencer source.</span></span>

<span data-ttu-id="6706b-170">Wenn das Segment, das gelöscht wird, die aktive Topologie ist, wird die Wiedergabe angehalten, und die Sequencer-Quelle löst das [meendof presentationsegment](meendofpresentationsegment.md) -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="6706b-170">If the segment being deleted is the active topology, playback is stopped and the sequencer source raises the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span> <span data-ttu-id="6706b-171">Wenn die aktive Topologie auch die letzte Topologie ist, wird das [meendof Presentation](meendofpresentation.md) -Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6706b-171">If the active topology is also the last topology, the [MEEndOfPresentation](meendofpresentation.md) event is raised.</span></span>

## <a name="skipping-to-a-segment"></a><span data-ttu-id="6706b-172">Überspringen zu einem Segment</span><span class="sxs-lookup"><span data-stu-id="6706b-172">Skipping to a Segment</span></span>

<span data-ttu-id="6706b-173">Eine Anwendung kann mit einem bestimmten Segment in der Sequenz übersprungen werden, indem die [Medien Sitzung](media-session.md) mit einem Segment Offset wie folgt gestartet wird:</span><span class="sxs-lookup"><span data-stu-id="6706b-173">An application can skip to a particular segment in the sequence by starting the [Media Session](media-session.md) with a segment offset, as follows:</span></span>

1.  <span data-ttu-id="6706b-174">Rufen Sie die [**mfkreatesequencersegmentoffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) -Funktion auf, um den Segment Offset zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6706b-174">Call the [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) function to create the segment offset.</span></span> <span data-ttu-id="6706b-175">Geben Sie den Bezeichner des Segments im *dwID* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="6706b-175">Specify the identifier of the segment in the *dwId* parameter.</span></span> <span data-ttu-id="6706b-176">(Der Bezeichner wurde von der [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) -Methode zurückgegeben, als Sie die Topologie zum ersten Mal der Sequencer-Quelle hinzugefügt haben.) Der *hnsoffset* -Parameter gibt einen Zeit Offset relativ zum Anfang des Segments an.</span><span class="sxs-lookup"><span data-stu-id="6706b-176">(The identifier was returned by the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method when you first added the topology to the sequencer source.) The *hnsOffset* parameter specifies a time offset, relative to the start of the segment.</span></span> <span data-ttu-id="6706b-177">Die Wiedergabe wird zu diesem Zeitpunkt gestartet.</span><span class="sxs-lookup"><span data-stu-id="6706b-177">Playback will start at this time.</span></span> <span data-ttu-id="6706b-178">Übergeben Sie für den *pvarsegmentoffset* -Parameter die Adresse eines leeren **PROPVARIANT**-Parameters.</span><span class="sxs-lookup"><span data-stu-id="6706b-178">For the *pvarSegmentOffset* parameter, pass in the address of an empty **PROPVARIANT**.</span></span> <span data-ttu-id="6706b-179">Wenn die Funktion zurückgegeben wird, enthält diese **PROPVARIANT** den Segment Offset.</span><span class="sxs-lookup"><span data-stu-id="6706b-179">When the function returns, this **PROPVARIANT** contains the segment offset.</span></span>

2.  <span data-ttu-id="6706b-180">Nennen Sie die [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode für die Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6706b-180">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method on the Media Session.</span></span> <span data-ttu-id="6706b-181">Verwenden Sie für den *pguidtimeformat* -Parameter den GUID-Wert MF- \_ Zeit \_ Format \_ Segment \_ Offset.</span><span class="sxs-lookup"><span data-stu-id="6706b-181">For the *pguidTimeFormat* parameter, use the GUID value MF\_TIME\_FORMAT\_SEGMENT\_OFFSET.</span></span> <span data-ttu-id="6706b-182">Dieser Wert gibt die Suche nach Segment Offset an.</span><span class="sxs-lookup"><span data-stu-id="6706b-182">This value indicates seeking by segment offset.</span></span> <span data-ttu-id="6706b-183">Übergeben Sie für den *pvarstartposition* -Parameter die Adresse der im vorherigen Schritt erstellten **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="6706b-183">For the *pvarStartPosition* parameter, pass the address of the **PROPVARIANT** created in the previous step.</span></span>

<span data-ttu-id="6706b-184">Im folgenden Codebeispiel wird veranschaulicht, wie mit dem Anfang eines angegebenen Segments in einer Sequenz übersprungen wird.</span><span class="sxs-lookup"><span data-stu-id="6706b-184">The following code example shows how to skip to the start of a specified segment in a sequence.</span></span>


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="6706b-185">Wenn die Anwendung über Segmente hinweg sucht, empfängt die Anwendung mehrere Ereignisse, da die Sequencer-Quelle das aktuelle Segment beendet und die Wiedergabe des neuen Segments vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="6706b-185">When the application seeks across segments, the application receives several events as the sequencer source ends the current segment and prepares to play the new segment.</span></span> <span data-ttu-id="6706b-186">Da diese Ereignisse asynchron empfangen werden, ist es schwierig, die genaue Reihenfolge der Ereignisse vorherzusagen.</span><span class="sxs-lookup"><span data-stu-id="6706b-186">Because these events are received asynchronously, it is difficult to predict the exact sequence of events.</span></span> <span data-ttu-id="6706b-187">Diese Ereignisse lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6706b-187">These events are as follows:</span></span>

-   <span data-ttu-id="6706b-188">Die Sequencer-Quelle sendet ein [menewpresentation](menewpresentation.md) -Ereignis für das neue Segment, an das die Medien Sitzung übersprungen wird.</span><span class="sxs-lookup"><span data-stu-id="6706b-188">The sequencer source sends an [MENewPresentation](menewpresentation.md) event for the new segment to which the Media Session is skipping.</span></span>

-   <span data-ttu-id="6706b-189">Wenn die Sequencer-Quelle das aktive Segment beendet, sendet Sie das [meendofpresentationsegment](meendofpresentationsegment.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6706b-189">When the sequencer source ends the active segment, it sends the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span>
-   <span data-ttu-id="6706b-190">Die Sequencer-Quelle bricht dann die ein Vorlauf ausgeführt-Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="6706b-190">The sequencer source then cancels the preroll topology.</span></span> <span data-ttu-id="6706b-191">Dies führt zu den folgenden Ereignissen für die abgebrochene Topologie:</span><span class="sxs-lookup"><span data-stu-id="6706b-191">This results in the following events for the canceled topology:</span></span>

    -   <span data-ttu-id="6706b-192">[Mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis mit dem MF- \_ Flag "topostatus \_ Ready".</span><span class="sxs-lookup"><span data-stu-id="6706b-192">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span>
    -   <span data-ttu-id="6706b-193">Das [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis mit dem \_ \_ quellflag "MF topostatus Started" \_ .</span><span class="sxs-lookup"><span data-stu-id="6706b-193">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_STARTED\_SOURCE flag.</span></span>
    -   <span data-ttu-id="6706b-194">Das [meendofpresentationsegment](meendofpresentationsegment.md) -Ereignis mit der [MF- \_ Ereignis \_ Quell Topologie hat das Attribut \_ \_ abgebrochen](mf-event-source-topology-canceled-attribute.md) , um anzugeben, dass die Topologie von der Sequencer-Quelle abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="6706b-194">[MEEndOfPresentationSegment](meendofpresentationsegment.md) event with the [MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED](mf-event-source-topology-canceled-attribute.md) attribute to indicate that the topology was canceled by the sequencer source.</span></span>

-   <span data-ttu-id="6706b-195">Als nächstes sendet die Sequencer-Quelle Ereignisse für das neue Segment, einschließlich verschiedener [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6706b-195">Next, the sequencer source sends events for the new segment, including various [MESessionTopologyStatus](mesessiontopologystatus.md) events.</span></span>
-   <span data-ttu-id="6706b-196">Wenn das neue Segment nicht das letzte in der Liste ist, aktualisiert die Sequencer-Quelle die vorab Liste und löst eine weitere [menewpresentation](menewpresentation.md) für die neue ein Vorlauf ausgeführt-Topologie aus.</span><span class="sxs-lookup"><span data-stu-id="6706b-196">If the new segment is not the last on the list, the sequencer source refreshes the preroll list and raises another [MENewPresentation](menewpresentation.md) for the new preroll topology.</span></span> <span data-ttu-id="6706b-197">Weitere Informationen zu Topologien in der ein Vorlauf ausgeführt-Liste finden Sie unter Informationen zur [Sequencer-Quelle](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="6706b-197">For information about topologies in the preroll list, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="6706b-198">Weitere Informationen zu den von der Sequencer-Quelle gesendeten Ereignissen finden Sie im Thema [Sequencer-Quell Ereignisse](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="6706b-198">More details about the events sent by the sequencer source can be found in the topic [Sequencer Source Events](sequencer-source-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6706b-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6706b-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6706b-200">Erstellen einer Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="6706b-200">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="6706b-201">Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="6706b-201">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



