---
description: Dieses Thema ist Schritt 3 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Schritt 3: Öffnen einer Mediendatei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050702"
---
# <a name="step-3-open-a-media-file"></a>Schritt 3: Öffnen einer Mediendatei

Dieses Thema ist Schritt 3 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.

Die- `CPlayer::OpenURL` Methode öffnet eine Mediendatei aus einer URL.


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

1.  Ruft **cplayer:: kreatesession** auf, um eine neue Instanz der Medien Sitzung zu erstellen. Weitere Informationen finden Sie [unterschritt 4: Erstellen der Medien Sitzung](step-4--create-the-media-session.md).
2.  Erstellt eine Medienquelle aus der URL. Den gesamten Code für diesen Schritt finden Sie im Thema [using the Source Resolver](using-the-source-resolver.md).
3.  Ruft [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) auf, um den Präsentations Deskriptor der Medienquelle zu erhalten. Der Präsentations Deskriptor beschreibt die einzelnen Streams in der Quelldatei.
4.  Erstellt die Wiedergabe Topologie. Code für diesen Schritt finden Sie im Thema [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md).
5.  Ruft [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) auf, um die Topologie für die Medien Sitzung festzulegen.

Die [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode wird asynchron abgeschlossen. Wenn der Vorgang abgeschlossen ist, wird die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode des cplayer-Objekts aufgerufen. Weitere Informationen finden Sie unter [Step 5: handle Media Session Events](step-5--handle-media-session-events.md).

Nächste [Schritte: Schritt 4: Erstellen der Medien Sitzung](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



