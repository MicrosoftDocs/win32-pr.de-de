---
description: Audioereignisse für Legacyaudioanwendungen
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Audioereignisse für Legacyaudioanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030561123ba8501a66a2837bcc323a6505226a80c385f3dcaa532b2e6cd8c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018488"
---
# <a name="audio-events-for-legacy-audio-applications"></a>Audioereignisse für Legacyaudioanwendungen

Legacy-Audio-APIs wie DirectSound, DirectShow und die **WaveOutXxx-Funktionen** ermöglichen Es Anwendungen, die Lautstärkestufen von Audiostreams abzurufen und festzulegen. Anwendungen können die Volumesteuerungsfunktionen in diesen APIs verwenden, um Volumeschieberegler in ihren Anwendungsfenstern anzuzeigen.

In Windows Vista ermöglicht das Systemvolumeprogramm Sndvol die Steuerung der Audiovolumenebenen für einzelne Anwendungen. Die von Anwendungen angezeigten Volumeschieberegler sollten mit den entsprechenden Volumeschiebereglern in Sndvol verknüpft werden. Wenn ein Benutzer das Anwendungsvolume über einen Volumeschieberegler in einem Anwendungsfenster anpasst, wird der entsprechende Volumeschieberegler in Sndvol sofort verschoben, um die neue Lautstärkestufe anzugeben. Wenn der Benutzer das Anwendungsvolume dagegen über Sndvol anpasst, sollten die Volumeschieberegler im Anwendungsfenster verschoben werden, um die neue Volumeebene anzugeben.

In Windows Vista spiegelt Sndvol sofort Volumeänderungen wider, die eine Anwendung durch Aufrufe der **IDirectSoundBuffer::SetVolume-Methode** oder **waveOutSetVolume-Funktion** vornimmt. Eine legacy-Audio-API wie DirectSound oder die **WaveOutXxx-Funktionen** bietet jedoch keine Möglichkeit, eine Anwendung zu benachrichtigen, wenn der Benutzer das Anwendungsvolume über Sndvol ändert. Wenn eine Anwendung einen Volumeschieberegler anzeigt, aber keine Benachrichtigungen über Volumeänderungen empfängt, spiegelt der Schieberegler die vom Benutzer in Sndvol vorgenommenen Änderungen nicht wider. Um das entsprechende Verhalten zu implementieren, muss der Anwendungs-Designer das Fehlen von Benachrichtigungen durch die Legacyaudio-API kompensieren.

Eine Lösung kann darin liegen, dass die Anwendung einen Timer so einstellt, dass er regelmäßig daran erinnert wird, die Volumeebene zu überprüfen, um festzustellen, ob sie sich geändert hat.

Eine elegantere Lösung besteht darin, dass die Anwendung die Ereignisbenachrichtigungsfunktionen der Kernaudio-APIs verwendet. Insbesondere kann die Anwendung eine [**IAudioSessionEvents-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) registrieren, um Rückrufe zu empfangen, wenn Volumeänderungen oder andere Arten von Audioereignissen auftreten. Wenn sich das Volume ändert, kann die Rückrufroutine für Volumeänderungen den Volumeschieberegler der Anwendung sofort aktualisieren, um die Änderung widerzuspiegeln.

Das folgende Codebeispiel zeigt, wie sich eine Anwendung registrieren kann, um Benachrichtigungen über Volumeänderungen und andere Audioereignisse zu empfangen:


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



Im vorangehenden Codebeispiel wird eine Klasse namens AudioVolumeEvents implementiert. Während der Programminitialisierung aktiviert die Audioanwendung Audioereignisbenachrichtigungen, indem ein AudioVolumeEvents-Objekt erstellt wird. Der Konstruktor für diese Klasse nimmt drei Eingabeparameter an:

-   *flow*: Die Datenflussrichtung des [Audioendpunktgeräts](audio-endpoint-devices.md) (ein [**EDataFlow-Enumerationswert).**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)
-   *role*: Die aktuelle [Geräterolle](device-roles.md) des Endpunktgeräts (ein [**ERole-Enumerationswert).**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)
-   *pAudioEvents*– Zeiger auf ein Objekt (eine [**IAudioSessionEvents-Schnittstelleninstanz),**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) das eine Reihe von Rückrufroutinen enthält, die von der Anwendung implementiert werden.

Der Konstruktor stellt die Flow- und Rollenwerte als Eingabeparameter für die [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) bereit. Die -Methode erstellt ein [**IMMDevice-Objekt,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) das das Audioendpunktgerät mit der angegebenen Datenflussrichtung und Geräterolle kapselt.

Die Anwendung implementiert das Objekt, auf das *pAudioEvents* zeigt. (Die Implementierung wird im vorherigen Codebeispiel nicht gezeigt. Ein Codebeispiel, das eine **IAudioSessionEvents-Schnittstelle** implementiert, finden Sie unter [Audio Session Events](audio-session-events.md).) Jede Methode in dieser Schnittstelle empfängt Benachrichtigungen eines bestimmten Audioereignistyps. Wenn die Anwendung nicht an einem bestimmten Ereignistyp interessiert ist, sollte die Methode für diesen Ereignistyp nichts tun, sondern S \_ OK zurückgeben.

Die [**IAudioSessionEvents::OnSimpleVolumeChanged-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) empfängt Benachrichtigungen über Volumeänderungen. In der Regel aktualisiert diese Methode den Volumeschieberegler der Anwendung.

Im vorherigen Codebeispiel registriert sich der Konstruktor für die AudioVolumeEvents-Klasse für Benachrichtigungen in der prozessspezifischen [Audiositzung,](audio-sessions.md) die durch den GUID-Wert DER Sitzung NULL identifiziert \_ wird. Standardmäßig weisen Legacy-Audio-APIs wie DirectSound, DirectShow und die **WaveOutXxx-Funktionen** ihre Streams dieser Sitzung zu. Eine DirectSound- oder DirectShow-Anwendung kann jedoch als Option das Standardverhalten überschreiben und ihre Streams einer prozessübergreifenden Sitzung oder einer Sitzung zuweisen, die durch einen anderen GUID-Wert als GUID NULL identifiziert \_ wird. (Derzeit wird kein Mechanismus für eine **waveOutXxx-Anwendung** bereitgestellt, um das Standardverhalten auf ähnliche Weise zu überschreiben.) Ein Codebeispiel für eine DirectShow-Anwendung mit diesem Verhalten finden Sie unter [Geräterollen für DirectShow-Anwendungen.](device-roles-for-directshow-applications.md) Um eine solche Anwendung zu berücksichtigen, können Sie den Konstruktor im vorherigen Codebeispiel so ändern, dass zwei zusätzliche Eingabeparameter akzeptiert werden: eine Sitzungs-GUID und ein Flag, um anzugeben, ob die zu überwachende Sitzung eine prozessübergreifende oder prozessspezifische Sitzung ist. Übergeben Sie diese Parameter an den Aufruf der [**IAudioSessionManager::GetAudioSessionControl-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) im Konstruktor.

Nachdem der Konstruktor die [**IAudioSessionControl::RegisterAudioSessionNotification-Methode**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) zum Registrieren für Benachrichtigungen aufruft, empfängt die Anwendung weiterhin nur Benachrichtigungen, solange entweder die [**IAudioSessionControl-**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) oder [**die IAudioSessionManager-Schnittstelle**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) vorhanden ist. Das AudioVolumeEvents-Objekt im vorherigen Codebeispiel enthält Verweise auf diese Schnittstellen, bis dessen Destruktor aufgerufen wird. Dieses Verhalten stellt sicher, dass die Anwendung während der Lebensdauer des AudioVolumeEvents-Objekts weiterhin Benachrichtigungen empfängt.

Anstatt ein Audiogerät basierend auf seiner Geräterolle implizit auszuwählen, ermöglicht eine DirectSound- oder Legacy-Windows Multimediaanwendung dem Benutzer möglicherweise, explizit ein Gerät aus einer Liste der verfügbaren Geräte auszuwählen, die anhand seiner Anzeigenamen identifiziert werden. Um dieses Verhalten zu unterstützen, muss das vorherige Codebeispiel geändert werden, um Audioereignisbenachrichtigungen für das ausgewählte Gerät zu generieren. Es sind zwei Änderungen erforderlich. Ändern Sie zunächst die Konstruktordefinition so, dass eine [Endpunkt-ID-Zeichenfolge](endpoint-id-strings.md) als Eingabeparameter akzeptiert wird (anstelle der Flow- und Rollenparameter im Codebeispiel). Diese Zeichenfolge identifiziert das Audioendpunktgerät, das dem ausgewählten DirectSound- oder Legacy waveform-Gerät entspricht. Ersetzen Sie zweitens den Aufruf der [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) durch einen Aufruf der [**IMMDeviceEnumerator::GetDevice-Methode.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) Der **GetDevice-Aufruf** verwendet die Endpunkt-ID-Zeichenfolge als Eingabeparameter und erstellt eine Instanz des Endpunktgeräts, das durch die Zeichenfolge identifiziert wird.

Das Verfahren zum Abrufen der Endpunkt-ID-Zeichenfolge für ein DirectSound-Gerät oder ein Älteres Waveform-Gerät lautet wie folgt.

Erstens stellt DirectSound während der Geräteenumeration die Endpunkt-ID-Zeichenfolge für jedes aufgelistete Gerät zur Verfügung. Um mit der Geräteenumeration zu beginnen, übergibt die Anwendung einen Rückruffunktionszeiger als Eingabeparameter an die **DirectSoundCreate-** oder **DirectSoundCaptureCreate-Funktion.** Die Definition der Rückruffunktion lautet:


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



In Windows Vista zeigt der *Parameter lpcstrModule* auf die Endpunkt-ID-Zeichenfolge. (In früheren Versionen von Windows, einschließlich Windows Server 2003, Windows XP und Windows 2000, verweist der *Parameter lpcstrModule* auf den Namen des Treibermoduls für das Gerät.) Der *lpcstrDescription-Parameter* verweist auf eine Zeichenfolge, die den Anzeigenamen des Geräts enthält. Weitere Informationen zur DirectSound-Geräteenumeration finden Sie in der Windows SDK-Dokumentation.

Verwenden Sie zum Abrufen der Endpunkt-ID-Zeichenfolge für ein älteres Wellenformgerät die **WaveOutMessage-** oder **waveInMessage-Funktion,** um eine DRV \_ QUERYFUNCTIONINSTANCEID-Nachricht an den Waveform-Gerätetreiber zu senden. Ein Codebeispiel, das die Verwendung dieser Meldung zeigt, finden Sie unter [Geräterollen für Legacy-Windows Multimediaanwendungen.](device-roles-for-legacy-windows-multimedia-applications.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacy-Audio-APIs](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



