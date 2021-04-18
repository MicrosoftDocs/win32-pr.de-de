---
description: Dieses Thema ist Schritt 1 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 'Schritt 1: Deklarieren der cplayer-Klasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1593842ecece68fcd3c4cca35a7e2e28eac503c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354568"
---
# <a name="step-1-declare-the-cplayer-class"></a>Schritt 1: Deklarieren der cplayer-Klasse

Dieses Thema ist Schritt 1 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.

In diesem Tutorial wird die Wiedergabefunktion in der-Klasse gekapselt `CPlayer` . Die `CPlayer`-Klasse wird folgendermaßen deklariert:


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



Hier sind einige Punkte zu beachten `CPlayer` :

-   Das Ereignis "Constant **WM \_ App \_ Player \_** " definiert eine private Fenster Meldung. Diese Meldung wird verwendet, um die Anwendung über Medien Sitzungs Ereignisse zu benachrichtigen. Weitere Informationen finden Sie unter [Step 5: handle Media Session Events](step-5--handle-media-session-events.md).
-   Die- `PlayerState` Enumeration definiert die möglichen Zustände des- `CPlayer` Objekts.
-   Die- `CPlayer` Klasse implementiert die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle, die verwendet wird, um Ereignis Benachrichtigungen von der Medien Sitzung zu erhalten.
-   Der `CPlayer` Konstruktor ist privat. Die Anwendung ruft die statische- `CreateInstance` Methode auf, um eine Instanz der-Klasse zu erstellen `CPlayer` .
-   Der `CPlayer` Dekonstruktor ist auch privat. Die `CPlayer` Klasse implementiert **IUnknown**, sodass die Lebensdauer des Objekts durch den Verweis Zähler (*m \_ nref count*) gesteuert wird. Um das Objekt zu zerstören, ruft die Anwendung **IUnknown:: Release** und nicht **Delete** auf.
-   Das `CPlayer` -Objekt verwaltet sowohl die Medien Sitzung als auch die Medienquelle.

## <a name="implement-iunknown"></a>Implementieren von IUnknown

Die `CPlayer` Klasse implementiert [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), das **IUnknown** erbt.

Der hier gezeigte Code ist eine relativ standardmäßige Implementierung von **IUnknown**. Wenn Sie möchten, können Sie die Active Template Library (ATL) verwenden, um diese Methoden zu implementieren. `CPlayer`Unterstützt jedoch keine [**cokreateingestance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -oder Advanced COM-Funktionen, sodass es keinen überwältigenden Grund gibt, ATL hier zu verwenden.


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



Weiter: [Schritt 2: Erstellen des cplayer-Objekts](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
