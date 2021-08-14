---
description: In diesem Thema wird beschrieben, wie Die Audiolautstärke bei Verwendung von MFPlay für die Audio-/Videowiedergabe gesteuert wird.
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: Verwalten der Audiositzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8573bd7145cc792d3178d51cead18c3a8694dde9281644b37439a377f18bec96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062825"
---
# <a name="managing-the-audio-session"></a>Verwalten der Audiositzung

\[MFPlay ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Die Audiolautstärke bei Verwendung von MFPlay für die Audio-/Videowiedergabe gesteuert wird.

MFPlay stellt die folgenden Methoden bereit, um die Audiolautstärke während der Wiedergabe zu steuern.



| Methode                                                            | BESCHREIBUNG                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [**IMFPMediaPlayer::SetBalance**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | Legt das Gleichgewicht zwischen dem linken und dem rechten Kanal fest. |
| [**IMFPMediaPlayer::SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | Stummschalten oder Aufheben der Audioumschaltung.                           |
| [**IMFPMediaPlayer::SetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | Legt die Volumeebene fest.                                |



 

Um das Verhalten dieser Methoden zu verstehen, müssen Sie einige Terminologie aus der Windows Audio Session API (WASAPI) kennen, die die von MFPlay verwendete Low-Level-Audiofunktionalität implementiert.

In WASAPI gehört jeder Audiostream zu genau einer *Audiositzung,* bei der es sich um eine Gruppe verwandter Audiostreams handelt. In der Regel verwaltet eine Anwendung eine einzelne Audiositzung, obwohl Anwendungen mehrere Sitzungen erstellen können. Das Systemvolume-Steuerungsprogramm (Sndvol) zeigt eine Lautstärkeregler für jede Audiositzung an. Über Sndvol kann ein Benutzer die Lautstärke einer Audiositzung von außerhalb der Anwendung anpassen. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm, das Audiostreams zeigt, die die Lautstärkeregler auf dem Weg zu den Lautsprechern durchlaufen; Anwendung und Sndvolume zeigen auf Volumesteuerung](images/audio-session.gif)

In MFPlay kann ein Medienelement über einen oder mehrere aktive Audiostreams verfügen (in der Regel nur einen). Intern verwendet MFPlay den [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR), um die Audiostreams zu rendern. Sofern Sie dies nicht anders konfigurieren, wird die Standardaudiositzung der Anwendung vom SAR-Join verwendet.

Die MFPlay-Audiomethoden steuern nur die Streams, die zum aktuellen Medienelement gehören. Sie wirken sich nicht auf das Volume für andere Streams aus, die zur gleichen Audiositzung gehören. Im Hinblick auf WASAPI steuern die MFPlay-Methoden die *Pro-Kanal-Volumeebenen,* nicht die Mastervolumeebene. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm ähnlich dem vorherigen, aber der zweite Stream beginnt beim Medienelement, und die Anwendung verweist auf den zweiten Stream und auf die Volumesteuerung.](images/audio-session02.gif)

Es ist wichtig, einige Auswirkungen dieses Features von MFPlay zu verstehen. Zunächst kann eine Anwendung die Wiedergabelautstärke anpassen, ohne dass andere Audiostreams beeinträchtigt werden. Sie können dieses Feature verwenden, wenn MFPlay die Audioüberblendung implementiert, indem Sie zwei Instanzen des MFPlay-Objekts erstellen und die Lautstärke separat anpassen.

Wenn Sie MFPlay-Methoden verwenden, um das Volume oder den Stummschaltungszustand zu ändern, werden die Änderungen nicht in Sndvol angezeigt. Beispielsweise können Sie [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) aufrufen, um die Audiodaten zu stummschalten, aber Sndvol zeigt die Sitzung nicht als stummgeschaltet an. Wenn dagegen SndVol zum Anpassen des Sitzungsvolumes verwendet wird, spiegeln sich die Änderungen nicht in den Werten wider, die von [**IMFPMediaPlayer::GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) oder [**IMFPMediaPlayer::GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute)zurückgegeben werden.

Für jede Instanz des MFPlay-Playerobjekts entspricht die effektive Volumeebene *fPlayerVolume* × *fSessionVolume,* wobei *fPlayerVolume* der von [**GetVolume zurückgegebene**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)Wert und *fSessionVolume* das Mastervolume für die Sitzung ist.

Bei einfachen Wiedergabeszenarien ist es möglicherweise besser, die WASAPI zum Steuern der Audiolautstärke für die gesamte Sitzung zu verwenden, anstatt die MFPlay-Methoden zu verwenden.

## <a name="example-code"></a>Beispielcode

Im Folgenden wird eine C++-Klasse beschrieben, die die grundlegenden Aufgaben in WASAPI verarbeitet:

-   Steuern des Volumes und des Stummschaltungszustands für die Sitzung.
-   Abrufen von Benachrichtigungen, wenn sich das Volume oder der Stummschaltungszustand ändert.

### <a name="class-declaration"></a>Klassendeklaration

Die `CAudioSessionVolume` Klassendeklaration implementiert die [**IAudioSessionEvents-Schnittstelle,**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) die die Rückrufschnittstelle für Audiositzungsereignisse ist.


```C++
class CAudioSessionVolume : public IAudioSessionEvents
{
public:
    // Static method to create an instance of the object.
    static HRESULT CreateInstance(
        UINT uNotificationMessage,
        HWND hwndNotification,
        CAudioSessionVolume **ppAudioSessionVolume
    );

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IAudioSessionEvents methods.

    STDMETHODIMP OnSimpleVolumeChanged(
        float NewVolume,
        BOOL NewMute,
        LPCGUID EventContext
        );

    // The remaining audio session events do not require any action.
    STDMETHODIMP OnDisplayNameChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnIconPathChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnChannelVolumeChanged(DWORD,float[],DWORD,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnGroupingParamChanged(LPCGUID,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnStateChanged(AudioSessionState)
    {
        return S_OK;
    }

    STDMETHODIMP OnSessionDisconnected(AudioSessionDisconnectReason)
    {
        return S_OK;
    }

    // Other methods
    HRESULT EnableNotifications(BOOL bEnable);
    HRESULT GetVolume(float *pflVolume);
    HRESULT SetVolume(float flVolume);
    HRESULT GetMute(BOOL *pbMute);
    HRESULT SetMute(BOOL bMute);
    HRESULT SetDisplayName(const WCHAR *wszName);

protected:
    CAudioSessionVolume(UINT uNotificationMessage, HWND hwndNotification);
    ~CAudioSessionVolume();

    HRESULT Initialize();

protected:
    LONG m_cRef;                        // Reference count.
    UINT m_uNotificationMessage;        // Window message to send when an audio event occurs.
    HWND m_hwndNotification;            // Window to receives messages.
    BOOL m_bNotificationsEnabled;       // Are audio notifications enabled?

    IAudioSessionControl    *m_pAudioSession;
    ISimpleAudioVolume      *m_pSimpleAudioVolume;
};
```



Wenn das `CAudioSessionVolume` Objekt ein Audiositzungsereignis empfängt, sendet es eine Private Window-Nachricht an die Anwendung. Das Fensterhandle und die Fenstermeldung werden der statischen Methode als Parameter `CAudioSessionVolume::CreateInstance` übergeben.

### <a name="getting-the-wasapi-interface-pointers"></a>Abrufen der WASAPI-Schnittstellenzeiger

`CAudioSessionVolume` verwendet zwei WASAPI-Hauptschnittstellen:

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) verwaltet die Audiositzung.
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) steuert die Volumeebene und den Stummschaltungszustand der Sitzung.

Um diese Schnittstellen abzurufen, müssen Sie den Audioendpunkt aufzählen, der vom SAR verwendet wird. Ein *Audioendpunkt* ist ein Hardwaregerät, das Audiodaten erfasst oder nutzt. Bei der Audiowiedergabe ist ein Endpunkt einfach ein Lautsprecher oder eine andere Audioausgabe. Standardmäßig verwendet die SAR den Standardendpunkt für die **eConsole-Geräterolle.** Eine *Geräterolle* ist eine zugewiesene Rolle für einen Endpunkt. Geräterollen werden durch die [**ERole-Enumeration**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) angegeben, die in [Core Audio-APIs](../coreaudio/core-audio-apis-in-windows-vista.md)dokumentiert ist.

Der folgende Code zeigt, wie sie den Endpunkt aufzählen und die WASAPI-Schnittstellen abrufen.


```C++
HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}
```



### <a name="controlling-the-volume"></a>Steuern des Volumes

Die `CAudioSessionVolume` Methoden, die die Audiolautstärke steuern, rufen die entsprechenden [**ISimpleAudioVolume-Methoden**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) auf. Ruft beispielsweise `CAudioSessionVolume::SetVolume` [**ISimpleAudioVolume::SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume)auf, wie im folgenden Code gezeigt.


```C++
HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}
```



## <a name="complete-caudiosessionvolume-code"></a>Vollständigen CAudioSessionVolume-Code

Hier ist die vollständige Auflistung der Methoden der `CAudioSessionVolume` -Klasse.


```C++
static const GUID AudioSessionVolumeCtx =
{ 0x2715279f, 0x4139, 0x4ba0, { 0x9c, 0xb1, 0xb3, 0x51, 0xf1, 0xb5, 0x8a, 0x4a } };


CAudioSessionVolume::CAudioSessionVolume(
    UINT uNotificationMessage,
    HWND hwndNotification
    )
    : m_cRef(1),
      m_uNotificationMessage(uNotificationMessage),
      m_hwndNotification(hwndNotification),
      m_bNotificationsEnabled(FALSE),
      m_pAudioSession(NULL),
      m_pSimpleAudioVolume(NULL)
{
}

CAudioSessionVolume::~CAudioSessionVolume()
{
    EnableNotifications(FALSE);

    SafeRelease(&m_pAudioSession);
    SafeRelease(&m_pSimpleAudioVolume);
};


//  Creates an instance of the CAudioSessionVolume object.

/* static */
HRESULT CAudioSessionVolume::CreateInstance(
    UINT uNotificationMessage,
    HWND hwndNotification,
    CAudioSessionVolume **ppAudioSessionVolume
    )
{

    CAudioSessionVolume *pAudioSessionVolume = new (std::nothrow)
        CAudioSessionVolume(uNotificationMessage, hwndNotification);

    if (pAudioSessionVolume == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pAudioSessionVolume->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppAudioSessionVolume = pAudioSessionVolume;
    }
    else
    {
        pAudioSessionVolume->Release();
    }

    return hr;
}


//  Initializes the CAudioSessionVolume object.

HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}

STDMETHODIMP CAudioSessionVolume::QueryInterface(REFIID riid, void **ppv)
{
    static const QITAB qit[] =
    {
        QITABENT(CAudioSessionVolume, IAudioSessionEvents),
        { 0 },
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::Release()
{
    LONG cRef = InterlockedDecrement( &m_cRef );
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}


// Enables or disables notifications from the audio session. For example, the
// application is notified if the user mutes the audio through the system
// volume-control program (Sndvol).

HRESULT CAudioSessionVolume::EnableNotifications(BOOL bEnable)
{
    HRESULT hr = S_OK;

    if (m_hwndNotification == NULL || m_pAudioSession == NULL)
    {
        return E_FAIL;
    }

    if (m_bNotificationsEnabled == bEnable)
    {
        // No change.
        return S_OK;
    }

    if (bEnable)
    {
        hr = m_pAudioSession->RegisterAudioSessionNotification(this);
    }
    else
    {
        hr = m_pAudioSession->UnregisterAudioSessionNotification(this);
    }

    if (SUCCEEDED(hr))
    {
        m_bNotificationsEnabled = bEnable;
    }

    return hr;
}


// Gets the session volume level.

HRESULT CAudioSessionVolume::GetVolume(float *pflVolume)
{
    if ( m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMasterVolume(pflVolume);
    }
}

//  Sets the session volume level.
//
//  flVolume: Ranges from 0 (silent) to 1 (full volume)

HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}


//  Gets the muting state of the session.

HRESULT CAudioSessionVolume::GetMute(BOOL *pbMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMute(pbMute);
    }
}

//  Mutes or unmutes the session audio.

HRESULT CAudioSessionVolume::SetMute(BOOL bMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMute(
            bMute,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}

//  Sets the display name for the session audio.

HRESULT CAudioSessionVolume::SetDisplayName(const WCHAR *wszName)
{
    if (m_pAudioSession == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pAudioSession->SetDisplayName(wszName, NULL);
    }
}


//  Called when the session volume level or muting state changes.
//  (Implements IAudioSessionEvents::OnSimpleVolumeChanged.)

HRESULT CAudioSessionVolume::OnSimpleVolumeChanged(
    float NewVolume,
    BOOL NewMute,
    LPCGUID EventContext
    )
{
    // Check if we should post a message to the application.

    if ( m_bNotificationsEnabled &&
        (*EventContext != AudioSessionVolumeCtx) &&
        (m_hwndNotification != NULL)
        )
    {
        // Notifications are enabled, AND
        // We did not trigger the event ourselves, AND
        // We have a valid window handle.

        // Post the message.
        ::PostMessage(
            m_hwndNotification,
            m_uNotificationMessage,
            *((WPARAM*)(&NewVolume)),  // Coerce the float.
            (LPARAM)NewMute
            );
    }
    return S_OK;
}
```



## <a name="requirements"></a>Anforderungen

MFPlay erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MFPlay für die Audio-/Videowiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
