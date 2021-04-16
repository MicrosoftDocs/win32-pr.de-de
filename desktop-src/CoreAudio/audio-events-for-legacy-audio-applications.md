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
# <a name="audio-events-for-legacy-audio-applications"></a>Audioereignisse für Legacy-Audioanwendungen

Ältere Audio-APIs, wie z. b. DirectSound, DirectShow und die **waveoutxxx** -Funktionen, ermöglichen Anwendungen das Get und Festlegen der volumeebenen von Audiodatenströmen. Anwendungen können die Volumen Steuerungsfunktionen in diesen APIs verwenden, um volumeschiebe Regler in ihren Anwendungs Fenstern anzuzeigen.

In Windows Vista ermöglicht das System Volume-Control-Programm, sndvol, Benutzern das Steuern der audiovolumeebenen für einzelne Anwendungen. Die von Anwendungen angezeigten volumeschiebe Regler müssen mit den entsprechenden volumeschiebe Reglern in sndvol verknüpft werden. Wenn ein Benutzer das Anwendungs Volume über einen volumeschiebe Regler in einem Anwendungsfenster anpasst, wird der entsprechende volumeschiebe Regler in sndvol sofort zur Angabe der neuen Volumeebene verschoben. Umgekehrt gilt: Wenn der Benutzer das Anwendungs Volume über sndvol anpasst, sollten die volumeschiebe Regler im Anwendungsfenster verschoben werden, um die neue Volumeebene anzugeben.

In Windows Vista reflektiert sndvol sofort Volumenänderungen, die eine Anwendung durch Aufrufe der **idirectsound Buffer:: SetVolume** -Methode oder der **waveoutsetvolume** -Funktion durchführt. Eine Legacy-Audio-API, z. b. DirectSound oder die **waveoutxxx** -Funktionen, bietet aber keine Möglichkeit, eine Anwendung zu benachrichtigen, wenn der Benutzer das Anwendungs Volume über sndvol ändert. Wenn eine Anwendung einen volumeschiebe Regler anzeigt, aber keine Benachrichtigungen zu volumeänderungen empfängt, kann der Schieberegler keine Änderungen widerspiegeln, die vom Benutzer in sndvol vorgenommen werden. Um das entsprechende Verhalten zu implementieren, muss der Anwendungs-Designer den Mangel an Benachrichtigungen durch die Legacy-audioapi auf irgendeine Weise kompensieren.

Eine mögliche Lösung ist, dass die Anwendung einen Zeitgeber festlegen kann, um Sie in regelmäßigen Abständen daran zu erinnern, den volumegrad zu überprüfen

Eine elegantere Lösung besteht darin, dass die Anwendung die Ereignis Benachrichtigungsfunktionen der kernaudioapis verwendet. Insbesondere kann die Anwendung eine [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstelle registrieren, um Rückrufe zu empfangen, wenn volumeänderungen oder andere Arten von Audioereignissen auftreten. Wenn das Volume geändert wird, kann die volumeänderungs-Rückruf Routine den volumeschiebe Regler der Anwendung sofort aktualisieren, um die Änderung widerzuspiegeln.

Im folgenden Codebeispiel wird gezeigt, wie eine Anwendung registriert werden kann, um Benachrichtigungen über volumeänderungen und andere Audioereignisse zu empfangen:


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



Im vorangehenden Codebeispiel wird eine Klasse mit dem Namen audiovolumeevents implementiert. Während der Programm Initialisierung aktiviert die Audioanwendung audioereignisbenachrichtigungen durch Erstellen eines audiovolumeevents-Objekts. Der Konstruktor für diese Klasse nimmt drei Eingabeparameter an:

-   *Flow*– die Datenfluss Richtung des [audioendpunktgeräts](audio-endpoint-devices.md) (ein [**edataflow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) -Enumerationswert).
-   *Role*– die aktuelle [Geräte Rolle](device-roles.md) des Endpunkt Geräts (ein [**erole-Enumerationswert**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).
-   *paudioevents*– Zeiger auf ein Objekt (eine [**iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) -Schnittstellen Instanz), das einen Satz von Rückruf Routinen enthält, die von der Anwendung implementiert werden.

Der-Konstruktor stellt den Flow und die Rollen Werte als Eingabeparameter für die [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode bereit. Die-Methode erstellt ein [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Objekt, das das audioendpunktgerät mit der angegebenen Datenfluss Richtung und der angegebenen Geräte Rolle kapselt.

Die Anwendung implementiert das Objekt, auf das *paudioevents* zeigt. (Die-Implementierung wird im vorangehenden Codebeispiel nicht gezeigt. Ein Codebeispiel, in dem eine **iaudiosessionevents** -Schnittstelle implementiert wird, finden Sie unter [audiositzungsereignisse](audio-session-events.md).) Jede Methode in dieser Schnittstelle empfängt Benachrichtigungen zu einem bestimmten Typ von Audioereignis. Wenn die Anwendung nicht an einem bestimmten Ereignistyp interessiert ist, sollte die-Methode für diesen Ereignistyp nichts Unternehmen, sondern "S OK" zurückgeben \_ .

Die [**iaudiosessionevents:: onsimplevolumechaning**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) -Methode empfängt Benachrichtigungen zu volumeänderungen. In der Regel wird mit dieser Methode der volumeschiebe Regler der Anwendung aktualisiert.

Im vorangehenden Codebeispiel registriert der Konstruktor für die audiovolumeevents-Klasse Benachrichtigungen für die prozessspezifische [Audiositzung](audio-sessions.md) , die durch den Sitzungs-GUID-Wert GUID \_ null identifiziert wird. Standardmäßig weisen ältere Audio-APIs, wie z. b. DirectSound, DirectShow und die **waveoutxxx** -Funktionen, ihre Streams dieser Sitzung zu. Eine DirectSound-oder DirectShow-Anwendung kann jedoch als Option das Standardverhalten überschreiben und die Streams einer prozessübergreifenden Sitzung oder einer Sitzung zuweisen, die durch einen anderen GUID-Wert als GUID NULL identifiziert wird \_ . (Zurzeit wird kein Mechanismus für eine **waveoutxxx** -Anwendung bereitgestellt, um das Standardverhalten auf ähnliche Weise zu überschreiben.) Ein Codebeispiel für eine DirectShow-Anwendung mit diesem Verhalten finden Sie unter [Geräte Rollen für DirectShow-Anwendungen](device-roles-for-directshow-applications.md). Um eine solche Anwendung zu integrieren, können Sie den Konstruktor im vorangehenden Codebeispiel so ändern, dass zwei zusätzliche Eingabeparameter akzeptiert werden – eine Sitzungs-GUID und ein Flag, mit dem angegeben wird, ob die zu überwachende Sitzung eine prozessübergreifende oder prozessspezifische Sitzung ist. Übergeben Sie diese Parameter an den Aufrufen der [**iaudiosessionmanager:: getaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) -Methode im-Konstruktor.

Nachdem der Konstruktor die [**iaudiosessioncontrol:: registeraudiosessionnotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) -Methode aufgerufen hat, um Benachrichtigungen zu registrieren, empfängt die Anwendung weiterhin nur dann Benachrichtigungen, wenn entweder die [**iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) -Schnittstelle oder die [**iaudiosessionmanager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) -Schnittstelle vorhanden ist. Das audiovolumeevents-Objekt im vorangehenden Codebeispiel enthält Verweise auf diese Schnittstellen, bis der debugtor aufgerufen wird. Durch dieses Verhalten wird sichergestellt, dass die Anwendung für die Lebensdauer des audiovolumeevents-Objekts weiterhin Benachrichtigungen empfängt.

Anstatt ein Audiogerät basierend auf seiner Geräte Rolle implizit auszuwählen, kann eine DirectSound-oder ältere Windows-Multimediaanwendung es dem Benutzer ermöglichen, ein Gerät explizit aus einer Liste der verfügbaren Geräte auszuwählen, die anhand seiner anzeigen Amen identifiziert werden. Um dieses Verhalten zu unterstützen, muss das vorangehende Codebeispiel so geändert werden, dass audioereignisbenachrichtigungen für das ausgewählte Gerät generiert werden. Es sind zwei Änderungen erforderlich. Ändern Sie zunächst die Konstruktordefinition so, dass Sie eine [Endpunkt-ID-Zeichenfolge](endpoint-id-strings.md) als Eingabeparameter akzeptiert (anstelle des Flows und der Rollen Parameter im Codebeispiel). Diese Zeichenfolge identifiziert das audioendpunktgerät, das dem ausgewählten DirectSound-oder Legacy Wellenform-Gerät entspricht. Ersetzen Sie anschließend den Aufrufen der Methode [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) durch einen Aufrufen der Methode [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . Der **getdevice** -Befehl nimmt die Endpunkt-ID-Zeichenfolge als Eingabeparameter an und erstellt eine Instanz des Endpunkt Geräts, das von der Zeichenfolge identifiziert wird.

Die Methode zum Abrufen der Endpunkt-ID-Zeichenfolge für ein DirectSound-Gerät oder ein Legacy-Wellenform-Gerät lautet wie folgt.

Zuerst stellt DirectSound während der Geräte Enumeration die Endpunkt-ID-Zeichenfolge für jedes aufgezählte Gerät bereit. Um mit der Geräte Enumeration zu beginnen, übergibt die Anwendung einen Rückruf Funktionszeiger als Eingabeparameter an die Funktion **directsoundcreate** oder **directsoundcaptuneu** . Die Definition der Rückruffunktion lautet wie folgt:


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



In Windows Vista zeigt der *lpcstrauch Module* -Parameter auf die Endpunkt-ID-Zeichenfolge. (In früheren Versionen von Windows, einschließlich Windows Server 2003, Windows XP und Windows 2000, verweist der *lpcstrauch Module* -Parameter auf den Namen des Treiber Moduls für das Gerät.) Der *lpcstraudescription* -Parameter verweist auf eine Zeichenfolge, die den anzeigen amen des Geräts enthält. Weitere Informationen zur DirectSound-Geräte Enumeration finden Sie in der Windows SDK-Dokumentation.

Zweitens: zum Abrufen der Endpunkt-ID-Zeichenfolge für ein älteres Wellenform-Gerät verwenden Sie die **waveoutmessage** -Funktion oder die **waveinmessage** -Funktion, um eine drv \_ -queryfunctioninstanceid-Meldung an den Wellenform-Gerätetreiber zu senden. Ein Codebeispiel, in dem die Verwendung dieser Nachricht veranschaulicht wird, finden Sie unter [Geräte Rollen für ältere Windows-Multimediaanwendungen](device-roles-for-legacy-windows-multimedia-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacy-audioapis](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



