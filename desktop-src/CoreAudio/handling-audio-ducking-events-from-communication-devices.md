---
description: Die vom System bereitgestellte standardmäßige duckingfunktion übernimmt alle nicht-Kommunikationsstreams, die im System verfügbar sind, wenn ein Kommunikationsstream geöffnet wird.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Implementierungs Überlegungen für Ducking-Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de07ea23b7cdc8d726ab68a5a6554bf1713a921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127053"
---
# <a name="implementation-considerations-for-ducking-notifications"></a><span data-ttu-id="8906b-103">Implementierungs Überlegungen für Ducking-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="8906b-103">Implementation Considerations for Ducking Notifications</span></span>

<span data-ttu-id="8906b-104">Die vom System bereitgestellte [standardmäßige duckingfunktion](stream-attenuation.md) übernimmt alle nicht-Kommunikationsstreams, die im System verfügbar sind, wenn ein Kommunikationsstream geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8906b-104">The [Default Ducking Experience](stream-attenuation.md) provided by the system ducks all non-communication streams available in the system when a communication stream opens.</span></span> <span data-ttu-id="8906b-105">Eine Medien Anwendung kann die Standardbehandlung überschreiben, wenn Sie weiß, wann die Kommunikationssitzung beginnt und endet.</span><span class="sxs-lookup"><span data-stu-id="8906b-105">A media application can override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="8906b-106">Sehen Sie sich das Szenario an, das von der Medien Anwendung im Beispiel " [duckingmediaplayer](duckingmediaplayer.md) " implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="8906b-106">Consider the scenario implemented by the media application in the [DuckingMediaPlayer](duckingmediaplayer.md) sample.</span></span> <span data-ttu-id="8906b-107">Die Anwendung hält den Audiostream an, den Sie wieder gibt, wenn Sie eine Enten Benachrichtigung empfängt, und setzt die Wiedergabe fort, wenn eine unduck-Benachrichtigung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="8906b-107">The application pauses the audio stream that it is playing when it receives a duck notification and continues playback when it receives an unduck notification.</span></span> <span data-ttu-id="8906b-108">Die Ereignisse zum Anhalten und fortfahren werden in der Benutzeroberfläche der Medien Anwendung widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="8906b-108">The pause and continue events are reflected in the media application's user interface.</span></span> <span data-ttu-id="8906b-109">Dies wird durch zwei von der Anwendung definierte Fenster Meldungen unterstützt: die WM- \_ App- \_ Sitzung ist \_ geduckt und die WM- \_ App-Sitzung ist \_ \_ unverankert</span><span class="sxs-lookup"><span data-stu-id="8906b-109">This is supported through two application-defined window messages, WM\_APP\_SESSION\_DUCKED and WM\_APP\_SESSION\_UNDUCKED.</span></span> <span data-ttu-id="8906b-110">Die Ducking-Benachrichtigungen werden asynchron im Hintergrund empfangen, und die Medien Anwendung darf den Benachrichtigungs Thread nicht blockieren, um die Fenster Meldungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8906b-110">The ducking notifications are received asynchronously in the background and the media application must not block the notification thread to process the window messages.</span></span> <span data-ttu-id="8906b-111">Die Fenster Meldungen müssen im Benutzeroberflächen Thread verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8906b-111">The window messages must be processed on the user interface thread.</span></span>

<span data-ttu-id="8906b-112">Das Ducking-Verhalten funktioniert über einen Benachrichtigungs Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="8906b-112">The ducking behavior works through a notification mechanism.</span></span> <span data-ttu-id="8906b-113">Um eine angepasste Benutzeroberfläche bereitzustellen, muss die Medien Anwendung die [**iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) -Schnittstelle implementieren und die Implementierung beim Audiosystem registrieren.</span><span class="sxs-lookup"><span data-stu-id="8906b-113">To provide a customized experience, the media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="8906b-114">Bei erfolgreicher Registrierung empfängt die Medien Anwendung Ereignis Benachrichtigungen in Form von Rückrufen durch die Methoden in der-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8906b-114">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="8906b-115">Der Sitzungs-Manager, der die Kommunikationssitzung verarbeitet, ruft [**iaudiovolumeducknotification:: onvolumeducknotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) auf, wenn der Kommunikationsstream geöffnet wird, und ruft dann [**iaudiovolumeducknotification:: onvolumeunducknotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) auf, wenn der Stream auf dem Kommunikationsgerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="8906b-115">The session manager handling the communication session calls [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) when the communication stream opens and then calls [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) when the stream is closed on the communication device.</span></span>

<span data-ttu-id="8906b-116">Der folgende Code zeigt eine Beispiel Implementierung der [**iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8906b-116">The following code shows a sample implementation of the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface.</span></span> <span data-ttu-id="8906b-117">Die Definition von cmediaplayer::D uckingoptout finden Sie unter erhalten von Ducking-Ereignissen von einem Kommunikationsgerät.</span><span class="sxs-lookup"><span data-stu-id="8906b-117">For the definition of CMediaPlayer::DuckingOptOut, see Getting Ducking Events from a Communication Device.</span></span>


```C++
class CMediaPlayer : public IAudioVolumeDuckNotification
{
    LONG _refCount;

    HWND _AppWindow;

    ~CMediaPlayer();

    STDMETHOD(OnVolumeDuckNotification) (LPCWSTR sessionID, 
                  UINT32 countCommunicationSessions);
    STDMETHOD(OnVolumeUnduckNotification) (LPCWSTR sessionID);

public:
    CDuckingImpl(HWND hWnd);
    HRESULT DuckingOptOut(bool GetDuckEvents);

    // IUnknown
    IFACEMETHODIMP QueryInterface(__in REFIID riid, __deref_out void **ppv);
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
};

CMediaPlayer::CMediaPlayer(HWND AppWindow) :
        _AppWindow(AppWindow),
        _refCount(1)
{
}
CMediaPlayer::~CMediaPlayer()
{
}

// When we receive a duck notification, 
// post a "Session Ducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeDuckNotification(LPCWSTR SessionID, 
                                                    UINT32 CountCommunicationsSessions)
{
    PostMessage(_AppWindow, WM_APP_SESSION_DUCKED, 0, 0);
    return 0;
}


// When we receive an unduck notification, 
// post a "Session Unducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeUnduckNotification(LPCWSTR SessionID)
{
    PostMessage(_AppWindow, WM_APP_SESSION_UNDUCKED, 0, 0);
    return 0;
}

IFACEMETHODIMP CMediaPlayer::QueryInterface(REFIID iid, void **pvObject)
{
    if (pvObject == NULL)
    {
        return E_POINTER;
    }
    *pvObject = NULL;
    if (iid == IID_IUnknown)
    {
        *pvObject = static_cast<IUnknown *>(static_cast<IAudioVolumeDuckNotification *>
                                                                              (this));
        AddRef();
    }
    else if (iid == __uuidof(IAudioVolumeDuckNotification))
    {
        *pvObject = static_cast<IAudioVolumeDuckNotification *>(this);
        AddRef();
    }
    else
    {
        return E_NOINTERFACE;
    }
    return S_OK;
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::AddRef()
{
    return InterlockedIncrement(&_refCount);
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::Release()
{
    LONG refs = InterlockedDecrement(&_refCount);

    if (refs == 0)
    {
        delete this; 
    }

    return refs;   
}
```



## <a name="related-topics"></a><span data-ttu-id="8906b-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8906b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8906b-119">Verwenden eines kommunikationsgeräts</span><span class="sxs-lookup"><span data-stu-id="8906b-119">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="8906b-120">Standardmäßiges ducken</span><span class="sxs-lookup"><span data-stu-id="8906b-120">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="8906b-121">Deaktivieren der Standardeinstellung für das ducken</span><span class="sxs-lookup"><span data-stu-id="8906b-121">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="8906b-122">Bereitstellen eines benutzerdefinierten Ducking-Verhaltens</span><span class="sxs-lookup"><span data-stu-id="8906b-122">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="8906b-123">Erhalten von Ducking-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="8906b-123">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



