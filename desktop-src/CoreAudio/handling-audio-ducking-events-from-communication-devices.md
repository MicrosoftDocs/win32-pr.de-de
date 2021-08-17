---
description: Die vom System bereitgestellte Standardverhaltenserfahrung stiert alle im System verfügbaren Nichtkommunikationsstreams, wenn ein Kommunikationsstream geöffnet wird.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Überlegungen zur Implementierung von Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61d7e67bd456e962442f62f59c3119c756258aadd75334e7736cbc69fba0867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957319"
---
# <a name="implementation-considerations-for-ducking-notifications"></a>Überlegungen zur Implementierung von Benachrichtigungen

Die [vom System bereitgestellte](stream-attenuation.md) Standardverhaltenserfahrung stiert alle im System verfügbaren Nichtkommunikationsstreams, wenn ein Kommunikationsstream geöffnet wird. Eine Medienanwendung kann die Standardbehandlung überschreiben, wenn sie weiß, wann die Kommunikationssitzung gestartet und beendet wird.

Betrachten Sie das Szenario, das von der Medienanwendung im [Beispiel "IngMediaPlayer" implementiert](duckingmediaplayer.md) wird. Die Anwendung hält den Abspieldatenstrom an, wenn sie eine Benachrichtigung empfängt, und setzt die Wiedergabe fort, wenn sie eine Benachrichtigung zum Abdrucken empfängt. Die Pausen- und Fortsetzungsereignisse werden auf der Benutzeroberfläche der Medienanwendung widergespiegelt. Dies wird durch zwei anwendungsdefinierte Fenstermeldungen unterstützt: WM APP SESSION UNBEsädigt \_ und WM APP SESSION \_ \_ \_ \_ \_ UNDUCKED. Die sendenden Benachrichtigungen werden asynchron im Hintergrund empfangen, und die Medienanwendung darf den Benachrichtigungsthread nicht blockieren, um die Fenstermeldungen zu verarbeiten. Die Fenstermeldungen müssen im Benutzeroberflächenthread verarbeitet werden.

Das Benachrichtigungsverhalten funktioniert über einen Benachrichtigungsmechanismus. Um eine benutzerdefinierte Oberfläche zu bieten, muss die Medienanwendung die [**IAudioVolumeDuckNotification-Schnittstelle**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementieren und die Implementierung beim Audiosystem registrieren. Nach erfolgreicher Registrierung empfängt die Medienanwendung Ereignisbenachrichtigungen in Form von Rückrufen über die Methoden in der Schnittstelle. Der Sitzungs-Manager, der die Kommunikationssitzung verwendet, ruft [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) auf, wenn der Kommunikationsstream geöffnet wird, und ruft dann [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) auf, wenn der Stream auf dem Kommunikationsgerät geschlossen wird.

Der folgende Code zeigt eine Beispielimplementierung der [**IAudioVolumeDuckNotification-Schnittstelle.**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) Die Definition von CMediaPlayer::D uckingOptOut finden Sie unter Getting GettingIng Events from a Communication Device (Abrufen von Beschriftungsereignissen von einem Kommunikationsgerät).


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

[Verwenden eines Kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Standardeinstellung für die Beeinschnung](stream-attenuation.md)
</dt> <dt>

[Deaktivieren der Standardmäßigen Begeherfahrung](disabling-the-ducking-experience.md)
</dt> <dt>

[Bereitstellen eines benutzerdefinierten Verhaltens bei der Abschüssung](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Getting GettingIng Events (Getting GettingIng Events) (Abrufen](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



