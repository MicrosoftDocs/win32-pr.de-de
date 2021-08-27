---
description: 'Diese Programmierreferenz für das Core Audio SDK umfasst die folgenden Schnittstellen:'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Kernaudioschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330bb620b48b865db3db2ab5ea5625b7859588bd8e53e1addbcd8fd8ec9bda6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109470"
---
# <a name="core-audio-interfaces"></a>Kernaudioschnittstellen

Diese Programmierreferenz für das Core Audio SDK umfasst die folgenden Schnittstellen:

## <a name="mmdevice-api"></a>MMDevice-API

Die Windows Multimedia Device -API (MMDevice) ermöglicht Audioclients, Audioendpunktgeräte zu [ermitteln,](audio-endpoint-devices.md)ihre Funktionen zu bestimmen und Treiberinstanzen für diese Geräte zu erstellen. Die Headerdatei Mmdeviceapi.h definiert die Schnittstellen in der MMDevice-API. Weitere Informationen finden Sie unter [Informationen zur MMDevice-API.](mmdevice-api.md)

In der folgenden Tabelle sind die MMDevice-Schnittstellen aufgeführt, die mit dem Core Audio SDK für Windows Vista verfügbar sind.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Stellt ein Audiogerät dar.                                                                                                                                                                    |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Stellt eine Auflistung von Audiogeräten dar.                                                                                                                                                      |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Stellt Methoden zum Aufzählen von Audiogeräten zur Verfügung.                                                                                                                                                |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Stellt ein Audioendpunktgerät dar.                                                                                                                                                           |
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Stellt Benachrichtigungen zum Hinzu- oder Entfernen eines Audioendpunktgeräts, zum Ändern des Zustands oder der Eigenschaften eines Geräts oder zu einer Änderung der einem Gerät zugewiesenen Standardrolle zur Benachrichtigung. |



 

## <a name="wasapi"></a>WASAPI

Mit Windows AUDIO Session API (WASAPI) können Clientanwendungen den Fluss von Audiodaten zwischen der Anwendung und einem [Audioendpunktgerät verwalten.](audio-endpoint-devices.md) Die HEADERdateien Audioclient.h und Audiopolicy.h definieren die WASAPI-Schnittstellen. Weitere Informationen finden Sie unter [Informationen zu WASAPI.](wasapi.md)

In der folgenden Tabelle sind die WASAPI-Schnittstellen aufgeführt, die mit dem Core Audio SDK für Windows Vista und höher verfügbar sind.



| Schnittstelle                                                                                    | BESCHREIBUNG                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActivateAudioInterfaceAsyncOperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Stellt einen asynchronen Vorgang dar, bei dem eine [WASAPI-Schnittstelle](wasapi.md) aktiviert wird, und stellt eine Methode zum Abrufen der Aktivierungsergebnisse bereit.<br/> Gilt ab Windows 8.<br/> |
| [**IActivateAudioInterfaceCompletionHandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Stellt einen Rückruf bereit, um anzugeben, dass die Aktivierung einer [WASAPI-Schnittstelle](wasapi.md) abgeschlossen ist.<br/> Gilt ab Windows 8.<br/>                                                  |
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Ermöglicht einem Client das Lesen von Eingabedaten aus einem Erfassungsendpunktpuffer.                                                                                                                                       |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Ermöglicht einem Client das Erstellen und Initialisieren eines Audiostreams zwischen einer Audioanwendung und der Audio-Engine oder dem Hardwarepuffer eines Audioendpunktgeräts.                                           |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Ermöglicht es einem Client, die Datenrate eines Streams und die aktuelle Position im Stream zu überwachen.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Ermöglicht einem Client, die aktuelle Geräteposition zu erhalten.<br/>                                                                                                                                           |
| [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Ermöglicht einem Client das Festlegen der Abtastrate eines Streams.<br/>                                                                                                                                           |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Ermöglicht einem Client das Schreiben von Ausgabedaten in einen Renderingendpunktpuffer.                                                                                                                                     |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Ermöglicht einem Client, die Steuerungsparameter für eine Audiositzung zu konfigurieren und Ereignisse in der Sitzung zu überwachen.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Ermöglicht einem Client das Erhalten von Informationen über die Audiositzung.<br/>                                                                                                                                   |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Ermöglicht einem Client den Zugriff auf die Sitzungssteuerelemente und Volumesteuerelemente für prozessübergreifende und prozessspezifische Audiositzungen.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Verwaltet alle Untermischungen, einschließlich Enumeration und Benachrichtigung über Untermischungen. Es bietet auch Unterstützung für das Senden von Benachrichtigungen.<br/>                                                                   |
| [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Ermöglicht einem Client das Aufzählen von Audiositzungen.<br/>                                                                                                                                                  |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Ermöglicht es einem Client, die Lautstärkeebenen für alle Kanäle in einem Audiostream zu steuern und zu überwachen.                                                                                                     |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Ermöglicht es einem Client, die Lautstärkeebenen für alle Kanäle in der Audiositzung zu steuern, zu der der Stream gehört.                                                                                    |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Ermöglicht es einem Client, die Master-Volumeebene einer Audiositzung zu steuern.                                                                                                                                  |
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Stellt Benachrichtigungen zu sitzungsbezogenen Ereignissen wie Änderungen auf Volumeebene, Anzeigename und Sitzungszustand zur Verfügung.                                                                                    |
| [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Sendet Benachrichtigungen, wenn Sitzungsänderungen auftreten. <br/>                                                                                                                                               |
| [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Sendet Benachrichtigungen über ausstehende Systemänderungen.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>DeviceTopology-API

Die DeviceTopology-API bietet Clientanwendungen die Möglichkeit, die funktionalen Hardwaretopologien von Audiorendering- und Erfassungsgeräten zu durchlaufen. Die Headerdatei Devicetopology.h definiert die Schnittstellen in der DeviceTopology-API. Weitere Informationen finden Sie unter [Gerätetopologien und](device-topologies.md) [**DeviceTopology-API.**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)

In der folgenden Tabelle sind die DeviceTopology-Schnittstellen aufgeführt, die mit dem Core Audio SDK für Windows Vista und höher verfügbar sind.



| Schnittstelle                                                           | BESCHREIBUNG                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Ermöglicht den Zugriff auf eine Hardware automatic gain control (AGC).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Ermöglicht den Zugriff auf ein Hardwaresteuersystem auf Hardwareebene.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Ermöglicht den Zugriff auf ein Hardwarekanalkonfigurations-Steuerelement.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Ermöglicht den Zugriff auf ein Hardware-Multiplexer-Steuerelement (Eingabeselektor).                                                                                                                                                       |
| [**IAudioGuidedness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Ermöglicht den Zugriff auf ein "Lautheit"-Kompensationssteuer steuerelement.                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Ermöglicht den Zugriff auf ein Hardware-Midrange-Level-Steuerelement.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Ermöglicht den Zugriff auf ein Hardwaremute-Steuerelement.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Ermöglicht den Zugriff auf ein Hardwaredemultiplexer-Steuerelement (Ausgabeauswahl).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Ermöglicht den Zugriff auf ein Hardware-Peak-Meter-Steuerelement.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Ermöglicht den Zugriff auf eine Hardwaresteuerung auf Trebleebene.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Ermöglicht den Zugriff auf eine Hardware-Volumesteuerung.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Stellt einen Verbindungspunkt zwischen Komponenten dar.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Stellt eine Steuerelementschnittstelle für einen Teil (Untereinheit oder Connector) dar.                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Stellt eine gerätespezifische Eigenschaft eines Connectors oder einer Untereinheit dar.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Ermöglicht den Zugriff auf die Topologie eines Audiogeräts.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Stellt Informationen zu den Audiodatenformaten bereit, die von einer softwarekonfigurierten E/A-Verbindung (in der Regel einem DMA-Kanal) zwischen dem Audiogerät und dem Systemspeicher unterstützt werden.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Stellt Informationen zu den Buchsen oder internen Connectors bereit, die eine physische Verbindung zwischen einem Gerät auf einem Audioadapter und einem externen oder internen Endpunktgerät (z. B. einem Mikrofon oder CD-Player) bereitstellen. |
| [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Bietet bequemen Zugriff auf die **KSPROPERTY \_ JACK \_ DESCRIPTION2-Eigenschaft** eines Connectors auf ein Endpunktgerät.<br/>                                                                                            |
| [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Stellt Informationen über die Klinkensenke bereit, wenn die Buchse von der Hardware unterstützt wird.<br/>                                                                                                                             |
| [**Ipart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Stellt einen Teil (Connector oder Untereinheit) einer Gerätetopologie dar.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Stellt eine Liste von Teilen (Connectors und Untereinheiten) dar.                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Stellt eine generische Untereinheitssteuerungsschnittstelle dar, die kanalspezifische Steuerungen über die Lautstärkeebene eines Audiodatenstroms oder eines Frequenzbands in einem Audiostream in Decibeln bereitstellt.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Stellt eine Hardwareuntereinheit (z. B. eine Steuerung auf Volumeebene) dar, die sich im Datenpfad zwischen einem Client und einem Audioendpunktgerät befindet.                                                                             |
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Stellt Benachrichtigungen bereit, wenn sich der Status eines Teils (Connector oder Untereinheit) ändert.                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>EndpointVolume-API

Mit der EndpointVolume-API können spezialisierte Clients die Lautstärkestufen von [Audioendpunktgeräten](audio-endpoint-devices.md)steuern und überwachen. Die Headerdatei Endpointvolume.h definiert die Schnittstellen in der EndpointVolume-API. Weitere Informationen finden Sie unter [**EndpointVolume-API.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)

In der folgenden Tabelle sind die EndpointVolume-Schnittstellen aufgeführt, die mit dem Core Audio SDK für Windows Vista verfügbar sind.



| **Interface**                                                        | **Beschreibung**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Stellt die Volumesteuerelemente für den Audiostream an ein oder von einem Audioendpunktgerät dar.           |
| [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Stellt Volumesteuerelemente für den Audiostream an oder von einem Geräteendpunkt bereit.<br/>             |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Stellt eine Spitzenmessung im Audiodatenstrom eines Audioendpunktgeräts oder von einem Audioendpunktgerät dar.                  |
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Stellt Benachrichtigungen bereit, wenn sich die Lautstärke oder der Mutingzustand eines Audioendpunktgeräts ändert. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

