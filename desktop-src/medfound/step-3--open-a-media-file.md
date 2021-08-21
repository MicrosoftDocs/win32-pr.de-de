---
description: Dieses Thema ist Schritt 3 des Tutorials How to Play Media Files with Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Schritt 3: Öffnen einer Mediendatei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c198b07358ebbf5d8da591d75d44f4687b600f6bb387c4f55901974397308dc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012352"
---
# <a name="step-3-open-a-media-file"></a>Schritt 3: Öffnen einer Mediendatei

Dieses Thema ist Schritt 3 des Tutorials [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md). Der vollständige Code wird im Thema [Media Session Playback Example (Media Session Playback Example) gezeigt.](media-session-playback-example.md)

Die `CPlayer::OpenURL` -Methode öffnet eine Mediendatei aus einer URL.


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



Diese Methode führt die folgenden Schritte aus:

1.  Ruft **CPlayer::CreateSession auf,** um eine neue Instanz der Mediensitzung zu erstellen. Weitere Informationen [finden Sie unter Schritt 4: Erstellen der Mediensitzung.](step-4--create-the-media-session.md)
2.  Erstellt eine Medienquelle aus der URL. Der vollständige Code für diesen Schritt wird im Thema Using [the Source Resolver (Verwenden des Quellre resolvers) gezeigt.](using-the-source-resolver.md)
3.  Ruft [**DEN MEDIENMEDIASOURCE::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) auf, um den Präsentationsdeskriptor der Medienquelle zu erhalten. Der Präsentationsdeskriptor beschreibt die einzelnen Streams in der Quelldatei.
4.  Erstellt die Wiedergabetopologie. Der Code für diesen Schritt wird im Thema Creating [Playback Topologies (Erstellen von Wiedergabetopologien) gezeigt.](creating-playback-topologies.md)
5.  Ruft [**DIEZMediaSession::SetTopology auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) um die Topologie für die Mediensitzung festzugeben.

Die [**SetTopology-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) wird asynchron abgeschlossen. Nach Abschluss des Verfahrens wird die [**METHODEASYNCCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) des CPlayer-Objekts aufgerufen. Siehe [Schritt 5: Behandeln von Mediensitzungsereignissen](step-5--handle-media-session-events.md).

Weiter: [Schritt 4: Erstellen der Mediensitzung](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiederspielen von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



