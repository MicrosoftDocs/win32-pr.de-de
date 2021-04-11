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
# <a name="implementation-considerations-for-ducking-notifications"></a>Implementierungs Überlegungen für Ducking-Benachrichtigungen

Die vom System bereitgestellte [standardmäßige duckingfunktion](stream-attenuation.md) übernimmt alle nicht-Kommunikationsstreams, die im System verfügbar sind, wenn ein Kommunikationsstream geöffnet wird. Eine Medien Anwendung kann die Standardbehandlung überschreiben, wenn Sie weiß, wann die Kommunikationssitzung beginnt und endet.

Sehen Sie sich das Szenario an, das von der Medien Anwendung im Beispiel " [duckingmediaplayer](duckingmediaplayer.md) " implementiert wird. Die Anwendung hält den Audiostream an, den Sie wieder gibt, wenn Sie eine Enten Benachrichtigung empfängt, und setzt die Wiedergabe fort, wenn eine unduck-Benachrichtigung empfangen wird. Die Ereignisse zum Anhalten und fortfahren werden in der Benutzeroberfläche der Medien Anwendung widergespiegelt. Dies wird durch zwei von der Anwendung definierte Fenster Meldungen unterstützt: die WM- \_ App- \_ Sitzung ist \_ geduckt und die WM- \_ App-Sitzung ist \_ \_ unverankert Die Ducking-Benachrichtigungen werden asynchron im Hintergrund empfangen, und die Medien Anwendung darf den Benachrichtigungs Thread nicht blockieren, um die Fenster Meldungen zu verarbeiten. Die Fenster Meldungen müssen im Benutzeroberflächen Thread verarbeitet werden.

Das Ducking-Verhalten funktioniert über einen Benachrichtigungs Mechanismus. Um eine angepasste Benutzeroberfläche bereitzustellen, muss die Medien Anwendung die [**iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) -Schnittstelle implementieren und die Implementierung beim Audiosystem registrieren. Bei erfolgreicher Registrierung empfängt die Medien Anwendung Ereignis Benachrichtigungen in Form von Rückrufen durch die Methoden in der-Schnittstelle. Der Sitzungs-Manager, der die Kommunikationssitzung verarbeitet, ruft [**iaudiovolumeducknotification:: onvolumeducknotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) auf, wenn der Kommunikationsstream geöffnet wird, und ruft dann [**iaudiovolumeducknotification:: onvolumeunducknotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) auf, wenn der Stream auf dem Kommunikationsgerät geschlossen wird.

Der folgende Code zeigt eine Beispiel Implementierung der [**iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) -Schnittstelle. Die Definition von cmediaplayer::D uckingoptout finden Sie unter erhalten von Ducking-Ereignissen von einem Kommunikationsgerät.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden eines kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Standardmäßiges ducken](stream-attenuation.md)
</dt> <dt>

[Deaktivieren der Standardeinstellung für das ducken](disabling-the-ducking-experience.md)
</dt> <dt>

[Bereitstellen eines benutzerdefinierten Ducking-Verhaltens](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Erhalten von Ducking-Ereignissen](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



