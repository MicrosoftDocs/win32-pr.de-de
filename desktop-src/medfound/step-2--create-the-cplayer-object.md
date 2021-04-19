---
description: Dieses Thema ist Schritt 2 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 'Schritt 2: Erstellen des cplayer-Objekts'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360128"
---
# <a name="step-2-create-the-cplayer-object"></a>Schritt 2: Erstellen des cplayer-Objekts

Dieses Thema ist Schritt 2 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.

Um eine Instanz der-Klasse zu erstellen `CPlayer` , ruft die Anwendung die statische- `CPlayer::CreateInstance` Methode auf. Diese Methode übernimmt die folgenden Parameter:

-   *hvideo* gibt das Fenster zum Anzeigen von Videos an.
-   *hevent* gibt ein Fenster für das Empfangen von Ereignissen an. Es ist zulässig, das gleiche Handle für beide Fenster Handles zu übergeben.
-   *ppplayer* erhält einen Zeiger auf eine neue- `CPlayer` Instanz.

Der folgende Code veranschaulicht die `CreateInstance`-Methode:


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
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

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



Der folgende Code zeigt den- `CPlayer` Konstruktor:


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



Der-Konstruktor führt Folgendes aus:

1.  Ruft [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) auf, um die Media Foundation Plattform zu initialisieren.
2.  Erstellt ein Ereignis für die automatische zurück Setzung. Dieses Ereignis wird beim Schließen der Medien Sitzung verwendet. Weitere Informationen finden [Sie unterschritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md).

Der debugtor fährt die Medien Sitzung herunter, wie in [Schritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md)beschrieben.


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



Beachten Sie, dass der Konstruktor und der Dekonstruktor beide geschützte Klassen Methoden sind. Die Anwendung erstellt das-Objekt mit der statischen- `CreateInstance` Methode. Das Objekt wird durch Aufrufen von " **IUnknown:: Release**" zerstört und nicht explizit mithilfe von " **Delete**".

Nächstes: [Schritt 3: Öffnen einer Mediendatei](step-3--open-a-media-file.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



