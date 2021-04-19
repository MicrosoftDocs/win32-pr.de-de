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
# <a name="step-2-create-the-cplayer-object"></a><span data-ttu-id="73620-103">Schritt 2: Erstellen des cplayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="73620-103">Step 2: Create the CPlayer Object</span></span>

<span data-ttu-id="73620-104">Dieses Thema ist Schritt 2 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="73620-104">This topic is step 2 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="73620-105">Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73620-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="73620-106">Um eine Instanz der-Klasse zu erstellen `CPlayer` , ruft die Anwendung die statische- `CPlayer::CreateInstance` Methode auf.</span><span class="sxs-lookup"><span data-stu-id="73620-106">To create an instance of the `CPlayer` class, the application calls the static `CPlayer::CreateInstance` method.</span></span> <span data-ttu-id="73620-107">Diese Methode übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="73620-107">This method takes the following parameters:</span></span>

-   <span data-ttu-id="73620-108">*hvideo* gibt das Fenster zum Anzeigen von Videos an.</span><span class="sxs-lookup"><span data-stu-id="73620-108">*hVideo* specifies the window to display video.</span></span>
-   <span data-ttu-id="73620-109">*hevent* gibt ein Fenster für das Empfangen von Ereignissen an.</span><span class="sxs-lookup"><span data-stu-id="73620-109">*hEvent* specifies a window to receive events.</span></span> <span data-ttu-id="73620-110">Es ist zulässig, das gleiche Handle für beide Fenster Handles zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="73620-110">It is valid to pass the same handle for both window handles.</span></span>
-   <span data-ttu-id="73620-111">*ppplayer* erhält einen Zeiger auf eine neue- `CPlayer` Instanz.</span><span class="sxs-lookup"><span data-stu-id="73620-111">*ppPlayer* receives a pointer to a new `CPlayer` instance.</span></span>

<span data-ttu-id="73620-112">Der folgende Code veranschaulicht die `CreateInstance`-Methode:</span><span class="sxs-lookup"><span data-stu-id="73620-112">The following code shows the `CreateInstance` method:</span></span>


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



<span data-ttu-id="73620-113">Der folgende Code zeigt den- `CPlayer` Konstruktor:</span><span class="sxs-lookup"><span data-stu-id="73620-113">The following code shows the `CPlayer` constructor:</span></span>


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



<span data-ttu-id="73620-114">Der-Konstruktor führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="73620-114">The constructor does the following:</span></span>

1.  <span data-ttu-id="73620-115">Ruft [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) auf, um die Media Foundation Plattform zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="73620-115">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="73620-116">Erstellt ein Ereignis für die automatische zurück Setzung.</span><span class="sxs-lookup"><span data-stu-id="73620-116">Creates an auto-reset event.</span></span> <span data-ttu-id="73620-117">Dieses Ereignis wird beim Schließen der Medien Sitzung verwendet. Weitere Informationen finden [Sie unterschritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="73620-117">This event is used when closing the Media Session; see [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>

<span data-ttu-id="73620-118">Der debugtor fährt die Medien Sitzung herunter, wie in [Schritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="73620-118">The destructor shuts down the Media Session, as described in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>


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



<span data-ttu-id="73620-119">Beachten Sie, dass der Konstruktor und der Dekonstruktor beide geschützte Klassen Methoden sind.</span><span class="sxs-lookup"><span data-stu-id="73620-119">Note that the constructor and destructor are both protected class methods.</span></span> <span data-ttu-id="73620-120">Die Anwendung erstellt das-Objekt mit der statischen- `CreateInstance` Methode.</span><span class="sxs-lookup"><span data-stu-id="73620-120">The application creates the object using the static `CreateInstance` method.</span></span> <span data-ttu-id="73620-121">Das Objekt wird durch Aufrufen von " **IUnknown:: Release**" zerstört und nicht explizit mithilfe von " **Delete**".</span><span class="sxs-lookup"><span data-stu-id="73620-121">It destroys the object by calling **IUnknown::Release**, rather than explicitly using **delete**.</span></span>

<span data-ttu-id="73620-122">Nächstes: [Schritt 3: Öffnen einer Mediendatei](step-3--open-a-media-file.md)</span><span class="sxs-lookup"><span data-stu-id="73620-122">Next: [Step 3: Open a Media File](step-3--open-a-media-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="73620-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73620-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73620-124">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="73620-124">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="73620-125">Wiedergeben von Mediendateien mit Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73620-125">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



