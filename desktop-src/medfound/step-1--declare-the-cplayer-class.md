---
description: Dieses Thema ist Schritt 1 des Tutorials How to Play Media Files with Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 'Schritt 1: Deklarieren der CPlayer-Klasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61f03a9054e96769414320811d32a549027defb80ff929aba2c27ad4aa5b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112910"
---
# <a name="step-1-declare-the-cplayer-class"></a>Schritt 1: Deklarieren der CPlayer-Klasse

Dieses Thema ist Schritt 1 des Tutorials [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md). Der vollständige Code wird im Thema [Media Session Playback Example (Media Session Playback Example) gezeigt.](media-session-playback-example.md)

In diesem Tutorial ist die Wiedergabefunktion in der -Klasse `CPlayer` gekapselt. Die `CPlayer`-Klasse wird folgendermaßen deklariert:


```C++
const UINT WM_APP_PLAYER_EVENT = WM_APP + 1;   

    // WPARAM = IMFMediaEvent*, WPARAM = MediaEventType

enum PlayerState
{
    Closed = 0,     // No session.
    Ready,          // Session was created, ready to open a file. 
    OpenPending,    // Session is opening a file.
    Started,        // Session is playing a file.
    Paused,         // Session is paused.
    Stopped,        // Session is stopped (ready to play). 
    Closing         // Application has closed the session, but is waiting for MESessionClosed.
};

class CPlayer : public IMFAsyncCallback
{
public:
    static HRESULT CreateInstance(HWND hVideo, HWND hEvent, CPlayer **ppPlayer);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP  GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP  Invoke(IMFAsyncResult* pAsyncResult);

    // Playback
    HRESULT       OpenURL(const WCHAR *sURL);
    HRESULT       Play();
    HRESULT       Pause();
    HRESULT       Stop();
    HRESULT       Shutdown();
    HRESULT       HandleEvent(UINT_PTR pUnkPtr);
    PlayerState   GetState() const { return m_state; }

    // Video functionality
    HRESULT       Repaint();
    HRESULT       ResizeVideo(WORD width, WORD height);
    
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }

protected:
    
    // Constructor is private. Use static CreateInstance method to instantiate.
    CPlayer(HWND hVideo, HWND hEvent);

    // Destructor is private. Caller should call Release.
    virtual ~CPlayer(); 

    HRESULT Initialize();
    HRESULT CreateSession();
    HRESULT CloseSession();
    HRESULT StartPlayback();

    // Media event handlers
    virtual HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    virtual HRESULT OnPresentationEnded(IMFMediaEvent *pEvent);
    virtual HRESULT OnNewPresentation(IMFMediaEvent *pEvent);

    // Override to handle additional session events.
    virtual HRESULT OnSessionEvent(IMFMediaEvent*, MediaEventType) 
    { 
        return S_OK; 
    }

protected:
    long                    m_nRefCount;        // Reference count.

    IMFMediaSession         *m_pSession;
    IMFMediaSource          *m_pSource;
    IMFVideoDisplayControl  *m_pVideoDisplay;

    HWND                    m_hwndVideo;        // Video window.
    HWND                    m_hwndEvent;        // App window to receive events.
    PlayerState             m_state;            // Current state of the media session.
    HANDLE                  m_hCloseEvent;      // Event to wait on while closing.
};
```



Hier sind einige Dinge zu `CPlayer` beachten:

-   Die Konstante **WM \_ APP PLAYER \_ \_ EVENT** definiert eine Private Window-Nachricht. Diese Meldung wird verwendet, um die Anwendung über Media Session-Ereignisse zu benachrichtigen. Weitere Informationen [finden Sie unter Schritt 5: Behandeln von Mediensitzungsereignissen.](step-5--handle-media-session-events.md)
-   Die `PlayerState` -Enumeration definiert die möglichen Zustände des `CPlayer` -Objekts.
-   Die `CPlayer` -Klasse implementiert [**dieASYNCCallback-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) die zum Empfangen von Ereignisbenachrichtigungen aus der Mediensitzung verwendet wird.
-   Der `CPlayer` Konstruktor ist privat. Die Anwendung ruft die statische `CreateInstance` -Methode auf, um eine Instanz der -Klasse zu `CPlayer` erstellen.
-   Der `CPlayer` Destruktor ist ebenfalls privat. Die `CPlayer` -Klasse implementiert **IUnknown,** sodass die Lebensdauer des Objekts über die Verweisanzahl (*m \_ nRefCount*) gesteuert wird. Um das Objekt zu zerstören, ruft die Anwendung **IUnknown::Release auf** und löscht **nicht**.
-   Das `CPlayer` -Objekt verwaltet sowohl die Mediensitzung als auch die Medienquelle.

## <a name="implement-iunknown"></a>Implementieren von IUnknown

Die `CPlayer` -Klasse implementiert [**DIEASYNCCallback-Klasse,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)die **IUnknown erbt.**

Der hier gezeigte Code ist eine ziemlich standardmäßige Implementierung von **IUnknown**. Wenn Sie möchten, können Sie die Active Template Library (ATL) verwenden, um diese Methoden zu implementieren. Unterstützt jedoch `CPlayer` weder [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) noch erweiterte COM-Features, sodass es hier keinen überforderischen Grund gibt, ATL zu verwenden.


```C++
HRESULT CPlayer::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CPlayer, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

ULONG CPlayer::AddRef()
{
    return InterlockedIncrement(&m_nRefCount);
}

ULONG CPlayer::Release()
{
    ULONG uCount = InterlockedDecrement(&m_nRefCount);
    if (uCount == 0)
    {
        delete this;
    }
    return uCount;
}
```



Weiter: [Schritt 2: Erstellen des CPlayer-Objekts](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiederspielen von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
