---
description: Dieses Thema zeigt Beispielcode für die Verwendung der Sequencer-Quelle in Microsoft Media Foundation.
ms.assetid: 6f39a297-33a9-414a-9d41-47aec54eaa6b
title: Sequencer-Quellcodebeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3098faa0b979d6ad3baa96256c0ffac1eb14f482df5caff966ebc1cda3957f50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012356"
---
# <a name="sequencer-source-example-code"></a>Sequencer-Quellcodebeispiel

In diesem Thema wird Beispielcode für die Verwendung der [Sequencer-Quelle](sequencer-source.md) in Microsoft Media Foundation gezeigt. Der Abschnitt ist wie folgt gegliedert.

-   [CPlaylist-Klasse](#cplaylist-class)
-   [Erstellen einer Instanz von CPlaylist](#creating-an-instance-of-cplaylist)
-   [Hinzufügen und Entfernen von Wiedergabelistensegmenten](#adding-and-removing-playlist-segments)
-   [Behandeln von Sitzungsereignissen](#handling-session-events)
-   [Zugehörige Themen](#related-topics)

## <a name="cplaylist-class"></a>CPlaylist-Klasse

Die `CPlaylist` -Klasse wird von der `CPlayer` -Klasse abgeleitet, die im Tutorial Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)gezeigt wird.


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



## <a name="creating-an-instance-of-cplaylist"></a>Erstellen einer Instanz von CPlaylist

Die `CPlaylist::CreateInstance` -Methode erstellt ein neues `CPlaylist` -Objekt. Intern ruft diese Methode `CPlaylist::Initialize` auf, um das Objekt zu initialisieren. Die `Initialize` -Methode ruft [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) auf, um die Sequenzquelle zu erstellen. Außerdem ruft sie [**DIE DATEI "POINTERMediaSession::GetClock"**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) auf, um einen Zeiger auf die Präsentationsuhr abzurufen.


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



## <a name="adding-and-removing-playlist-segments"></a>Hinzufügen und Entfernen von Wiedergabelistensegmenten

Die `AddSegment` -Methode fügt ein neues Wiedergabelistensegment hinzu.

Diese Methode führt die folgenden Schritte aus:

1.  Erstellt eine Wiedergabetopologie. Der Code für diesen Schritt wird im Thema [Erstellen von Wiedergabetopologien](creating-playback-topologies.md)gezeigt.
2.  Ruft [**DIE APPENDSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) auf, um die Topologie der Wiedergabeliste hinzuzufügen.
3.  Ruft im ersten Segment den Wert des [**MF \_ PD \_ DURATION-Attributs**](mf-pd-duration-attribute.md) ab, das die Wiedergabedauer enthält.
4.  Speichert die Segment-ID und die Topologie-ID in einer Nachschlagetabelle.


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



Die `AddSegment` -Methode ist privat für `CPlaylist` und wird von der folgenden öffentlichen Methode aufgerufen:


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



Wenn Sie das erste Wiedergabelistensegment erstellen, müssen Sie die Segmenttopologie wie folgt in der Mediensitzung in die Warteschlange stellen:

1.  Fragen Sie die Sequencerquelle nach der [**SCHNITTSTELLE VONMEDIASourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) ab.
2.  Übergeben Sie den Präsentationsdeskriptor an die [**METHODE VONMEDIASOURCETopologyProvider::GetMediaSourceTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) Diese Methode ruft einen Zeiger auf die Segmenttopologie ab. Beachten Sie, dass diese Topologie nicht genau mit der Wiedergabetopologie identisch ist, die Sie zuvor erstellt haben. Stattdessen handelt es sich um eine geänderte Version dieser Topologie. Weitere Informationen finden Sie unter [Informationen zur Sequencerquelle.](about-the-sequencer-source.md)
3.  Stellen Sie die Topologie in der Mediensitzung in die Warteschlange, indem Sie [**DEN AUFRUF VONMEDIASESSION::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufrufen.

Der folgende Code zeigt diese Schritte. Der gleiche Code wird auch verwendet, wenn die Wiedergabeliste das nächste Segment vorabrollt.


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



Um ein Wiedergabelistensegment zu löschen, rufen Sie [**DANNSEQUENcerSource::D eleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology)auf. Das Segment wird durch die Segment-ID angegeben. (Aus diesem Grund sollte die Anwendung die Liste der Segment-IDs zwischenspeichern.)


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



## <a name="handling-session-events"></a>Behandeln von Sitzungsereignissen


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 



