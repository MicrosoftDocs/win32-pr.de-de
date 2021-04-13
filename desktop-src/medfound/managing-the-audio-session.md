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
# <a name="managing-the-audio-session"></a><span data-ttu-id="09b38-103">Verwalten der Audiositzung</span><span class="sxs-lookup"><span data-stu-id="09b38-103">Managing the Audio Session</span></span>

<span data-ttu-id="09b38-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="09b38-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="09b38-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="09b38-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="09b38-106">\]</span><span class="sxs-lookup"><span data-stu-id="09b38-106">\]</span></span>

<span data-ttu-id="09b38-107">In diesem Thema wird beschrieben, wie das audiovolume bei Verwendung von mfplay für die Audiowiedergabe und Videowiedergabe gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="09b38-107">This topic describes how to control audio volume when using MFPlay for audio/video playback.</span></span>

<span data-ttu-id="09b38-108">Mfplay bietet die folgenden Methoden, um das audiovolume während der Wiedergabe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="09b38-108">MFPlay provides the following methods to control the audio volume during playback.</span></span>



| <span data-ttu-id="09b38-109">Methode</span><span class="sxs-lookup"><span data-stu-id="09b38-109">Method</span></span>                                                            | <span data-ttu-id="09b38-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09b38-110">Description</span></span>                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="09b38-111">**Imfpmediaplayer:: setbalance**</span><span class="sxs-lookup"><span data-stu-id="09b38-111">**IMFPMediaPlayer::SetBalance**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | <span data-ttu-id="09b38-112">Legt das Gleichgewicht zwischen dem linken und dem rechten Kanal fest.</span><span class="sxs-lookup"><span data-stu-id="09b38-112">Sets the balance between the left and right channels.</span></span> |
| [<span data-ttu-id="09b38-113">**Imfpmediaplayer:: setstumm**</span><span class="sxs-lookup"><span data-stu-id="09b38-113">**IMFPMediaPlayer::SetMute**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | <span data-ttu-id="09b38-114">Die Audiodatei wird von der Audiodatei abgleichen.</span><span class="sxs-lookup"><span data-stu-id="09b38-114">Mutes or unmutes the audio.</span></span>                           |
| [<span data-ttu-id="09b38-115">**Imfpmediaplayer:: SetVolume**</span><span class="sxs-lookup"><span data-stu-id="09b38-115">**IMFPMediaPlayer::SetVolume**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | <span data-ttu-id="09b38-116">Legt die Volumeebene fest.</span><span class="sxs-lookup"><span data-stu-id="09b38-116">Sets the volume level.</span></span>                                |



 

<span data-ttu-id="09b38-117">Um das Verhalten dieser Methoden zu verstehen, müssen Sie einige Begriffe der Windows-audiositzungs-API (WASAPI) kennen, die die von mfplay verwendete Audiofunktionalität auf niedriger Ebene implementiert.</span><span class="sxs-lookup"><span data-stu-id="09b38-117">To understand the behavior of these methods, you must know some terminology from the Windows Audio Session API (WASAPI), which implements the low-level audio functionality used by MFPlay.</span></span>

<span data-ttu-id="09b38-118">In WASAPI gehört jeder Audiostream genau einer *Audiositzung* an, bei der es sich um eine Gruppe verwandter Audiodatenströme handelt.</span><span class="sxs-lookup"><span data-stu-id="09b38-118">In WASAPI, every audio stream belongs to exactly one *audio session*, which is a group of related audio streams.</span></span> <span data-ttu-id="09b38-119">In der Regel behält eine Anwendung eine einzelne Audiositzung bei, obwohl Anwendungen mehr als eine Sitzung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="09b38-119">Typically, an application maintains a single audio session, although applications can create more than one session.</span></span> <span data-ttu-id="09b38-120">Das System Volume-Control-Programm (sndvol) zeigt für jede Audiositzung ein Volume-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="09b38-120">The system volume-control program (Sndvol) displays a volume control for each audio session.</span></span> <span data-ttu-id="09b38-121">Mithilfe von sndvol kann ein Benutzer das Volume einer Audiositzung von außerhalb der Anwendung anpassen.</span><span class="sxs-lookup"><span data-stu-id="09b38-121">Through Sndvol, a user can adjust the volume of an audio session from outside of the application.</span></span> <span data-ttu-id="09b38-122">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="09b38-122">The following image illustrates this process.</span></span>

![Diagramm, das Audiostreams anzeigt, die die volumesteuerung auf dem Weg zu den Referenten durchlaufen Anwendung und sndvol zeigen auf volumesteuerung](images/audio-session.gif)

<span data-ttu-id="09b38-124">In MF Play kann ein Medien Element mindestens einen aktiven Audiodatenstrom (in der Regel nur einen) enthalten.</span><span class="sxs-lookup"><span data-stu-id="09b38-124">In MFPlay, a media item can have one or more active audio streams (typically only one).</span></span> <span data-ttu-id="09b38-125">Intern verwendet mfplay den [streamingaudiorenderer](streaming-audio-renderer.md) (SAR), um die Audiostreams zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="09b38-125">Internally, MFPlay uses the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) to render the audio streams.</span></span> <span data-ttu-id="09b38-126">Wenn Sie Sie nicht anderweitig konfigurieren, wird die SAR-Datei der standardmäßigen Audiositzung der Anwendung beitreten.</span><span class="sxs-lookup"><span data-stu-id="09b38-126">Unless you configure it otherwise, the SAR joins the application's default audio session.</span></span>

<span data-ttu-id="09b38-127">Die mfplay-Audiomethoden Steuern nur die Streams, die zum aktuellen Medien Element gehören.</span><span class="sxs-lookup"><span data-stu-id="09b38-127">The MFPlay audio methods control only the streams that belong to the current media item.</span></span> <span data-ttu-id="09b38-128">Sie wirken sich nicht auf das Volume für andere Streams aus, die zur gleichen Audiositzung gehören.</span><span class="sxs-lookup"><span data-stu-id="09b38-128">They do not affect the volume for any other streams that belong to the same audio session.</span></span> <span data-ttu-id="09b38-129">Im Hinblick auf die WASAPI steuern die MF Play-Methoden die volumeebenen *pro Kanal* und nicht die Master Volume-Ebene.</span><span class="sxs-lookup"><span data-stu-id="09b38-129">In terms of WASAPI, the MFPlay methods control the *per-channel* volume levels, not the master volume level.</span></span> <span data-ttu-id="09b38-130">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="09b38-130">The following image illustrates this process.</span></span>

![das Diagramm ähnelt dem vorherigen, aber der zweite Stream beginnt bei einem Medien Element, und die Anwendung zeigt auf den zweiten Stream und die volumesteuerung.](images/audio-session02.gif)

<span data-ttu-id="09b38-132">Es ist wichtig, dass Sie einige Auswirkungen dieses Features von mfplay verstehen.</span><span class="sxs-lookup"><span data-stu-id="09b38-132">It is important to understand some implications of this feature of MFPlay.</span></span> <span data-ttu-id="09b38-133">Zuerst kann eine Anwendung das Wiedergabe Volume anpassen, ohne dass sich dies auf andere Audiostreams auswirkt.</span><span class="sxs-lookup"><span data-stu-id="09b38-133">First, an application can adjust the playback volume without affecting other audio streams.</span></span> <span data-ttu-id="09b38-134">Sie können diese Funktion verwenden, wenn mfplay das Kreuz Ausblenden von Audiodaten implementiert, indem zwei Instanzen des mfplay-Objekts erstellt und das Volume separat angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="09b38-134">You could use this feature if MFPlay to implement audio cross-fading, by creating two instances of the MFPlay object and adjusting the volume separately.</span></span>

<span data-ttu-id="09b38-135">Wenn Sie die mfplay-Methode verwenden, um das Volume oder den Zustand stumm zu ändern, werden die Änderungen nicht in sndvol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="09b38-135">If you use MFPlay methods to change the volume or mute state, the changes do not appear in Sndvol.</span></span> <span data-ttu-id="09b38-136">Beispielsweise können Sie [**setstumm**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) zum stumm schalten der Audiodatei aufrufen, aber sndvol zeigt die Sitzung nicht als stumm.</span><span class="sxs-lookup"><span data-stu-id="09b38-136">For example, you can call [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) to mute the audio, but Sndvol will not show the session as muted.</span></span> <span data-ttu-id="09b38-137">Wenn hingegen sndvol verwendet wird, um das Sitzungs Volume anzupassen, werden die Änderungen nicht in den von [**imfpmediaplayer:: getvolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) oder [**imfpmediaplayer:: getstumm**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute)zurückgegebenen Werten widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="09b38-137">Conversely, if SndVol is used to adjust the session volume, the changes are not reflected in the values returned by [**IMFPMediaPlayer::GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) or [**IMFPMediaPlayer::GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span></span>

<span data-ttu-id="09b38-138">Für jede Instanz des mfplay Player-Objekts entspricht die effektive Volumeebene dem *fplayervolume* × *fsessionvolume*, wobei *fplayervolume* der von [**getvolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)zurückgegebene Wert und *fsessionvolume* das Master Volume für die Sitzung ist.</span><span class="sxs-lookup"><span data-stu-id="09b38-138">For each instance of the MFPlay player object, the effective volume level equals *fPlayerVolume* × *fSessionVolume*, where *fPlayerVolume* is the value returned by [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume), and *fSessionVolume* is the master volume for the session.</span></span>

<span data-ttu-id="09b38-139">Für einfache Wiedergabe Szenarios ist es möglicherweise besser, die WASAPI zu verwenden, um das audiovolume für die gesamte Sitzung zu steuern, anstatt die mfplay-Methoden zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="09b38-139">For simple playback scenarios, it might be preferable to use the WASAPI to control the audio volume for the entire session, rather than use the MFPlay methods.</span></span>

## <a name="example-code"></a><span data-ttu-id="09b38-140">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="09b38-140">Example Code</span></span>

<span data-ttu-id="09b38-141">Im folgenden finden Sie eine C++-Klasse, die die grundlegenden Aufgaben in WASAPI behandelt:</span><span class="sxs-lookup"><span data-stu-id="09b38-141">What follows is a C++ class that handles the basic tasks in WASAPI:</span></span>

-   <span data-ttu-id="09b38-142">Steuern des Volumes und des stumm Zustands der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="09b38-142">Controlling the volume and mute state for the session.</span></span>
-   <span data-ttu-id="09b38-143">Benachrichtigungen erhalten, wenn sich das Volume oder der stumm Zustand ändert.</span><span class="sxs-lookup"><span data-stu-id="09b38-143">Getting notifications whenever the volume or mute state change.</span></span>

### <a name="class-declaration"></a><span data-ttu-id="09b38-144">Klassendeklaration</span><span class="sxs-lookup"><span data-stu-id="09b38-144">Class Declaration</span></span>

<span data-ttu-id="09b38-145">Die `CAudioSessionVolume` Klassen Deklaration implementiert die [**iaudiosessionevents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle, die die Rückruf Schnittstelle für audiositzungsereignisse ist.</span><span class="sxs-lookup"><span data-stu-id="09b38-145">The `CAudioSessionVolume` class declaration implements the [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, which is the callback interface for audio session events.</span></span>


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



<span data-ttu-id="09b38-146">Wenn das `CAudioSessionVolume` Objekt ein audiositzungsereignis empfängt, sendet es eine private Fenster Meldung an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="09b38-146">When the `CAudioSessionVolume` object receives an audio session event, it posts a private window message to the application.</span></span> <span data-ttu-id="09b38-147">Das Fenster Handle und die Fenster Meldung werden der statischen Methode als Parameter übergeben `CAudioSessionVolume::CreateInstance` .</span><span class="sxs-lookup"><span data-stu-id="09b38-147">The window handle and the window message are given as parameters to the static `CAudioSessionVolume::CreateInstance` method.</span></span>

### <a name="getting-the-wasapi-interface-pointers"></a><span data-ttu-id="09b38-148">Die WASAPI-Schnittstellen Zeiger werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="09b38-148">Getting the WASAPI Interface Pointers</span></span>

<span data-ttu-id="09b38-149">`CAudioSessionVolume` verwendet zwei Haupt-WASAPI-Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="09b38-149">`CAudioSessionVolume` uses two main WASAPI interfaces:</span></span>

-   <span data-ttu-id="09b38-150">[**Iaudiosessioncontrol**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) verwaltet die Audiositzung.</span><span class="sxs-lookup"><span data-stu-id="09b38-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) manages the audio session.</span></span>
-   <span data-ttu-id="09b38-151">[**Isimpleaudiovolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) steuert die Volumeebene und den stumm Zustand der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="09b38-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controls the volume level and mute state of the session.</span></span>

<span data-ttu-id="09b38-152">Um diese Schnittstellen zu erhalten, müssen Sie den audioendpunkt auflisten, der von der SAR-Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09b38-152">To get these interfaces, you must enumerate the audio endpoint that is used by the SAR.</span></span> <span data-ttu-id="09b38-153">Ein *audioendpunkt* ist ein Hardware Gerät, das Audiodaten erfasst oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="09b38-153">An *audio endpoint* is a hardware device that captures or consumes audio data.</span></span> <span data-ttu-id="09b38-154">Bei der Audiowiedergabe ist ein Endpunkt einfach ein Redner oder eine andere Audioausgabe.</span><span class="sxs-lookup"><span data-stu-id="09b38-154">For audio playback, an endpoint is simply a speaker or other audio output.</span></span> <span data-ttu-id="09b38-155">Standardmäßig verwendet der SAR den Standard Endpunkt für die **econsole** -Geräte Rolle.</span><span class="sxs-lookup"><span data-stu-id="09b38-155">By default, the SAR uses the default endpoint for the **eConsole** device role.</span></span> <span data-ttu-id="09b38-156">Eine *Geräte Rolle* ist eine zugewiesene Rolle für einen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="09b38-156">A *device role* is an assigned role for an endpoint.</span></span> <span data-ttu-id="09b38-157">Geräte Rollen werden von der [**erole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) -Enumeration angegeben, die in [Core-audioapis](../coreaudio/core-audio-apis-in-windows-vista.md)dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="09b38-157">Device roles are specified by the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration, which is documented in [Core Audio APIs](../coreaudio/core-audio-apis-in-windows-vista.md).</span></span>

<span data-ttu-id="09b38-158">Der folgende Code zeigt, wie Sie den Endpunkt auflisten und die WASAPI-Schnittstellen erhalten.</span><span class="sxs-lookup"><span data-stu-id="09b38-158">The following code shows how to enumerate the endpoint and get the WASAPI interfaces.</span></span>


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



### <a name="controlling-the-volume"></a><span data-ttu-id="09b38-159">Steuern des Volumes</span><span class="sxs-lookup"><span data-stu-id="09b38-159">Controlling the Volume</span></span>

<span data-ttu-id="09b38-160">Die `CAudioSessionVolume` Methoden, die das audiovolume steuern, werden mit den entsprechenden [**isimpleaudiovolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) -Methoden aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="09b38-160">The `CAudioSessionVolume` methods that control the audio volume call the equivalent [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) methods.</span></span> <span data-ttu-id="09b38-161">Beispielsweise wird `CAudioSessionVolume::SetVolume` [**isimpleaudiovolume:: setmastervolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume)aufgerufen, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="09b38-161">For example, `CAudioSessionVolume::SetVolume` calls [**ISimpleAudioVolume::SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), as shown in the following code.</span></span>


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



## <a name="complete-caudiosessionvolume-code"></a><span data-ttu-id="09b38-162">Vervollständigen des caudiosessionvolume-Codes</span><span class="sxs-lookup"><span data-stu-id="09b38-162">Complete CAudioSessionVolume Code</span></span>

<span data-ttu-id="09b38-163">Im folgenden finden Sie die komplette Liste der Methoden der- `CAudioSessionVolume` Klasse.</span><span class="sxs-lookup"><span data-stu-id="09b38-163">Here is the complete listing for the methods of the `CAudioSessionVolume` class.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="09b38-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09b38-164">Requirements</span></span>

<span data-ttu-id="09b38-165">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="09b38-165">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09b38-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09b38-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09b38-167">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="09b38-167">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
