---
description: Audioereignisse für Legacy-Audioanwendungen
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Audioereignisse für Legacy-Audioanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fe99195910b1c1c68c0f3a1b39dd2706dde0be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127676"
---
# <a name="audio-events-for-legacy-audio-applications"></a><span data-ttu-id="9e197-103">Audioereignisse für Legacy-Audioanwendungen</span><span class="sxs-lookup"><span data-stu-id="9e197-103">Audio Events for Legacy Audio Applications</span></span>

<span data-ttu-id="9e197-104">Ältere Audio-APIs, wie z. b. DirectSound, DirectShow und die **waveoutxxx** -Funktionen, ermöglichen Anwendungen das Get und Festlegen der volumeebenen von Audiodatenströmen.</span><span class="sxs-lookup"><span data-stu-id="9e197-104">Legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions enable applications to get and set the volume levels of audio streams.</span></span> <span data-ttu-id="9e197-105">Anwendungen können die Volumen Steuerungsfunktionen in diesen APIs verwenden, um volumeschiebe Regler in ihren Anwendungs Fenstern anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9e197-105">Applications can use the volume-control capabilities in these APIs to display volume sliders in their application windows.</span></span>

<span data-ttu-id="9e197-106">In Windows Vista ermöglicht das System Volume-Control-Programm, sndvol, Benutzern das Steuern der audiovolumeebenen für einzelne Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9e197-106">In Windows Vista, the system volume-control program, Sndvol, allows users to control the audio volume levels for individual applications.</span></span> <span data-ttu-id="9e197-107">Die von Anwendungen angezeigten volumeschiebe Regler müssen mit den entsprechenden volumeschiebe Reglern in sndvol verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9e197-107">The volume sliders that are displayed by applications should be linked to the corresponding volume sliders in Sndvol.</span></span> <span data-ttu-id="9e197-108">Wenn ein Benutzer das Anwendungs Volume über einen volumeschiebe Regler in einem Anwendungsfenster anpasst, wird der entsprechende volumeschiebe Regler in sndvol sofort zur Angabe der neuen Volumeebene verschoben.</span><span class="sxs-lookup"><span data-stu-id="9e197-108">If a user adjusts the application volume through a volume slider in an application window, then the corresponding volume slider in Sndvol immediately moves to indicate the new volume level.</span></span> <span data-ttu-id="9e197-109">Umgekehrt gilt: Wenn der Benutzer das Anwendungs Volume über sndvol anpasst, sollten die volumeschiebe Regler im Anwendungsfenster verschoben werden, um die neue Volumeebene anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9e197-109">Conversely, if the user adjusts the application volume through Sndvol, then the volume sliders in the application window should move to indicate the new volume level.</span></span>

<span data-ttu-id="9e197-110">In Windows Vista reflektiert sndvol sofort Volumenänderungen, die eine Anwendung durch Aufrufe der **idirectsound Buffer:: SetVolume** -Methode oder der **waveoutsetvolume** -Funktion durchführt.</span><span class="sxs-lookup"><span data-stu-id="9e197-110">In Windows Vista, Sndvol immediately reflects volume changes that an application makes through calls to the **IDirectSoundBuffer::SetVolume** method or **waveOutSetVolume** function.</span></span> <span data-ttu-id="9e197-111">Eine Legacy-Audio-API, z. b. DirectSound oder die **waveoutxxx** -Funktionen, bietet aber keine Möglichkeit, eine Anwendung zu benachrichtigen, wenn der Benutzer das Anwendungs Volume über sndvol ändert.</span><span class="sxs-lookup"><span data-stu-id="9e197-111">However, a legacy audio API such as DirectSound or the **waveOutXxx** functions provides no means to notify an application when the user changes the application volume through Sndvol.</span></span> <span data-ttu-id="9e197-112">Wenn eine Anwendung einen volumeschiebe Regler anzeigt, aber keine Benachrichtigungen zu volumeänderungen empfängt, kann der Schieberegler keine Änderungen widerspiegeln, die vom Benutzer in sndvol vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="9e197-112">If an application displays a volume slider but does not receive notifications of volume changes, then the slider will fail to reflect changes made by the user in Sndvol.</span></span> <span data-ttu-id="9e197-113">Um das entsprechende Verhalten zu implementieren, muss der Anwendungs-Designer den Mangel an Benachrichtigungen durch die Legacy-audioapi auf irgendeine Weise kompensieren.</span><span class="sxs-lookup"><span data-stu-id="9e197-113">To implement the appropriate behavior, the application designer must somehow compensate for the lack of notifications by the legacy audio API.</span></span>

<span data-ttu-id="9e197-114">Eine mögliche Lösung ist, dass die Anwendung einen Zeitgeber festlegen kann, um Sie in regelmäßigen Abständen daran zu erinnern, den volumegrad zu überprüfen</span><span class="sxs-lookup"><span data-stu-id="9e197-114">One solution might be for the application to set a timer to periodically remind it to check the volume level to see if it has changed.</span></span>

<span data-ttu-id="9e197-115">Eine elegantere Lösung besteht darin, dass die Anwendung die Ereignis Benachrichtigungsfunktionen der kernaudioapis verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e197-115">A more elegant solution is for the application to use the event notification capabilities of the core audio APIs.</span></span> <span data-ttu-id="9e197-116">Insbesondere kann die Anwendung eine [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle registrieren, um Rückrufe zu empfangen, wenn volumeänderungen oder andere Arten von Audioereignissen auftreten.</span><span class="sxs-lookup"><span data-stu-id="9e197-116">In particular, the application can register an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to receive callbacks when volume changes or other types of audio events occur.</span></span> <span data-ttu-id="9e197-117">Wenn das Volume geändert wird, kann die volumeänderungs-Rückruf Routine den volumeschiebe Regler der Anwendung sofort aktualisieren, um die Änderung widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="9e197-117">When the volume changes, the volume-change callback routine can immediately update the application's volume slider to reflect the change.</span></span>

<span data-ttu-id="9e197-118">Im folgenden Codebeispiel wird gezeigt, wie eine Anwendung registriert werden kann, um Benachrichtigungen über volumeänderungen und andere Audioereignisse zu empfangen:</span><span class="sxs-lookup"><span data-stu-id="9e197-118">The following code example shows how an application can register to receive notifications of volume changes and other audio events:</span></span>


```C++
//-----------------------------------------------------------
// Register the application to receive notifications when the
// volume level changes on the default process-specific audio
// session (with session GUID value GUID_NULL) on the audio
// endpoint device with the specified data-flow direction
// (eRender or eCapture) and device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class AudioVolumeEvents
{
    HRESULT _hrStatus;
    IAudioSessionManager *_pManager;
    IAudioSessionControl *_pControl;
    IAudioSessionEvents *_pAudioEvents;
public:
    AudioVolumeEvents(EDataFlow, ERole, IAudioSessionEvents*);
    ~AudioVolumeEvents();
    HRESULT GetStatus() { return _hrStatus; };
};

// Constructor
AudioVolumeEvents::AudioVolumeEvents(EDataFlow flow, ERole role,
                                     IAudioSessionEvents *pAudioEvents)
{
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    _hrStatus = S_OK;
    _pManager = NULL;
    _pControl = NULL;
    _pAudioEvents = pAudioEvents;

    if (_pAudioEvents == NULL)
    {
        _hrStatus = E_POINTER;
        return;
    }

    _pAudioEvents->AddRef();

    // Get the enumerator for the audio endpoint devices
    // on this system.
    _hrStatus = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                                 NULL, CLSCTX_INPROC_SERVER,
                                 __uuidof(IMMDeviceEnumerator),
                                 (void**)&pEnumerator);
    EXIT_ON_ERROR(_hrStatus)

    // Get the audio endpoint device with the specified data-flow
    // direction (eRender or eCapture) and device role.
    _hrStatus = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                                     &pDevice);
    EXIT_ON_ERROR(_hrStatus)

    // Get the session manager for the endpoint device.
    _hrStatus = pDevice->Activate(__uuidof(IAudioSessionManager),
                                  CLSCTX_INPROC_SERVER, NULL,
                                  (void**)&_pManager);
    EXIT_ON_ERROR(_hrStatus)

    // Get the control interface for the process-specific audio
    // session with session GUID = GUID_NULL. This is the session
    // that an audio stream for a DirectSound, DirectShow, waveOut,
    // or PlaySound application stream belongs to by default.
    _hrStatus = _pManager->GetAudioSessionControl(NULL, 0, &_pControl);
    EXIT_ON_ERROR(_hrStatus)

    _hrStatus = _pControl->RegisterAudioSessionNotification(_pAudioEvents);
    EXIT_ON_ERROR(_hrStatus)

Exit:
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
}

// Destructor
AudioVolumeEvents::~AudioVolumeEvents()
{
    if (_pControl != NULL)
    {
        _pControl->UnregisterAudioSessionNotification(_pAudioEvents);
    }
    SAFE_RELEASE(_pManager)
    SAFE_RELEASE(_pControl)
    SAFE_RELEASE(_pAudioEvents)
};
```



<span data-ttu-id="9e197-119">Im vorangehenden Codebeispiel wird eine Klasse mit dem Namen audiovolumeevents implementiert.</span><span class="sxs-lookup"><span data-stu-id="9e197-119">The preceding code example implements a class named AudioVolumeEvents.</span></span> <span data-ttu-id="9e197-120">Während der Programm Initialisierung aktiviert die Audioanwendung audioereignisbenachrichtigungen durch Erstellen eines audiovolumeevents-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9e197-120">During program initialization, the audio application enables audio-event notifications by creating an AudioVolumeEvents object.</span></span> <span data-ttu-id="9e197-121">Der Konstruktor für diese Klasse nimmt drei Eingabeparameter an:</span><span class="sxs-lookup"><span data-stu-id="9e197-121">The constructor for this class takes three input parameters:</span></span>

-   <span data-ttu-id="9e197-122">*Flow*– die Datenfluss Richtung des [audioendpunktgeräts](audio-endpoint-devices.md) (ein [**edataflow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) -Enumerationswert).</span><span class="sxs-lookup"><span data-stu-id="9e197-122">*flow*—the data-flow direction of the [audio endpoint device](audio-endpoint-devices.md) (an [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) enumeration value).</span></span>
-   <span data-ttu-id="9e197-123">*Role*– die aktuelle [Geräte Rolle](device-roles.md) des Endpunkt Geräts (ein [**erole-Enumerationswert**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).</span><span class="sxs-lookup"><span data-stu-id="9e197-123">*role*—the current [device role](device-roles.md) of the endpoint device (an [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration value).</span></span>
-   <span data-ttu-id="9e197-124">*paudioevents*– Zeiger auf ein Objekt (eine [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstellen Instanz), das einen Satz von Rückruf Routinen enthält, die von der Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e197-124">*pAudioEvents*—pointer to an object (an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface instance) that contains a set of callback routines that are implemented by the application.</span></span>

<span data-ttu-id="9e197-125">Der-Konstruktor stellt den Flow und die Rollen Werte als Eingabeparameter für die [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="9e197-125">The constructor supplies the flow and role values as input parameters to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method.</span></span> <span data-ttu-id="9e197-126">Die-Methode erstellt ein [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Objekt, das das audioendpunktgerät mit der angegebenen Datenfluss Richtung und der angegebenen Geräte Rolle kapselt.</span><span class="sxs-lookup"><span data-stu-id="9e197-126">The method creates an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object that encapsulates the audio endpoint device with the specified data-flow direction and device role.</span></span>

<span data-ttu-id="9e197-127">Die Anwendung implementiert das Objekt, auf das *paudioevents* zeigt.</span><span class="sxs-lookup"><span data-stu-id="9e197-127">The application implements the object pointed to by *pAudioEvents*.</span></span> <span data-ttu-id="9e197-128">(Die-Implementierung wird im vorangehenden Codebeispiel nicht gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e197-128">(The implementation is not shown in the preceding code example.</span></span> <span data-ttu-id="9e197-129">Ein Codebeispiel, in dem eine **iaudiosessionevents** -Schnittstelle implementiert wird, finden Sie unter [audiositzungsereignisse](audio-session-events.md).) Jede Methode in dieser Schnittstelle empfängt Benachrichtigungen zu einem bestimmten Typ von Audioereignis.</span><span class="sxs-lookup"><span data-stu-id="9e197-129">For a code example that implements an **IAudioSessionEvents** interface, see [Audio Session Events](audio-session-events.md).) Each method in this interface receives notifications of a particular type of audio event.</span></span> <span data-ttu-id="9e197-130">Wenn die Anwendung nicht an einem bestimmten Ereignistyp interessiert ist, sollte die-Methode für diesen Ereignistyp nichts Unternehmen, sondern "S OK" zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="9e197-130">If the application is not interested in a particular event type, then the method for that event type should do nothing but return S\_OK.</span></span>

<span data-ttu-id="9e197-131">Die [**iaudiosessionevents:: onsimplevolumechaning**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) -Methode empfängt Benachrichtigungen zu volumeänderungen.</span><span class="sxs-lookup"><span data-stu-id="9e197-131">The [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) method receives notifications of volume changes.</span></span> <span data-ttu-id="9e197-132">In der Regel wird mit dieser Methode der volumeschiebe Regler der Anwendung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9e197-132">Typically, this method updates the application's volume slider.</span></span>

<span data-ttu-id="9e197-133">Im vorangehenden Codebeispiel registriert der Konstruktor für die audiovolumeevents-Klasse Benachrichtigungen für die prozessspezifische [Audiositzung](audio-sessions.md) , die durch den Sitzungs-GUID-Wert GUID \_ null identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9e197-133">In the preceding code example, the constructor for the AudioVolumeEvents class registers for notifications on the process-specific [audio session](audio-sessions.md) that is identified by session GUID value GUID\_NULL.</span></span> <span data-ttu-id="9e197-134">Standardmäßig weisen ältere Audio-APIs, wie z. b. DirectSound, DirectShow und die **waveoutxxx** -Funktionen, ihre Streams dieser Sitzung zu.</span><span class="sxs-lookup"><span data-stu-id="9e197-134">By default, legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions assign their streams to this session.</span></span> <span data-ttu-id="9e197-135">Eine DirectSound-oder DirectShow-Anwendung kann jedoch als Option das Standardverhalten überschreiben und die Streams einer prozessübergreifenden Sitzung oder einer Sitzung zuweisen, die durch einen anderen GUID-Wert als GUID NULL identifiziert wird \_ .</span><span class="sxs-lookup"><span data-stu-id="9e197-135">However, a DirectSound or DirectShow application can, as an option, override the default behavior and assign its streams to a cross-process session or to a session that is identified by a GUID value other than GUID\_NULL.</span></span> <span data-ttu-id="9e197-136">(Zurzeit wird kein Mechanismus für eine **waveoutxxx** -Anwendung bereitgestellt, um das Standardverhalten auf ähnliche Weise zu überschreiben.) Ein Codebeispiel für eine DirectShow-Anwendung mit diesem Verhalten finden Sie unter [Geräte Rollen für DirectShow-Anwendungen](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9e197-136">(No mechanism is currently provided for a **waveOutXxx** application to override the default behavior in a similar manner.) For a code example of a DirectShow application with this behavior, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="9e197-137">Um eine solche Anwendung zu integrieren, können Sie den Konstruktor im vorangehenden Codebeispiel so ändern, dass zwei zusätzliche Eingabeparameter akzeptiert werden – eine Sitzungs-GUID und ein Flag, mit dem angegeben wird, ob die zu überwachende Sitzung eine prozessübergreifende oder prozessspezifische Sitzung ist.</span><span class="sxs-lookup"><span data-stu-id="9e197-137">To accommodate such an application, you can modify the constructor in the preceding code example to accept two additional input parameters—a session GUID and a flag to indicate whether the session that is to be monitored is a cross-process or process-specific session.</span></span> <span data-ttu-id="9e197-138">Übergeben Sie diese Parameter an den Aufrufen der [**iaudiosessionmanager:: getaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) -Methode im-Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="9e197-138">Pass these parameters to the call to the [**IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) method in the constructor.</span></span>

<span data-ttu-id="9e197-139">Nachdem der Konstruktor die [**iaudiosessioncontrol:: registeraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) -Methode aufgerufen hat, um Benachrichtigungen zu registrieren, empfängt die Anwendung weiterhin nur dann Benachrichtigungen, wenn entweder die [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle oder die [**iaudiosessionmanager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) -Schnittstelle vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e197-139">After the constructor calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register for notifications, the application continues to receive notifications for only as long as either the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) or [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface exists.</span></span> <span data-ttu-id="9e197-140">Das audiovolumeevents-Objekt im vorangehenden Codebeispiel enthält Verweise auf diese Schnittstellen, bis der debugtor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9e197-140">The AudioVolumeEvents object in the preceding code example holds references to these interfaces until its destructor is called.</span></span> <span data-ttu-id="9e197-141">Durch dieses Verhalten wird sichergestellt, dass die Anwendung für die Lebensdauer des audiovolumeevents-Objekts weiterhin Benachrichtigungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="9e197-141">This behavior ensures that the application will continue to receive notifications for the lifetime of the AudioVolumeEvents object.</span></span>

<span data-ttu-id="9e197-142">Anstatt ein Audiogerät basierend auf seiner Geräte Rolle implizit auszuwählen, kann eine DirectSound-oder ältere Windows-Multimediaanwendung es dem Benutzer ermöglichen, ein Gerät explizit aus einer Liste der verfügbaren Geräte auszuwählen, die anhand seiner anzeigen Amen identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9e197-142">Instead of implicitly selecting an audio device based on its device role, a DirectSound or legacy Windows multimedia application might allow the user to explicitly select a device from a list of available devices that are identified by their friendly names.</span></span> <span data-ttu-id="9e197-143">Um dieses Verhalten zu unterstützen, muss das vorangehende Codebeispiel so geändert werden, dass audioereignisbenachrichtigungen für das ausgewählte Gerät generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e197-143">To support this behavior, the preceding code example must be modified to generate audio-event notifications for the selected device.</span></span> <span data-ttu-id="9e197-144">Es sind zwei Änderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e197-144">Two modifications are required.</span></span> <span data-ttu-id="9e197-145">Ändern Sie zunächst die Konstruktordefinition so, dass Sie eine [Endpunkt-ID-Zeichenfolge](endpoint-id-strings.md) als Eingabeparameter akzeptiert (anstelle des Flows und der Rollen Parameter im Codebeispiel).</span><span class="sxs-lookup"><span data-stu-id="9e197-145">First, change the constructor definition to accept an [endpoint ID string](endpoint-id-strings.md) as an input parameter (in place of the flow and role parameters in the code example).</span></span> <span data-ttu-id="9e197-146">Diese Zeichenfolge identifiziert das audioendpunktgerät, das dem ausgewählten DirectSound-oder Legacy Wellenform-Gerät entspricht.</span><span class="sxs-lookup"><span data-stu-id="9e197-146">This string identifies the audio endpoint device that corresponds to the selected DirectSound or legacy waveform device.</span></span> <span data-ttu-id="9e197-147">Ersetzen Sie anschließend den Aufrufen der Methode [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) durch einen Aufrufen der Methode [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="9e197-147">Second, replace the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method with a call to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="9e197-148">Der **getdevice** -Befehl nimmt die Endpunkt-ID-Zeichenfolge als Eingabeparameter an und erstellt eine Instanz des Endpunkt Geräts, das von der Zeichenfolge identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9e197-148">The **GetDevice** call takes the endpoint ID string as an input parameter and creates an instance of the endpoint device that is identified by the string.</span></span>

<span data-ttu-id="9e197-149">Die Methode zum Abrufen der Endpunkt-ID-Zeichenfolge für ein DirectSound-Gerät oder ein Legacy-Wellenform-Gerät lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="9e197-149">The technique for obtaining the endpoint ID string for a DirectSound device or legacy waveform device is as follows.</span></span>

<span data-ttu-id="9e197-150">Zuerst stellt DirectSound während der Geräte Enumeration die Endpunkt-ID-Zeichenfolge für jedes aufgezählte Gerät bereit.</span><span class="sxs-lookup"><span data-stu-id="9e197-150">First, during device enumeration, DirectSound supplies the endpoint ID string for each enumerated device.</span></span> <span data-ttu-id="9e197-151">Um mit der Geräte Enumeration zu beginnen, übergibt die Anwendung einen Rückruf Funktionszeiger als Eingabeparameter an die Funktion **directsoundcreate** oder **directsoundcaptuneu** .</span><span class="sxs-lookup"><span data-stu-id="9e197-151">To begin device enumeration, the application passes a callback function pointer as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span> <span data-ttu-id="9e197-152">Die Definition der Rückruffunktion lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9e197-152">The definition of the callback function is:</span></span>


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



<span data-ttu-id="9e197-153">In Windows Vista zeigt der *lpcstrauch Module* -Parameter auf die Endpunkt-ID-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9e197-153">In Windows Vista, the *lpcstrModule* parameter points to the endpoint ID string.</span></span> <span data-ttu-id="9e197-154">(In früheren Versionen von Windows, einschließlich Windows Server 2003, Windows XP und Windows 2000, verweist der *lpcstrauch Module* -Parameter auf den Namen des Treiber Moduls für das Gerät.) Der *lpcstraudescription* -Parameter verweist auf eine Zeichenfolge, die den anzeigen amen des Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="9e197-154">(In earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000, the *lpcstrModule* parameter points to the name of the driver module for the device.) The *lpcstrDescription* parameter points to a string that contains the friendly name of the device.</span></span> <span data-ttu-id="9e197-155">Weitere Informationen zur DirectSound-Geräte Enumeration finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="9e197-155">For more information about DirectSound device enumeration, see the Windows SDK documentation.</span></span>

<span data-ttu-id="9e197-156">Zweitens: zum Abrufen der Endpunkt-ID-Zeichenfolge für ein älteres Wellenform-Gerät verwenden Sie die **waveoutmessage** -Funktion oder die **waveinmessage** -Funktion, um eine drv \_ -queryfunctioninstanceid-Meldung an den Wellenform-Gerätetreiber zu senden.</span><span class="sxs-lookup"><span data-stu-id="9e197-156">Second, to obtain the endpoint ID string for a legacy waveform device, use the **waveOutMessage** or **waveInMessage** function to send a DRV\_QUERYFUNCTIONINSTANCEID message to the waveform device driver.</span></span> <span data-ttu-id="9e197-157">Ein Codebeispiel, in dem die Verwendung dieser Nachricht veranschaulicht wird, finden Sie unter [Geräte Rollen für ältere Windows-Multimediaanwendungen](device-roles-for-legacy-windows-multimedia-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9e197-157">For a code example that shows the use of this message, see [Device Roles for Legacy Windows Multimedia Applications](device-roles-for-legacy-windows-multimedia-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e197-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e197-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e197-159">Interoperabilität mit Legacy-audioapis</span><span class="sxs-lookup"><span data-stu-id="9e197-159">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



