---
description: Die Core Audio-APIs wurden in Windows Vista eingeführt, die einen neuen Satz von Audiokomponenten im Benutzermodus bereitstellte, die eine Clientanwendung zum Rendern oder Erfassen von Audiostreams mit verbesserten Audiofunktionen verwenden kann.
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: Neuerungen bei Core Audio-APIs in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6160b275512a7efbd3b795e263f2ce8ae01be965
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474706"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>Neuerungen bei Core Audio-APIs in Windows 7

Die Core Audio-APIs wurden in Windows Vista eingeführt, die einen neuen Satz von Audiokomponenten im Benutzermodus bereitstellte, die eine Clientanwendung zum Rendern oder Erfassen von Audiostreams mit verbesserten Audiofunktionen verwenden kann. Eine allgemeine Übersicht über diesen API-Satz finden Sie unter [Informationen zu den Windows Core Audio-APIs.](about-the-windows-core-audio-apis.md)

Die Core Audio-APIs wurden in Windows 7 verbessert. In der folgenden Tabelle sind die neuen Features und verbesserungen an den Core Audio-APIs zusammengefasst:




| Funktion | BESCHREIBUNG | 
|---------|-------------|
| Generische Verbesserungen | Die folgenden Features wurden in Windows 7 verbessert:<ul><li>In Windows 7-Freigabemodus werden Streams im <em>Modus mit geringer Latenz</em>ausgeführt. Die Audio-Engine wird im Pullmodus mit einer erheblichen Verringerung der Latenz ausgeführt. Dies ist sehr nützlich für Kommunikationsanwendungen, die eine niedrige Audiostreamlatenz für schnelleres Streaming erfordern.</li><li>Windows 7 bietet eine bessere Erkennung von Geräterollen, wenn dem System ein neues Gerät hinzugefügt wird. Weitere Informationen finden Sie unter <a href="device-roles-in-windows-vista.md">Arbeiten mit Geräterollen.</a></li><li>In Windows 7 können Sie Musik von Ihrem portablen Media Player über Die Lautsprecher Ihres Computers hören. Sie können dieses Capture Monitor-Feature verwenden, indem Sie einen portablen Medienplayer mit einem analogen Audiokabel an Ihren Computer anschließen. In der Vergangenheit haben einige OEMs diese Funktionalität im Audiotreiber mithilfe eines Hardware-Loopbacks bereitgestellt. In Windows 7 wurde diese Funktion dem Betriebssystem hinzugefügt. Da sich dies im System und nicht im Treiber befindet, können Sie dies für jedes andere Gerät verwenden, das mit dem System verbunden ist, z. B. ein USB-Headset.</li><li>DAS AUDIO wurde in Windows 7 verbessert, das Unterstützung für das Format mit hoher Bitrate bietet. Mit dieser Verbesserung können Sie Mehrkanalaudio- und komprimierte Audioformate über einen CONNECTORS-Connector an einen Audioempfänger unterstützen.</li><li>In Windows Vista gibt Windows Media Player Musik nur über das Standardaudiogerät wieder, das vom Benutzer nicht geändert werden kann. Damit Windows Media Player Audio auf einem bestimmten Gerät rendern kann, muss das Standardgerät in <strong>der</strong> Sound-Systemsteuerung geändert werden. In Windows 7 stellt Windows Media Player APIs bereit, die es einer Anwendung ermöglichen, auf jedem vom Benutzer ausgewählten Gerät und nicht nur auf dem Standardgerät zu rendern.</li><li>Wenn in Windows Vista ein Computer, auf dem Audio wiedergegeben wird, in den Energiesparmodus wechselt, der Computer gesperrt ist und der Benutzer die Wiedergabe unterbrechen möchte, muss er sich anmelden und die Stopptaste drücken, um die Wiedergabe zu beenden. Wenn der Computer in Windows 7 gesperrt ist, können Sie die Wiedergabe weiterhin mithilfe des HID-Steuerelements auf der Tastatur steuern.</li><li>Windows 7 reduziert den Stromverbrauch für alle Anwendungen, die DirectSound und DirectShow zum Rendern von Medien verwenden. Darüber hinaus ermöglicht der Multimedia Class Scheduler Service störungsresiliente Audiodaten und verbraucht weniger Leistung, während die Audiobeispiele generiert werden.</li></ul> | 
| Kommunikationsgerät (neu) | In dieser Version wurde <strong>der</strong> Sound-Systemsteuerung ein neuer Gerätetyp hinzugefügt: <strong>Kommunikationsgerät.</strong> Dieses Gerät wird hauptsächlich für die Kommunikation verwendet, d. h. zum Tätigen oder Empfangen von Telefonanrufen auf dem Computer. Eine Kommunikationsanwendung kann Core Audio-Komponenten verwenden, um einen Verweis auf den Endpunkt des Standardkommunikationsgeräts abzurufen und Audiostreams zu Kommunikationszwecken zu rendern. Das Betriebssystem betrachtet den auf einem Kommunikationsgerät geöffneten Datenstrom als Kommunikationsdatenstrom. Die WASAPI-Vorgänge für einen Kommunikationsdatenstrom ähneln jedem anderen Audiostream. Weitere Informationen finden Sie unter <a href="device-roles-in-windows-vista.md">Arbeiten mit Geräterollen.</a> | 
| Stream-Dämpfung oder Audioentzung (Neu) | Automatisches Entschüben oder <a href="stream-attenuation.md">Stream Attenuation</a> ist ein neues Feature in Windows 7, das für VoIP- und Unified Communication-Anwendungen vorgesehen ist. Standardmäßig verringert das Betriebssystem die Intensität eines Audiodatenstroms, wenn ein Kommunikationsdatenstrom, z. B. ein Telefonanruf, auf dem Kommunikationsgerät über den Computer empfangen wird. Die Lautstärkeoptionen werden vom Benutzer <strong></strong> in der Sound-Systemsteuerung festgelegt. Dem Windows SDK wurden neue APIs hinzugefügt, die es Anwendungen ermöglichen, das Standardverhalten zu ersetzen. Weitere Informationen zum Implementieren einer benutzerdefinierten Entenfunktion finden Sie unter <a href="providing-a-custom-ducking-experience.md">Bereitstellen eines benutzerdefinierten Enthaltungsverhaltens.</a> <br /> | 
| Streamrouting (neu) | In Windows 7 wurden die Core Audio-APIs verbessert, um einen Audiostream nahtlos von einem vorhandenen Gerät an einen neuen Standardaudioendpunkt zu übertragen. High-Level-Audio-API-Sätze, die Core Audio-APIs wie Media Foundation, DirectSound und WAVE-APIs verwenden, implementieren das Streamroutingfeature. Medienanwendungen, die diese API-Sätze zum Wiedergeben oder Erfassen eines Streams verwenden, verwenden die Standardimplementierungen und müssen die Anwendung nicht ändern. Wenn Ihre Medienanwendung jedoch Core Audio-APIs direkt verwendet, muss die Anwendung die Implementierung des Streamroutings bereitstellen. Zu diesem Zeitpunkt muss die Anwendung neue Ereignisse behandeln, die hinzugefügt wurden, die einen WASAPI-Client benachrichtigen, wenn das Standardgerät verbunden oder entfernt wird. Weitere Informationen zu diesem Feature finden Sie unter <a href="stream-routing.md">Streamrouting.</a> | 
| Audio im geschützten Benutzermodus (PROTECTED) (verbessert) | FÜR Windows 7 wurde DAS UPDATE aktualisiert, um die folgenden Features bereitzustellen:<ul><li>Festlegen von SCMS-Bits (Serial Copying Management System) auf S/PDIF-Endpunkten und High-bandwidth Digital Content Protection -Bits (HDCP) auf High-Definition MULTIMEDIA Interface-Endpunkten (CSV).</li><li>Aktivieren von SCMS- und PROTECTION Protection-Steuerelementen außerhalb einer geschützten Umgebung (PE).</li></ul>Weitere Informationen zu den Verbesserungen finden Sie unter <a href="protected-user-mode-audio--puma-.md">Protected User Mode Audio (MODI)</a>.<br /> | 
| Die <strong>WAVEFORMATEXTENSIBLE-Struktur</strong> wurde auf die <strong>WAVEFORMATEXTENSIBLE_IEC61937-Struktur</strong> erweitert (Neu). | In Windows 7 wurde eine neue Struktur hinzugefügt, um IEC 61937-Übertragungen zu unterstützen. <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> erweitert die <strong>WAVEFORMATEXTENSIBLE-Struktur,</strong> um zwei Sätze von Audiodatenstromeigenschaften zu speichern: das codierte Audioformat vor der Übertragung und die Merkmale des Audiodatenstroms nach der Decodierung. Die neue -Struktur gibt explizit die effektive Anzahl von Kanälen, die Stichprobengröße und die Datenrate eines Nicht-PCM-Formats an. Mit diesen Informationen kann eine Anwendung die Qualitätsstufe des Nicht-PCM-Streams ableiten, nachdem er dekomprimiert und wiedergegeben wurde. Weitere Informationen finden Sie unter <a href="representing-formats-for-iec-61937-transmissions.md">Darstellen von Formaten für IEC 61937-Übertragungen.</a><br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient::Initialize</strong></a> (verbessert) | Die <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient::Initialize-Methode</strong></a> wurde verbessert, um bestimmte Fehler anzugeben, die beim Öffnen eines Audiostreams auftreten können. Die neuen Fehlercodes sind:<ul><li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li><li>AUDCLNT_E_BUFFER_SIZE_ERROR</li><li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li></ul>Weitere Informationen zu diesen Fehlern finden Sie im Abschnitt Rückgabewert in <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient::Initialize</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient::GetBuffer</strong></a> und <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a> (verbessert) | Die Methoden <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient::GetBuffer</strong></a> und <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a> wurden verbessert, um den AUDCLNT_E_BUFFER_ERROR Fehlercode zurückzugeben, der angibt, dass der Endpunktpuffer im exklusiven Modus nicht abgerufen wurde. Weitere Informationen finden Sie unter Hinweise in <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient::GetBuffer</strong></a> und <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a>. | 
| Jack-Erkennungsfunktion (verbessert) | Eine neue Schnittstelle in Windows 7, <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2,</strong></a>erweitert <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>IKsJackDescription</strong></a>. Mithilfe der neuen Schnittstelle kann der Audiostapel oder eine Anwendung zusätzliche Jack-Informationen abrufen. Dies schließt die Erkennungsfunktion der Buchse ein und gibt an, ob sich das Format des Geräts dynamisch geändert hat. | 
| Windows Beispiele (neu) | Dem Windows SDK wurden neue Beispiele hinzugefügt, die die Verwendung der Core Audio-APIs veranschaulichen. Weitere Informationen finden Sie unter <a href="sdk-samples-that-use-the-core-audio-apis.md">SDK-Beispiele, die die Core Audio-APIs verwenden.</a> | 




 

## <a name="major-new-interfaces"></a>Wichtige neue Schnittstellen

Die folgenden Schnittstellen sind für Windows 7 neu:

-   [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)
-   [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)
-   [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)
-   [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)
-   [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)
-   [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)
-   [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)
-   [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)
-   [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)
-   [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu den Windows Core Audio-APIs](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




