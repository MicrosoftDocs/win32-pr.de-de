---
description: In diesem Thema wird beschrieben, wie die Sequenz Quelle verwendet wird, um eine Sequenz von Dateien wiederzugeben.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Erstellen einer Wiedergabeliste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527689"
---
# <a name="how-to-create-a-playlist"></a><span data-ttu-id="8b35e-103">Erstellen einer Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="8b35e-103">How to Create a Playlist</span></span>

<span data-ttu-id="8b35e-104">In diesem Thema wird beschrieben, wie die Sequenz Quelle verwendet wird, um eine Sequenz von Dateien wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="8b35e-104">This topic describes how to use the Sequence Source to play a sequence of files.</span></span>

## <a name="overview"></a><span data-ttu-id="8b35e-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8b35e-105">Overview</span></span>

<span data-ttu-id="8b35e-106">Zum Wiedergeben von Mediendateien in einer Sequenz muss die Anwendung Topologien in einer Sequenz hinzufügen, um eine Wiedergabeliste zu erstellen, und diese Topologien in der Medien Sitzung zur Wiedergabe in eine Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-106">To play media files in a sequence, the application must add topologies in a sequence to create a playlist, and queue these topologies on the Media Session for playback.</span></span>

<span data-ttu-id="8b35e-107">Die Sequencer-Quelle sorgt für eine nahtlose Wiedergabe durch initialisieren und Laden der nächsten Topologie, bevor die Medien Sitzung mit der Wiedergabe der aktuellen Topologie beginnt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-107">The sequencer source ensures seamless playback by initializing and loading the next topology before the Media Session starts playing the current topology.</span></span> <span data-ttu-id="8b35e-108">Dadurch kann die Anwendung die nächste Topologie schnell starten, wenn Sie benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="8b35e-108">This enables the application to start the next topology quickly whenever it is required.</span></span>

<span data-ttu-id="8b35e-109">Die Medien Sitzung ist für das Füttern von Daten in die senken und das Abspielen der Topologien in der Sequenz Quelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="8b35e-109">The Media Session is responsible for feeding data to the sinks and playing the topologies in the sequence source.</span></span> <span data-ttu-id="8b35e-110">Außerdem verwaltet die Medien Sitzung die Präsentationszeit für die Segmente.</span><span class="sxs-lookup"><span data-stu-id="8b35e-110">In addition, the Media Session manages the presentation time for the segments.</span></span>

<span data-ttu-id="8b35e-111">Weitere Informationen zum Verwalten von Topologien durch die Sequencer-Quelle finden Sie unter [Informationen zur Sequencer-Quelle](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="8b35e-111">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="8b35e-112">Diese exemplarische Vorgehensweise enthält die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="8b35e-112">This walk-through contains the following steps:</span></span>

1.  [<span data-ttu-id="8b35e-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8b35e-113">Prerequisites</span></span>](#prerequisites)
2.  [<span data-ttu-id="8b35e-114">Media Foundation wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="8b35e-114">Initializing Media Foundation</span></span>](#initializing-media-foundation)
3.  [<span data-ttu-id="8b35e-115">Erstellen von Media Foundation Objekten</span><span class="sxs-lookup"><span data-stu-id="8b35e-115">Creating Media Foundation Objects</span></span>](#creating-media-foundation-objects)
4.  [<span data-ttu-id="8b35e-116">Erstellen der Medienquelle</span><span class="sxs-lookup"><span data-stu-id="8b35e-116">Creating the Media Source</span></span>](#creating-the-media-source)
5.  [<span data-ttu-id="8b35e-117">Erstellen von partiellen Topologien</span><span class="sxs-lookup"><span data-stu-id="8b35e-117">Creating Partial Topologies</span></span>](#creating-partial-topologies)
6.  [<span data-ttu-id="8b35e-118">Hinzufügen von Topologien zur Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="8b35e-118">Adding Topologies to the Sequencer Source</span></span>](#adding-topologies-to-the-sequencer-source)
7.  [<span data-ttu-id="8b35e-119">Festlegen der ersten Topologie in der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="8b35e-119">Setting the First Topology on the Media Session</span></span>](#setting-the-first-topology-on-the-media-session)
8.  [<span data-ttu-id="8b35e-120">Nächste Topologie in der Medien Sitzung in die Warteschlange eingereiht</span><span class="sxs-lookup"><span data-stu-id="8b35e-120">Queuing the Next Topology on the Media Session</span></span>](#queuing-the-next-topology-on-the-media-session)
9.  [<span data-ttu-id="8b35e-121">Freigeben der Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="8b35e-121">Releasing the Sequencer Source</span></span>](#releasing-the-sequencer-source)

<span data-ttu-id="8b35e-122">Die in diesem Thema gezeigten Codebeispiele sind Ausschnitte aus dem Thema [Sequencer-Quell Codebeispiel Code](sequencer-source-example-code.md), der den gesamten Beispielcode enthält.</span><span class="sxs-lookup"><span data-stu-id="8b35e-122">The code examples shown this topic are excerpts from the topic [Sequencer Source Example Code](sequencer-source-example-code.md), which contains the complete example code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8b35e-123">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8b35e-123">Prerequisites</span></span>

<span data-ttu-id="8b35e-124">Bevor Sie mit dieser exemplarischen Vorgehensweise beginnen, machen Sie sich mit den folgenden Media Foundation Konzepten vertraut:</span><span class="sxs-lookup"><span data-stu-id="8b35e-124">Before starting this walk-through, familiarize yourself with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="8b35e-125">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="8b35e-125">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="8b35e-126">Topologien</span><span class="sxs-lookup"><span data-stu-id="8b35e-126">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="8b35e-127">Medienereignis Generatoren</span><span class="sxs-lookup"><span data-stu-id="8b35e-127">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="8b35e-128">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="8b35e-128">Presentation Descriptors</span></span>](presentation-descriptors.md)

<span data-ttu-id="8b35e-129">Lesen Sie außerdem die Informationen zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md), da der Code in diesem Thema den Code in diesem Thema erweitert.</span><span class="sxs-lookup"><span data-stu-id="8b35e-129">Also read [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), because the example code shwon here expands on the code in that topic.</span></span>

## <a name="initializing-media-foundation"></a><span data-ttu-id="8b35e-130">Media Foundation wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="8b35e-130">Initializing Media Foundation</span></span>

<span data-ttu-id="8b35e-131">Bevor Sie beliebige Media Foundation Schnittstellen oder Methoden verwenden können, initialisieren Sie Media Foundation, indem Sie die [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-131">Before you can use any Media Foundation interfaces or methods, initialize Media Foundation by calling the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="8b35e-132">Weitere Informationen finden Sie unter [Initialisieren von Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="8b35e-132">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a><span data-ttu-id="8b35e-133">Erstellen von Media Foundation Objekten</span><span class="sxs-lookup"><span data-stu-id="8b35e-133">Creating Media Foundation Objects</span></span>

<span data-ttu-id="8b35e-134">Erstellen Sie als nächstes die folgenden Media Foundation Objekte:</span><span class="sxs-lookup"><span data-stu-id="8b35e-134">Next, create the following Media Foundation objects:</span></span>

-   <span data-ttu-id="8b35e-135">Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8b35e-135">Media session.</span></span> <span data-ttu-id="8b35e-136">Dieses Objekt macht die [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstelle verfügbar, die Methoden zum Abspielen, anhalten und stoppen der aktuellen Topologie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-136">This object exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface, which provides methods to play, pause, and stop the current topology.</span></span>
-   <span data-ttu-id="8b35e-137">Sequencer-Quelle.</span><span class="sxs-lookup"><span data-stu-id="8b35e-137">Sequencer source.</span></span> <span data-ttu-id="8b35e-138">Dieses Objekt macht die [**imfsequencersource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) -Schnittstelle verfügbar, die Methoden zum Hinzufügen, aktualisieren und Löschen von Topologien in einer Sequenz bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-138">This object exposes the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface, which provides methods to add, update, and delete topologies in a sequence.</span></span>

1.  <span data-ttu-id="8b35e-139">Rufen Sie die [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) -Funktion auf, um die Medien Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-139">Call the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function to create the Media Session.</span></span>
2.  <span data-ttu-id="8b35e-140">Aufrufen von [**imfmediaeventqueue:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) , um das erste Ereignis aus der Medien Sitzung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="8b35e-140">Call [**IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) to request the first event from the Media Session.</span></span>
3.  <span data-ttu-id="8b35e-141">Rufen Sie die [**mfkreatesequencersource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) -Funktion auf, um die Sequencer-Quelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-141">Call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function to create the sequencer source.</span></span>

<span data-ttu-id="8b35e-142">Mit dem folgenden Code wird die Medien Sitzung erstellt und das erste Ereignis angefordert:</span><span class="sxs-lookup"><span data-stu-id="8b35e-142">The following code creates the Media Session and requests the first event:</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a><span data-ttu-id="8b35e-143">Erstellen der Medienquelle</span><span class="sxs-lookup"><span data-stu-id="8b35e-143">Creating the Media Source</span></span>

<span data-ttu-id="8b35e-144">Erstellen Sie als nächstes eine Medienquelle für das erste Wiedergabelisten Segment.</span><span class="sxs-lookup"><span data-stu-id="8b35e-144">Next, create a media source for the first playlist segment.</span></span> <span data-ttu-id="8b35e-145">Verwenden Sie den [quellresolver](source-resolver.md) , um eine Medienquelle aus einer URL zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-145">Use the [Source Resolver](source-resolver.md) to create a media source from a URL.</span></span> <span data-ttu-id="8b35e-146">Rufen Sie hierzu die [**mffroatesourceresolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) -Funktion auf, um einen quellresolver zu erstellen, und rufen Sie dann die [**imfsourceresolver::**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) -Methode auf, um die Medienquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-146">To do this, call the [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) function to create a source resolver and then call the [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method to create the media source.</span></span>

<span data-ttu-id="8b35e-147">Weitere Informationen zu Medienquellen finden Sie unter [Medienquellen](media-sources.md).</span><span class="sxs-lookup"><span data-stu-id="8b35e-147">For information about media sources, see [Media Sources](media-sources.md).</span></span>

## <a name="creating-partial-topologies"></a><span data-ttu-id="8b35e-148">Erstellen von partiellen Topologien</span><span class="sxs-lookup"><span data-stu-id="8b35e-148">Creating Partial Topologies</span></span>

<span data-ttu-id="8b35e-149">Jedes Segment in der Sequencer-Quelle verfügt über eine eigene partielle Topologie.</span><span class="sxs-lookup"><span data-stu-id="8b35e-149">Each segment in the sequencer source has its own partial topology.</span></span> <span data-ttu-id="8b35e-150">Erstellen Sie als nächstes partielle Topologien für Medienquellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-150">Next, create partial topologies for media sources.</span></span> <span data-ttu-id="8b35e-151">Bei einer partiellen Topologie sind die Quellknoten der Topologie direkt mit den Ausgabe Knoten verbunden, ohne dass zwischen Transformationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b35e-151">For a partial topology, the topology source nodes are connected directly to the output nodes, without specifying any intermediate transforms.</span></span> <span data-ttu-id="8b35e-152">Die Medien Sitzung verwendet das topologielademobjekt zum Auflösen der Topologie.</span><span class="sxs-lookup"><span data-stu-id="8b35e-152">The Media Session uses the topology loader object to resolve the topology.</span></span> <span data-ttu-id="8b35e-153">Nachdem eine Topologie aufgelöst wurde, werden die erforderlichen Decoder und andere Transformations Knoten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-153">After a topology is resolved, the required decoders and other transform nodes are added.</span></span> <span data-ttu-id="8b35e-154">Die Sequencer-Quelle kann auch vollständige Topologien enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b35e-154">The sequencer source can also contain full topologies.</span></span>

<span data-ttu-id="8b35e-155">Verwenden Sie zum Erstellen des topologieobjekts die [**mfkreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) -Funktion, und verwenden Sie dann die [**imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) -Schnittstelle zum Erstellen von streamknoten.</span><span class="sxs-lookup"><span data-stu-id="8b35e-155">To create the topology object, use the [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) function and then use the [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface to create stream nodes.</span></span>

<span data-ttu-id="8b35e-156">Umfassende Anweisungen zur Verwendung dieser Programmier Elemente zum Erstellen von Topologien finden Sie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="8b35e-156">For complete instructions on using these programming elements to create topologies, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="8b35e-157">Eine Anwendung kann einen ausgewählten Teil der systemeigenen Quelle wiedergeben, indem der Quellknoten konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="8b35e-157">An application can play a selected portion of the native source by configuring the source node.</span></span> <span data-ttu-id="8b35e-158">Legen Sie zu diesem Zweck das [**MF- \_ toponode \_ mediastart**](mf-toponode-mediastart-attribute.md) -Attribut und das [**MF- \_ toponode \_ mediastop**](mf-toponode-mediastop-attribute.md) -Attribut auf den Knoten der Knoten Topologie der **MF- \_ Topologie \_ \_** fest.</span><span class="sxs-lookup"><span data-stu-id="8b35e-158">To do this, set the [**MF\_TOPONODE\_MEDIASTART**](mf-toponode-mediastart-attribute.md) attribute and the [**MF\_TOPONODE\_MEDIASTOP**](mf-toponode-mediastop-attribute.md) attribute on **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** topology nodes.</span></span> <span data-ttu-id="8b35e-159">Geben Sie die Start Zeit des Mediums und die Endzeit des Mediums in Bezug auf den Start der systemeigenen Quelle als **UINT64** -Typen an.</span><span class="sxs-lookup"><span data-stu-id="8b35e-159">Specify the media start time and the media stop time relative to the start of the native source as **UINT64** types.</span></span>

## <a name="adding-topologies-to-the-sequencer-source"></a><span data-ttu-id="8b35e-160">Hinzufügen von Topologien zur Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="8b35e-160">Adding Topologies to the Sequencer Source</span></span>

<span data-ttu-id="8b35e-161">Fügen Sie als nächstes die partiellen Topologien, die Sie erstellt haben, der Sequencer-Quelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="8b35e-161">Next, add to the sequencer source the partial topologies that you created.</span></span> <span data-ttu-id="8b35e-162">Jedem Sequence-Element, das als *Segment* bezeichnet wird, wird ein **mfsequencerelementid-** Bezeichner zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-162">Each sequence element, called a *segment*, is assigned an **MFSequencerElementId** identifier.</span></span> <span data-ttu-id="8b35e-163">Weitere Informationen zum Verwalten von Topologien durch die Sequencer-Quelle finden Sie unter [Informationen zur Sequencer-Quelle](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="8b35e-163">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="8b35e-164">Nachdem alle Topologien der Sequencer-Quelle hinzugefügt wurden, muss die Anwendung das letzte Segment in der Sequenz markieren, um die Wiedergabe in der Pipeline beenden zu können.</span><span class="sxs-lookup"><span data-stu-id="8b35e-164">After all of the topologies are added to the sequencer source, the application must flag the last segment in the sequence to end playback in the pipeline.</span></span> <span data-ttu-id="8b35e-165">Ohne dieses Flag erwartet die Sequencer-Quelle, dass weitere Topologien hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8b35e-165">Without this flag, the sequencer source expects more topologies to be added.</span></span>

1.  <span data-ttu-id="8b35e-166">Wenden Sie die [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) -Methode an, um der Sequencer-Quelle eine bestimmte Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-166">Call the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method to add a specific topology to the sequencer source.</span></span>

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    <span data-ttu-id="8b35e-167">[**Appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) fügt der Sequenz die angegebene Topologie hinzu.</span><span class="sxs-lookup"><span data-stu-id="8b35e-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adds the specified topology to the sequence.</span></span> <span data-ttu-id="8b35e-168">Diese Methode gibt den Segment Bezeichner im *pdwid-* Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="8b35e-168">This method returns the segment identifier in the *pdwId* parameter.</span></span>

    <span data-ttu-id="8b35e-169">Wenn die Topologie die letzte in der Sequencer-Quelle ist, übergeben Sie sequencertopologyflags \_ zuletzt im *dwFlags* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="8b35e-169">If the topology is the last one in the sequencer source, pass SequencerTopologyFlags\_Last in the *dwFlags* parameter.</span></span> <span data-ttu-id="8b35e-170">Dieser Wert wird in der [**MF sequencertopologyflags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="8b35e-170">This value is defined in the [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) enumeration.</span></span>

2.  <span data-ttu-id="8b35e-171">Aufrufen von [**imfsequencersource:: updatetopologyflags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) zum Aktualisieren der Flags für die Topologie, die dem Segment Bezeichner in der Eingabeliste zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8b35e-171">Call [**IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) to update the flags for the topology associated with the segment identifier in the input list.</span></span> <span data-ttu-id="8b35e-172">In diesem Fall gibt der-Befehl an, dass es sich bei dem angegebenen Segment um das letzte Segment im Sequencer handelt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-172">In this case, the call indicates that the specified segment is the last segment in the sequencer.</span></span> <span data-ttu-id="8b35e-173">(Dieser-Befehl ist optional, wenn die letzte Topologie im [**appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) -Befehl angegeben wird.)</span><span class="sxs-lookup"><span data-stu-id="8b35e-173">(This call is optional if the last topology is specified in the [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) call.)</span></span>

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

<span data-ttu-id="8b35e-174">Die Anwendung kann die Topologie eines Segments durch eine andere Topologie ersetzen, indem Sie die [**imfsequencersource:: updatetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) aufrufen und die neue Topologie in *ptopology* übergibt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-174">The application can replace a segment's topology with another topology by calling the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) and passing the new topology in *pTopology*.</span></span> <span data-ttu-id="8b35e-175">Wenn neue Native Quellen in der neuen Topologie vorhanden sind, werden die Quellen dem Quell Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-175">If there are new native sources in the new topology, the sources are added to the source cache.</span></span> <span data-ttu-id="8b35e-176">Die vorab Liste wird ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8b35e-176">The preroll list is also refreshed.</span></span>

## <a name="setting-the-first-topology-on-the-media-session"></a><span data-ttu-id="8b35e-177">Festlegen der ersten Topologie in der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="8b35e-177">Setting the First Topology on the Media Session</span></span>

<span data-ttu-id="8b35e-178">Als Nächstes stellen Sie die erste Topologie in der Sequenz Quelle in der Medien Sitzung in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="8b35e-178">Next, queue the first topology in the sequence source on the Media Session.</span></span> <span data-ttu-id="8b35e-179">Wenn Sie die erste Topologie aus der Sequencer-Quelle abrufen möchten, muss die Anwendung die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-179">To get the first topology from the sequencer source, the application must call the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="8b35e-180">Diese Methode gibt die partielle Topologie zurück, die von der Medien Sitzung aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8b35e-180">This method returns the partial topology, which is resolved by the Media Session.</span></span>

<span data-ttu-id="8b35e-181">Weitere Informationen zu partiellen Topologien finden Sie unter Informationen [zu Topologien](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="8b35e-181">For information about partial topologies, see [About Topologies](about-topologies.md).</span></span>

1.  <span data-ttu-id="8b35e-182">Rufen Sie die native Medienquelle für die erste Topologie der Sequenz Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="8b35e-182">Retrieve the native media source for the first topology of the sequence source.</span></span>
2.  <span data-ttu-id="8b35e-183">Erstellen Sie einen Präsentations Deskriptor für die Medienquelle, indem Sie die [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-183">Create a presentation descriptor for the media source by calling the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>
3.  <span data-ttu-id="8b35e-184">Rufen Sie die zugehörige Topologie für die Präsentation ab, indem Sie die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-184">Retrieve the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
4.  <span data-ttu-id="8b35e-185">Legen Sie die erste Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)fest.</span><span class="sxs-lookup"><span data-stu-id="8b35e-185">Set the first topology on the Media Session by Calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

    <span data-ttu-id="8b35e-186">Aufrufen der [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , bei der der *dwsettopologyflags* -Parameter auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8b35e-186">Call [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the *dwSetTopologyFlags* parameter set to **NULL**.</span></span> <span data-ttu-id="8b35e-187">Dies weist die Medien Sitzung an, die angegebene Topologie zu starten, wenn die aktuelle Topologie abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8b35e-187">This instructs the Media Session to start the specified topology when the current topology has been completed.</span></span> <span data-ttu-id="8b35e-188">Da in diesem Fall die angegebene Topologie die erste Topologie ist und keine aktuelle Präsentation vorhanden ist, startet die Medien Sitzung die neue Präsentation sofort.</span><span class="sxs-lookup"><span data-stu-id="8b35e-188">Because in this case, the specified topology is the first topology and there is no current presentation, the Media Session starts the new presentation immediately.</span></span>

    <span data-ttu-id="8b35e-189">Der **null** -Wert gibt auch an, dass die Medien Sitzung die Topologie auflösen muss, da die vom topologieanbieter zurückgegebene Topologie immer eine partielle Topologie ist.</span><span class="sxs-lookup"><span data-stu-id="8b35e-189">The **NULL** value also indicates that Media Session must resolve the topology because the topology returned by the topology provider is always a partial topology.</span></span>


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



## <a name="queuing-the-next-topology-on-the-media-session"></a><span data-ttu-id="8b35e-190">Nächste Topologie in der Medien Sitzung in die Warteschlange eingereiht</span><span class="sxs-lookup"><span data-stu-id="8b35e-190">Queuing the Next Topology on the Media Session</span></span>

<span data-ttu-id="8b35e-191">Als nächstes muss die Anwendung das [menewpresentation](menewpresentation.md) -Ereignis behandeln.</span><span class="sxs-lookup"><span data-stu-id="8b35e-191">Next, the application needs to handle the [MENewPresentation](menewpresentation.md) event.</span></span>

<span data-ttu-id="8b35e-192">Die Sequencer-Quelle löst [menewpresentation](menewpresentation.md) aus, wenn die Medien Sitzung mit der Wiedergabe eines Segments beginnt, dem ein anderes Segment folgt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-192">Sequencer source raises [MENewPresentation](menewpresentation.md) when the Media Session starts playing a segment that has another segment following it.</span></span> <span data-ttu-id="8b35e-193">Dieses Ereignis informiert die Anwendung über die nächste Topologie in der Sequenz Quelle, indem Sie den Präsentations Deskriptor für das nächste Segment in der vorab Liste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8b35e-193">This event informs the application about the next topology in the sequence source by providing the presentation descriptor for the next segment in the preroll list.</span></span> <span data-ttu-id="8b35e-194">Die Anwendung muss die zugeordnete Topologie mit dem topologieanbieter abrufen und in der Medien Sitzung in eine Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-194">The application must retrieve the associated topology, by using the topology provider, and queue it on the Media Session.</span></span> <span data-ttu-id="8b35e-195">Die Sequencer-Quelle stellt dann eine Vorabversion dieser Topologie dar, wodurch ein nahtloser Übergang zwischen Präsentationen sichergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8b35e-195">The sequencer source then prerolls this topology, which ensures a seamless transition between presentations.</span></span>

<span data-ttu-id="8b35e-196">Wenn die Anwendung über Segmente hinweg sucht, empfängt die Anwendung mehrere [menewpresentation](menewpresentation.md) -Ereignisse, da die Sequencer-Quelle die vorab Liste aktualisiert und die richtige Topologie einrichtet.</span><span class="sxs-lookup"><span data-stu-id="8b35e-196">When the application seeks across segments, the application receives several [MENewPresentation](menewpresentation.md) events as the sequencer source refreshes the preroll list and sets up the correct topology.</span></span> <span data-ttu-id="8b35e-197">Die Anwendung muss jedes Ereignis verarbeiten und die in den Ereignisdaten zurückgegebene Topologie in der Medien Sitzung in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-197">The application must handle each event and queue the topology returned in the event data, on the Media Session.</span></span> <span data-ttu-id="8b35e-198">Weitere Informationen zum Überspringen von Segmenten finden [Sie unter Verwenden der Sequencer-Quelle](using-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="8b35e-198">For information about skipping segments, see [Using the Sequencer Source](using-the-sequencer-source.md).</span></span>

<span data-ttu-id="8b35e-199">Informationen zum erhalten von Sequencer-Quell Benachrichtigungen finden Sie unter [Sequencer](sequencer-source-events.md)-Quell Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8b35e-199">For information about getting sequencer source notifications, see [Sequencer Source Events](sequencer-source-events.md).</span></span>

1.  <span data-ttu-id="8b35e-200">Rufen Sie im [menewpresentation](menewpresentation.md) -Ereignishandler den Präsentations Deskriptor für das nächste Segment aus den Ereignisdaten ab.</span><span class="sxs-lookup"><span data-stu-id="8b35e-200">In the [MENewPresentation](menewpresentation.md) event handler, retrieve the presentation descriptor for the next segment from the event data.</span></span>
2.  <span data-ttu-id="8b35e-201">Rufen Sie die zugehörige Topologie für die Präsentation ab, indem Sie die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-201">Get the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
3.  <span data-ttu-id="8b35e-202">Legen Sie die Topologie für die Medien Sitzung fest, indem Sie die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-202">Set the topology on the Media Session by calling the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>

    <span data-ttu-id="8b35e-203">Die Medien Sitzung startet die neue Präsentation, wenn die aktuelle Präsentation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8b35e-203">The Media Session starts the new presentation when the current presentation has been completed.</span></span>


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a><span data-ttu-id="8b35e-204">Freigeben der Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="8b35e-204">Releasing the Sequencer Source</span></span>

<span data-ttu-id="8b35e-205">Beenden Sie abschließend die Sequencer-Quelle.</span><span class="sxs-lookup"><span data-stu-id="8b35e-205">Finally, shut down the sequencer source.</span></span> <span data-ttu-id="8b35e-206">Dazu können Sie die [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) -Methode für die Sequencer-Quelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b35e-206">To do so, call the [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) method on the sequencer source.</span></span> <span data-ttu-id="8b35e-207">Durch diesen aufzurufenden Befehl werden alle zugrunde liegenden systemeigenen Medienquellen in der Sequencer-Quelle heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="8b35e-207">This call shuts down all of the underlying native media sources in the sequencer source.</span></span>

<span data-ttu-id="8b35e-208">Nachdem die Sequencer-Quelle freigegeben wurde, sollte die Anwendung die Medien Sitzung schließen und beenden, indem [**imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) und [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)in dieser Reihenfolge aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8b35e-208">After releasing the sequencer source, the application should close and shut down the Media Session by calling [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) and [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in that order.</span></span>

<span data-ttu-id="8b35e-209">Um Speicher Verluste zu vermeiden, muss die Anwendung Zeiger auf Media Foundation-Schnittstellen freigeben, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8b35e-209">To avoid memory leaks, the application must release pointers to Media Foundation interfaces when they are no longer needed.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8b35e-210">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8b35e-210">Next Steps</span></span>

<span data-ttu-id="8b35e-211">In dieser exemplarischen Vorgehensweise wird veranschaulicht, wie eine einfache Wiedergabeliste mithilfe der Sequencer-Quelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8b35e-211">This walk-through illustrated how to create a basic playlist by using the sequencer source.</span></span> <span data-ttu-id="8b35e-212">Nachdem Sie die Wiedergabeliste erstellt haben, können Sie erweiterte Funktionen hinzufügen, wie z. b. das Überspringen von Segmenten, das Ändern des Wiedergabe Zustands und das Suchen innerhalb eines Segments.</span><span class="sxs-lookup"><span data-stu-id="8b35e-212">After creating the playlist, you might want to add advanced features such as segment skipping, changing the playback state, and seeking within a segment.</span></span> <span data-ttu-id="8b35e-213">In der folgenden Liste finden Sie Links zu den verwandten Themen:</span><span class="sxs-lookup"><span data-stu-id="8b35e-213">The following list provides links to the related topics:</span></span>

-   <span data-ttu-id="8b35e-214">[Steuern von Präsentations Zuständen](how-to-control-presentation-states.md): die Sequencer-Quelle basiert auf der Medien Sitzung, um die Transportsteuerung wie, wiedergeben, anhalten und stoppen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-214">[How to Control Presentation States](how-to-control-presentation-states.md): The sequencer source relies on the Media Session to provide transport control such as, Play, Pause, and Stop.</span></span>
-   <span data-ttu-id="8b35e-215">[In diesem](how-to-perform-scrubbing.md) Thema werden die Schritte beschrieben, die erforderlich sind, um eine bestimmte Position in einem Stream zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8b35e-215">[How to Perform Scrubbing](how-to-perform-scrubbing.md) describes the steps required to seek to a specific position in a stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b35e-216">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b35e-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b35e-217">Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="8b35e-217">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



