---
description: In diesem Thema wird beschrieben, wie das audiovolume bei Verwendung von mfplay für die Audiowiedergabe und Videowiedergabe gesteuert wird.
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: Verwalten der Audiositzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5231ca02603279675fabaaac4b96a1cd001906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342658"
---
# <a name="managing-the-audio-session"></a>Verwalten der Audiositzung

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie das audiovolume bei Verwendung von mfplay für die Audiowiedergabe und Videowiedergabe gesteuert wird.

Mfplay bietet die folgenden Methoden, um das audiovolume während der Wiedergabe zu steuern.



| Methode                                                            | BESCHREIBUNG                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [**Imfpmediaplayer:: setbalance**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | Legt das Gleichgewicht zwischen dem linken und dem rechten Kanal fest. |
| [**Imfpmediaplayer:: setstumm**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | Die Audiodatei wird von der Audiodatei abgleichen.                           |
| [**Imfpmediaplayer:: SetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | Legt die Volumeebene fest.                                |



 

Um das Verhalten dieser Methoden zu verstehen, müssen Sie einige Begriffe der Windows-audiositzungs-API (WASAPI) kennen, die die von mfplay verwendete Audiofunktionalität auf niedriger Ebene implementiert.

In WASAPI gehört jeder Audiostream genau einer *Audiositzung* an, bei der es sich um eine Gruppe verwandter Audiodatenströme handelt. In der Regel behält eine Anwendung eine einzelne Audiositzung bei, obwohl Anwendungen mehr als eine Sitzung erstellen können. Das System Volume-Control-Programm (sndvol) zeigt für jede Audiositzung ein Volume-Steuerelement an. Mithilfe von sndvol kann ein Benutzer das Volume einer Audiositzung von außerhalb der Anwendung anpassen. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![Diagramm, das Audiostreams anzeigt, die die volumesteuerung auf dem Weg zu den Referenten durchlaufen Anwendung und sndvol zeigen auf volumesteuerung](images/audio-session.gif)

In MF Play kann ein Medien Element mindestens einen aktiven Audiodatenstrom (in der Regel nur einen) enthalten. Intern verwendet mfplay den [streamingaudiorenderer](streaming-audio-renderer.md) (SAR), um die Audiostreams zu Rendering. Wenn Sie Sie nicht anderweitig konfigurieren, wird die SAR-Datei der standardmäßigen Audiositzung der Anwendung beitreten.

Die mfplay-Audiomethoden Steuern nur die Streams, die zum aktuellen Medien Element gehören. Sie wirken sich nicht auf das Volume für andere Streams aus, die zur gleichen Audiositzung gehören. Im Hinblick auf die WASAPI steuern die MF Play-Methoden die volumeebenen *pro Kanal* und nicht die Master Volume-Ebene. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![das Diagramm ähnelt dem vorherigen, aber der zweite Stream beginnt bei einem Medien Element, und die Anwendung zeigt auf den zweiten Stream und die volumesteuerung.](images/audio-session02.gif)

Es ist wichtig, dass Sie einige Auswirkungen dieses Features von mfplay verstehen. Zuerst kann eine Anwendung das Wiedergabe Volume anpassen, ohne dass sich dies auf andere Audiostreams auswirkt. Sie können diese Funktion verwenden, wenn mfplay das Kreuz Ausblenden von Audiodaten implementiert, indem zwei Instanzen des mfplay-Objekts erstellt und das Volume separat angepasst wird.

Wenn Sie die mfplay-Methode verwenden, um das Volume oder den Zustand stumm zu ändern, werden die Änderungen nicht in sndvol angezeigt. Beispielsweise können Sie [**setstumm**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) zum stumm schalten der Audiodatei aufrufen, aber sndvol zeigt die Sitzung nicht als stumm. Wenn hingegen sndvol verwendet wird, um das Sitzungs Volume anzupassen, werden die Änderungen nicht in den von [**imfpmediaplayer:: getvolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) oder [**imfpmediaplayer:: getstumm**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute)zurückgegebenen Werten widergespiegelt.

Für jede Instanz des mfplay Player-Objekts entspricht die effektive Volumeebene dem *fplayervolume* × *fsessionvolume*, wobei *fplayervolume* der von [**getvolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)zurückgegebene Wert und *fsessionvolume* das Master Volume für die Sitzung ist.

Für einfache Wiedergabe Szenarios ist es möglicherweise besser, die WASAPI zu verwenden, um das audiovolume für die gesamte Sitzung zu steuern, anstatt die mfplay-Methoden zu verwenden.

## <a name="example-code"></a>Beispielcode

Im folgenden finden Sie eine C++-Klasse, die die grundlegenden Aufgaben in WASAPI behandelt:

-   Steuern des Volumes und des stumm Zustands der Sitzung.
-   Benachrichtigungen erhalten, wenn sich das Volume oder der stumm Zustand ändert.

### <a name="class-declaration"></a>Klassendeklaration

Die `CAudioSessionVolume` Klassen Deklaration implementiert die [**iaudiosessionevents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle, die die Rückruf Schnittstelle für audiositzungsereignisse ist.


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



Wenn das `CAudioSessionVolume` Objekt ein audiositzungsereignis empfängt, sendet es eine private Fenster Meldung an die Anwendung. Das Fenster Handle und die Fenster Meldung werden der statischen Methode als Parameter übergeben `CAudioSessionVolume::CreateInstance` .

### <a name="getting-the-wasapi-interface-pointers"></a>Die WASAPI-Schnittstellen Zeiger werden erhalten.

`CAudioSessionVolume` verwendet zwei Haupt-WASAPI-Schnittstellen:

-   [**Iaudiosessioncontrol**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) verwaltet die Audiositzung.
-   [**Isimpleaudiovolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) steuert die Volumeebene und den stumm Zustand der Sitzung.

Um diese Schnittstellen zu erhalten, müssen Sie den audioendpunkt auflisten, der von der SAR-Datei verwendet wird. Ein *audioendpunkt* ist ein Hardware Gerät, das Audiodaten erfasst oder verarbeitet. Bei der Audiowiedergabe ist ein Endpunkt einfach ein Redner oder eine andere Audioausgabe. Standardmäßig verwendet der SAR den Standard Endpunkt für die **econsole** -Geräte Rolle. Eine *Geräte Rolle* ist eine zugewiesene Rolle für einen Endpunkt. Geräte Rollen werden von der [**erole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) -Enumeration angegeben, die in [Core-audioapis](../coreaudio/core-audio-apis-in-windows-vista.md)dokumentiert ist.

Der folgende Code zeigt, wie Sie den Endpunkt auflisten und die WASAPI-Schnittstellen erhalten.


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

Die `CAudioSessionVolume` Methoden, die das audiovolume steuern, werden mit den entsprechenden [**isimpleaudiovolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) -Methoden aufgerufen. Beispielsweise wird `CAudioSessionVolume::SetVolume` [**isimpleaudiovolume:: setmastervolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume)aufgerufen, wie im folgenden Code gezeigt.


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



## <a name="complete-caudiosessionvolume-code"></a>Vervollständigen des caudiosessionvolume-Codes

Im folgenden finden Sie die komplette Liste der Methoden der- `CAudioSessionVolume` Klasse.


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

MF Play erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
