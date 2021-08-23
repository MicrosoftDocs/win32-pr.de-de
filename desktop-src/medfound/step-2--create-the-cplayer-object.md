---
description: Dieses Thema ist Schritt 2 des Tutorials Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 'Schritt 2: Erstellen des CPlayer-Objekts'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df004aa060a8ce8a46adbf0fdae438ca0a0cd1a454e9fc17889ad29eebef21ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847780"
---
# <a name="step-2-create-the-cplayer-object"></a>Schritt 2: Erstellen des CPlayer-Objekts

Dieses Thema ist Schritt 2 des Tutorials Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der vollständige Code wird im Thema [Mediensitzung – Wiedergabebeispiel](media-session-playback-example.md)gezeigt.

Um eine Instanz der -Klasse zu `CPlayer` erstellen, ruft die Anwendung die statische `CPlayer::CreateInstance` Methode auf. Diese Methode verwendet die folgenden Parameter:

-   *hVideo* gibt das Fenster zum Anzeigen des Videos an.
-   *hEvent* gibt ein Fenster zum Empfangen von Ereignissen an. Es ist gültig, das gleiche Handle für beide Fensterhandles zu übergeben.
-   *ppPlayer* empfängt einen Zeiger auf eine neue `CPlayer` -Instanz.

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



Der folgende Code zeigt den `CPlayer` Konstruktor:


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



Der Konstruktor führt folgende Schritte aus:

1.  Ruft [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) auf, um die Media Foundation Plattform zu initialisieren.
2.  Erstellt ein Ereignis für die automatische Zurücksetzung. Dieses Ereignis wird verwendet, wenn die Mediensitzung geschlossen wird. siehe [Schritt 7: Herunterfahren der Mediensitzung.](step-7--shut-down-the-media-session.md)

Der Destruktor fährt die Mediensitzung herunter, wie in [Schritt 7: Herunterfahren der Mediensitzung](step-7--shut-down-the-media-session.md)beschrieben.


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



Beachten Sie, dass Konstruktor und Destruktor geschützte Klassenmethoden sind. Die Anwendung erstellt das Objekt mithilfe der statischen `CreateInstance` Methode. Es zerstört das -Objekt, indem **IUnknown::Release** aufgerufen wird, anstatt explizit delete zu **verwenden.**

Weiter: [Schritt 3: Öffnen einer Mediendatei](step-3--open-a-media-file.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



