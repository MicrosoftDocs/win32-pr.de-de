---
description: Dieses Thema ist Schritt 4 des Tutorials Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Schritt 4: Erstellen der Mediensitzung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9c31d4c5e07abe8f088aad38fec9f91046a7d4338905dbd917de9d414fd4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847770"
---
# <a name="step-4-create-the-media-session"></a>Schritt 4: Erstellen der Mediensitzung

Dieses Thema ist Schritt 4 des Tutorials Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der vollständige Code wird im Thema [Mediensitzung – Wiedergabebeispiel](media-session-playback-example.md)gezeigt.

`CPlayer::CreateSession`Erstellt eine neue Instanz der Mediensitzung.


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



Diese Methode führt die folgenden Schritte aus:

1.  Ruft `CPlayer::CloseSession` auf, um eine vorherige Instanz der Mediensitzung zu schließen.
2.  Ruft [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um eine neue Instanz der Mediensitzung zu erstellen.
3.  Ruft die [**METHODE VONMEDIAEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) auf, um das nächste Ereignis von der Mediensitzung anzufordern. Der erste Parameter für **BeginGetEvent** ist ein Zeiger auf das **CPlayer-Objekt** selbst, das die [**INTERFACESAsyncCallback-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementiert.

Die Ereignisbehandlung wird in Schritt 5 beschrieben.

Weiter: [Schritt 5: Behandeln von Mediensitzungsereignissen](step-5--handle-media-session-events.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



