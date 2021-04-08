---
description: Dieses Thema ist Schritt 4 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Schritt 4: Erstellen der Medien Sitzung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961224"
---
# <a name="step-4-create-the-media-session"></a>Schritt 4: Erstellen der Medien Sitzung

Dieses Thema ist Schritt 4 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.

`CPlayer::CreateSession`Erstellt eine neue Instanz der Medien Sitzung.


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

1.  Ruft `CPlayer::CloseSession` auf, um eine vorherige Instanz der Medien Sitzung zu schließen.
2.  Ruft [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um eine neue Instanz der Medien Sitzung zu erstellen.
3.  Ruft die [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) -Methode auf, um das nächste Ereignis aus der Medien Sitzung anzufordern. Der erste Parameter für **begingetevent** ist ein Zeiger auf das **cplayer** -Objekt, das die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle einrichtet.

Die Ereignis Behandlung wird in Schritt 5 beschrieben.

Weiter: [Schritt 5: Behandeln von Ereignissen für Medien Sitzungen](step-5--handle-media-session-events.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



