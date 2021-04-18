---
description: Dieses Thema enthält Beispielcode für die Verwendung der Sequencer-Quelle in Microsoft Media Foundation.
ms.assetid: 6f39a297-33a9-414a-9d41-47aec54eaa6b
title: Beispiel Code für die Sequencer-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a587a9b77413ad22ac49111489cf3e1b89cadf8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215009"
---
# <a name="sequencer-source-example-code"></a><span data-ttu-id="e1db5-103">Beispiel Code für die Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="e1db5-103">Sequencer Source Example Code</span></span>

<span data-ttu-id="e1db5-104">Dieses Thema enthält Beispielcode für die Verwendung der [Sequencer-Quelle](sequencer-source.md) in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e1db5-104">This topic shows example code for using the [Sequencer Source](sequencer-source.md) in Microsoft Media Foundation.</span></span> <span data-ttu-id="e1db5-105">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="e1db5-105">It contains the following sections.</span></span>

-   [<span data-ttu-id="e1db5-106">Cwiedergabe-Klasse</span><span class="sxs-lookup"><span data-stu-id="e1db5-106">CPlaylist Class</span></span>](#cplaylist-class)
-   [<span data-ttu-id="e1db5-107">Erstellen einer Instanz von cwiedergabe</span><span class="sxs-lookup"><span data-stu-id="e1db5-107">Creating an Instance of CPlaylist</span></span>](#creating-an-instance-of-cplaylist)
-   [<span data-ttu-id="e1db5-108">Hinzufügen und Entfernen von Wiedergabelisten Segmenten</span><span class="sxs-lookup"><span data-stu-id="e1db5-108">Adding and Removing Playlist Segments</span></span>](#adding-and-removing-playlist-segments)
-   [<span data-ttu-id="e1db5-109">Behandeln von Sitzungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="e1db5-109">Handling Session Events</span></span>](#handling-session-events)
-   [<span data-ttu-id="e1db5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1db5-110">Related topics</span></span>](#related-topics)

## <a name="cplaylist-class"></a><span data-ttu-id="e1db5-111">Cwiedergabe-Klasse</span><span class="sxs-lookup"><span data-stu-id="e1db5-111">CPlaylist Class</span></span>

<span data-ttu-id="e1db5-112">Die- `CPlaylist` Klasse wird von der- `CPlayer` Klasse abgeleitet, die im Tutorial Gewusst wie: Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e1db5-112">The `CPlaylist` class derives from the `CPlayer` class that is shown in the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>


```C++
const DWORD MAX_PLAYLIST_SEGMENTS = 128;

// For this example, there is a hard-coded limit to the number of playlist 
// segments, to avoid using a dynamically sized list.

class CPlaylist : public CPlayer
{
private:
    IMFSequencerSource     *m_pSequencerSource;
    IMFPresentationClock   *m_pPresentationClock;     

    MFTIME      m_PresentationTimeOffset;
    DWORD       m_ActiveSegment;
    LONGLONG    m_hnsSegmentDuration;

    // Table of segment IDs and topology IDs.
    struct 
    {
        MFSequencerElementId    SegmentID;
        TOPOID                    TopoID;
    } m_segments[MAX_PLAYLIST_SEGMENTS];

    DWORD m_count;

private:

    MFSequencerElementId LastSegment() const
    {
        return m_segments[ m_count - 1].SegmentID;
    }

    HRESULT LookupTopoID(TOPOID id, DWORD *pIndex);
    HRESULT OnSessionEvent(IMFMediaEvent *pEvent, MediaEventType meType);
    HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    HRESULT OnNewPresentation(IMFMediaEvent *pEvent);
    HRESULT AddSegment(PCWSTR pszURL);
    HRESULT QueueNextSegment(IMFPresentationDescriptor *pPD);

    CPlaylist(HWND hWnd, HRESULT *phr);
    ~CPlaylist();

    HRESULT Initialize();
    
public:

    static HRESULT CreateInstance(HWND hwnd, CPlaylist **ppPlayer);

    HRESULT AddToPlaylist(PCWSTR pszURL); 
    HRESULT DeleteSegment(DWORD index);
    HRESULT SkipTo(DWORD index);

    DWORD   NumSegments() { return m_count; }
    DWORD   ActiveSegment() const { return m_ActiveSegment; }

    HRESULT GetPlaybackTime(MFTIME *phnsPresentation, MFTIME *phnsSegment);

    LONGLONG SegmentDuration() { return m_hnsSegmentDuration; }
};
```



## <a name="creating-an-instance-of-cplaylist"></a><span data-ttu-id="e1db5-113">Erstellen einer Instanz von cwiedergabe</span><span class="sxs-lookup"><span data-stu-id="e1db5-113">Creating an Instance of CPlaylist</span></span>

<span data-ttu-id="e1db5-114">Die- `CPlaylist::CreateInstance` Methode erstellt ein neues- `CPlaylist` Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1db5-114">The `CPlaylist::CreateInstance` method creates a new `CPlaylist` object.</span></span> <span data-ttu-id="e1db5-115">Intern ruft diese Methode `CPlaylist::Initialize` auf, um das Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="e1db5-115">Internally, this method calls `CPlaylist::Initialize` to initialize the object.</span></span> <span data-ttu-id="e1db5-116">Die- `Initialize` Methode ruft [**mfkreatesequencersource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) auf, um die Sequenz Quelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1db5-116">The `Initialize` method calls [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) to create the sequence source.</span></span> <span data-ttu-id="e1db5-117">Außerdem wird [**imfmediasession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) aufgerufen, um einen Zeiger auf die Präsentations Uhr zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e1db5-117">It also calls [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) to get a pointer to the presentation clock.</span></span>


```C++
/*static*/ 
HRESULT CPlaylist::CreateInstance(HWND hwnd, CPlaylist **ppPlayer)
{
    *ppPlayer = NULL;

    HRESULT hr = S_OK;

    CPlaylist *pPlayer = new (std::nothrow) CPlaylist(hwnd, &hr);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->Initialize();
    }

    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlaylist::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = CPlayer::CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create an instance of the sequencer Source.
    hr = MFCreateSequencerSource(NULL, &m_pSequencerSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&m_pSource));
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Get the presentation clock.
    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }
    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pPresentationClock));

done:
    SafeRelease(&pClock);
    return hr;
}

CPlaylist::CPlaylist(HWND hWnd, HRESULT *phr)
:   CPlayer(NULL, hWnd, phr),
    m_pSequencerSource (NULL),
    m_pPresentationClock (NULL),
    m_PresentationTimeOffset (0),
    m_ActiveSegment((DWORD)-1),
    m_hnsSegmentDuration(0),
    m_count(0)
{
}

CPlaylist::~CPlaylist()
{
    SafeRelease(&m_pSequencerSource);
    SafeRelease(&m_pPresentationClock);
}
```



## <a name="adding-and-removing-playlist-segments"></a><span data-ttu-id="e1db5-118">Hinzufügen und Entfernen von Wiedergabelisten Segmenten</span><span class="sxs-lookup"><span data-stu-id="e1db5-118">Adding and Removing Playlist Segments</span></span>

<span data-ttu-id="e1db5-119">Die- `AddSegment` Methode fügt ein neues Wiedergabelisten Segment hinzu.</span><span class="sxs-lookup"><span data-stu-id="e1db5-119">The `AddSegment` method adds a new playlist segment.</span></span>

<span data-ttu-id="e1db5-120">Diese Methode führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="e1db5-120">This method performs the following steps:</span></span>

1.  <span data-ttu-id="e1db5-121">Erstellt eine Wiedergabe Topologie.</span><span class="sxs-lookup"><span data-stu-id="e1db5-121">Creates a playback topology.</span></span> <span data-ttu-id="e1db5-122">Der Code für diesen Schritt wird im Thema Erstellen von [Wiedergabe Topologien](creating-playback-topologies.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1db5-122">The code for this step is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
2.  <span data-ttu-id="e1db5-123">Ruft [**imfsequencersource:: appendtopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) auf, um der Wiedergabeliste die Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e1db5-123">Calls [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) to add the topology to the playlist.</span></span>
3.  <span data-ttu-id="e1db5-124">Ruft im ersten Segment den Wert des [**MF- \_ \_ laufzeitduration**](mf-pd-duration-attribute.md) -Attributs ab, das die Wiedergabedauer enthält.</span><span class="sxs-lookup"><span data-stu-id="e1db5-124">On the first segment, gets the value of the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute, which contains the playback duration.</span></span>
4.  <span data-ttu-id="e1db5-125">Speichert die Segment-ID und die topologiekennung in einer Nachschlage Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e1db5-125">Stores the segment ID and topology ID in a lookup table.</span></span>


```C++
// Adds a segment to the sequencer.

HRESULT CPlaylist::AddSegment(PCWSTR pszURL)
{
    IMFMediaSource *pMediaSource = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    MFSequencerElementId SegmentId;
    TOPOID TopologyID = 0;
    
    HRESULT hr = CreateMediaSource(pszURL, &pMediaSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMediaSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreatePlaybackTopology(pMediaSource, pPD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSequencerSource->AppendTopology(
        pTopology, 
        SequencerTopologyFlags_Last, 
        &SegmentId
        );

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopology->GetTopologyID(&TopologyID);
    if (FAILED(hr))
    {
        goto done;
    }
        
   
    if (m_count == 0)
    {
        // Get the segment duration
        m_hnsSegmentDuration = MFGetAttributeUINT64(pPD, MF_PD_DURATION, 0);
    }

    m_segments[m_count].SegmentID = SegmentId;
    m_segments[m_count].TopoID = TopologyID;

    m_count++;

done:
    SafeRelease(&pMediaSource);
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return hr;
}
```



<span data-ttu-id="e1db5-126">Die `AddSegment` -Methode ist privat für `CPlaylist` und wird von der folgenden öffentlichen Methode aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="e1db5-126">The `AddSegment` method is private to `CPlaylist`, and is called from the following public method:</span></span>


```C++
// Adds a new segment to the playlist.

HRESULT CPlaylist::AddToPlaylist(PCWSTR pszURL)
{
    if (NumSegments() >= MAX_PLAYLIST_SEGMENTS)
    {
        return MF_E_OUT_OF_RANGE;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor *pPD = NULL;

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

    // Create the topology and add it to the sequencer.
    hr = AddSegment(pszURL);
    if (FAILED(hr))
    {
        goto done;
    }

    // If this is the first segment, queue it on the session.
    if (bFirstSegment)
    {
        hr = m_pSource->CreatePresentationDescriptor(&pPD);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = QueueNextSegment(pPD);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    if (m_state < Started)
    {
        m_state = OpenPending;
    }

done:
    SafeRelease(&pPD);
    return hr;
}
```



<span data-ttu-id="e1db5-127">Wenn Sie das erste Wiedergabelisten Segment erstellen, müssen Sie die Segment Topologie in der Medien Sitzung wie folgt in die Warteschlange stellen:</span><span class="sxs-lookup"><span data-stu-id="e1db5-127">When you create the first playlist segment, you must queue the segment topology on the Media Session, as follows:</span></span>

1.  <span data-ttu-id="e1db5-128">Fragen Sie die Sequencer-Quelle für die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="e1db5-128">Query the sequencer source for the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface.</span></span>
2.  <span data-ttu-id="e1db5-129">Übergeben Sie den Präsentations Deskriptor an die [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e1db5-129">Pass the presentation descriptor to the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="e1db5-130">Diese Methode erhält einen Zeiger auf die Segment Topologie.</span><span class="sxs-lookup"><span data-stu-id="e1db5-130">This method gets a pointer to the segment topology.</span></span> <span data-ttu-id="e1db5-131">Beachten Sie, dass diese Topologie nicht exakt mit der Wiedergabe Topologie identisch ist, die Sie als earliers erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e1db5-131">Note that this topology is not exactly the same as the playback topology that you created earliers.</span></span> <span data-ttu-id="e1db5-132">Stattdessen handelt es sich um eine geänderte Version dieser Topologie.</span><span class="sxs-lookup"><span data-stu-id="e1db5-132">Instead, it is a modified version of that topology.</span></span> <span data-ttu-id="e1db5-133">Weitere Informationen finden Sie unter Informationen zur [Sequencer-Quelle](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="e1db5-133">For more information, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>
3.  <span data-ttu-id="e1db5-134">Stellen Sie die Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e1db5-134">Queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

<span data-ttu-id="e1db5-135">Der folgende Code zeigt diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="e1db5-135">The following code shows these steps.</span></span> <span data-ttu-id="e1db5-136">Derselbe Code wird auch verwendet, wenn die Wiedergabeliste das nächste Segment vorab verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1db5-136">This same code is also used when the playlist prerolls the next segment.</span></span>


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



<span data-ttu-id="e1db5-137">Um ein Wiedergabelisten Segment zu löschen, nennen Sie [**imfsequencersource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology).</span><span class="sxs-lookup"><span data-stu-id="e1db5-137">To delete a playlist segment, call [**IMFSequencerSource::DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology).</span></span> <span data-ttu-id="e1db5-138">Das Segment wird durch die Segment-ID angegeben.</span><span class="sxs-lookup"><span data-stu-id="e1db5-138">The segment is specified by segment ID.</span></span> <span data-ttu-id="e1db5-139">(Aus diesem Grund sollte die Anwendung die Liste der Segment-IDs Zwischenspeichern.)</span><span class="sxs-lookup"><span data-stu-id="e1db5-139">(This is why the application should cache the list of segment IDs.)</span></span>


```C++
// Deletes the corresponding topology from the sequencer source

HRESULT CPlaylist::DeleteSegment(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    if (index == m_ActiveSegment)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId LastSegId = LastSegment();
    MFSequencerElementId SegmentID = m_segments[index].SegmentID;

    HRESULT hr  = m_pSequencerSource->DeleteTopology( SegmentID );
    if (FAILED(hr))
    {
        goto done;
    }

    //Delete the segment entry from the list.

    // Move everything up one slot.
    for (DWORD i = index; i < m_count - 1; i++)
    {
        m_segments[i] = m_segments[i + 1];
    }

    m_count --;
   
    // Is the deleted topology the last one?
    if (LastSegId == SegmentID)
    {
        //Get the new last segment id
        LastSegId = LastSegment();

        //set this topology as the last in the sequencer
        hr = m_pSequencerSource->UpdateTopologyFlags(LastSegId, SequencerTopologyFlags_Last);
    }

done:
    return hr;
}
```



## <a name="handling-session-events"></a><span data-ttu-id="e1db5-140">Behandeln von Sitzungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="e1db5-140">Handling Session Events</span></span>


```C++
HRESULT CPlaylist::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    IMFTopology *pTopology = NULL;

    UINT value = 0;
    DWORD  SegmentIndex;
    TOPOID TopoID;

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &value);
    if (FAILED(hr))
    {
        goto done;
    }

    switch(value)
    {
    case MF_TOPOSTATUS_STARTED_SOURCE:

        // Get information about the new segment
        hr = GetEventObject(pEvent, &pTopology);
        if (FAILED(hr))
        {
            hr = S_OK;
            goto done;
        }

        hr = pTopology->GetTopologyID(&TopoID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = LookupTopoID(TopoID, &SegmentIndex);
        if (FAILED(hr))
        {
            goto done;
        }

        m_ActiveSegment = SegmentIndex;
        hr = GetDurationFromTopology(pTopology, &m_hnsSegmentDuration);
        break;

    case MF_TOPOSTATUS_ENDED:
        m_ActiveSegment = (DWORD)-1;
        break;

    case MF_TOPOSTATUS_READY:
        if (m_state == OpenPending)
        {
            m_state = Stopped;
        }
        break;
    }

done:
    SafeRelease(&pTopology);
    return hr;
}
```




```C++
HRESULT CPlaylist::LookupTopoID(TOPOID id, DWORD *pIndex)
{
    DWORD index;
    for (index = 0; index < m_count; index++)
    {
        if (m_segments[ index ].TopoID == id)
        {
            break;
        }
    }

    if (index == m_count)
    {
        return MF_E_NOT_FOUND;
    }

    *pIndex = index;
    return S_OK;
}
```




```C++
HRESULT CPlaylist::OnSessionEvent(IMFMediaEvent *pEvent, MediaEventType meType)
{
    if (meType == MESessionNotifyPresentationTime)
    {
        m_PresentationTimeOffset = 
            MFGetAttributeUINT64(pEvent, MF_EVENT_PRESENTATION_TIME_OFFSET, 0);
    }
    return S_OK;
}
```




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




```C++
HRESULT GetDurationFromTopology(IMFTopology *pTopology, LONGLONG *phnsDuration)
{
    *phnsDuration = 0;

    IMFCollection *pSourceNodes = NULL;
    IMFTopologyNode *pNode = NULL;
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pTopology->GetSourceNodeCollection(&pSourceNodes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetCollectionObject(pSourceNodes, 0, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    hr = pNode->GetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, IID_PPV_ARGS(&pPD));
    if (FAILED(hr))
    {
        goto done;
    }

    *phnsDuration = MFGetAttributeUINT64(pPD, MF_PD_DURATION, 0);

done:
    SafeRelease(&pSourceNodes);
    SafeRelease(&pNode);
    SafeRelease(&pPD);
    return hr;
}
```




```C++
HRESULT CPlaylist::GetPlaybackTime(
    MFTIME *phnsPresentation,    // Relative to start of presentation.
    MFTIME *phnsSegment          // Relative to start of segment.
    )
{
    *phnsPresentation = 0;
    *phnsSegment = 0;

    HRESULT hr = m_pPresentationClock->GetTime(phnsPresentation);

    if (SUCCEEDED(hr))
    {
        *phnsSegment = (*phnsPresentation) - m_PresentationTimeOffset;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e1db5-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1db5-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1db5-142">Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="e1db5-142">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



