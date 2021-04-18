---
description: Die Kern-audioapis wurden in Windows Vista eingeführt, das einen neuen Satz von Audiokomponenten im Benutzermodus bereitstellte, mit denen eine Client Anwendung Audiostreams mit verbesserten Audiofunktionen renderingoder aufzeichnen kann.
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: Neuerungen bei den Kerncode-APIs in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c87a4daa9e645587253239082475e59fd1563c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345620"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>Neuerungen bei den Kerncode-APIs in Windows 7

Die Kern-audioapis wurden in Windows Vista eingeführt, das einen neuen Satz von Audiokomponenten im Benutzermodus bereitstellte, mit denen eine Client Anwendung Audiostreams mit verbesserten Audiofunktionen renderingoder aufzeichnen kann. Eine allgemeine Übersicht über diesen API-Satz finden Sie unter [Informationen zu den Windows Core-audioapis](about-the-windows-core-audio-apis.md).

Die Kern-audioapis wurden in Windows 7 verbessert. In der folgenden Tabelle werden die neuen Features und die Verbesserungen der Kerncode-APIs zusammengefasst:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Allgemeine Verbesserungen</td>
<td>Die folgenden Features wurden in Windows 7 verbessert:
<ul>
<li>In Windows 7-freigabemodusstreams werden im <em>Modus mit niedriger Latenz</em>ausgeführt. Die Audioengine wird im Pullmodus ausgeführt, wobei die Latenz erheblich reduziert wird. Dies ist sehr nützlich für Kommunikationsanwendungen, bei denen eine niedrige audiostreamwartezeit für schnelleres Streaming erforderlich ist.</li>
<li>Windows 7 bietet eine bessere Erkennung von Geräte Rollen, wenn dem System ein neues Gerät hinzugefügt wird. Weitere Informationen finden Sie unter <a href="device-roles-in-windows-vista.md">Arbeiten mit Geräte Rollen</a>.</li>
<li>In Windows 7 können Sie Musik von Ihrem portablen Media Player über Ihre Computer Sprecher lauschen. Sie können dieses Aufzeichnungs Monitor Feature verwenden, indem Sie einen portablen Media Player mit einem analogen Audiokabel an Ihren Computer binden. In der Vergangenheit haben einige OEMs diese Funktionalität im Audiotreiber mithilfe eines Hardware Loopbacks bereitgestellt. In Windows 7 wurde diese Funktion dem Betriebssystem hinzugefügt. Da sich diese im System und nicht im Treiber befindet, können Sie diese für alle anderen Geräte verwenden, die mit dem System verbunden sind, z. b. ein USB-Headset.</li>
<li>Die Codec-Audiodatei wurde in Windows 7 verbessert und bietet Unterstützung für das High-Bit-Rate-Format. Mit dieser Verbesserung können Sie Multichannel-Audiodaten und komprimierte Audioformate über einen HDMI-Connector an einen Audioempfänger unterstützen.</li>
<li>In Windows Vista spielt Windows Media Player Musik nur über das Standardaudiogerät, das vom Benutzer nicht geändert werden kann. Damit Windows Media Player Audiodaten auf einem bestimmten Gerät Rendering, muss das Standardgerät in der <strong>Sounds</strong> -Systemsteuerung geändert werden. In Windows 7 werden von Windows Media Player APIs bereitstellt, mit denen eine Anwendung auf jedem Gerät, das vom Benutzer ausgewählt wurde, und nicht nur auf dem Standardgerät dargestellt werden kann.</li>
<li>Wenn ein Computer unter Windows Vista in den Energiesparmodus wechselt, wird der Computer gesperrt. wenn der Benutzer die Wiedergabe unterbrechen möchte, muss sich der Benutzer anmelden und die Taste drücken, um die Wiedergabe zu stoppen. Wenn der Computer in Windows 7 gesperrt ist, können Sie die Wiedergabe mit dem HID-Steuerelement auf der Tastatur weiterhin steuern.</li>
<li>Windows 7 verringert den Stromverbrauch für jede Anwendung, die DirectSound und DirectShow zum Rendering von Medien verwendet. Außerdem ermöglicht der multimediaklasse Scheduler-Dienst eine gleitbare Audiofunktion und verwendet weniger Leistung, während die Audiobeispiele generiert werden.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kommunikationsgerät (neu)</td>
<td>In dieser Version wurde der <strong>Sounds</strong> -Systemsteuerung ein neuer Gerätetyp hinzugefügt: <strong>Kommunikations</strong> Gerät. Dieses Gerät wird hauptsächlich für die Kommunikation verwendet, um Telefonanrufe auf dem Computer zu tätigen oder zu empfangen. Eine Kommunikationsanwendung kann kernaudiokomponenten verwenden, um einen Verweis auf den Endpunkt des Standard kommunikationsgeräts zu erhalten und Audiostreams zu Kommunikationszwecken zu erstellen. Das Betriebssystem betrachtet den in einem Kommunikationsgerät geöffneten Stream als einen Kommunikationsstream. Die WASAPI-Vorgänge in einem Kommunikationsstream ähneln anderen Audiodaten strömen. Weitere Informationen finden Sie unter <a href="device-roles-in-windows-vista.md">Arbeiten mit Geräte Rollen</a>.</td>
</tr>
<tr class="odd">
<td>Streamdämpfung oder audioducking (neu)</td>
<td>Das automatische ducken oder die <a href="stream-attenuation.md">streamdämpfung</a> ist ein neues Feature in Windows 7, das für VoIP-und Unified Communication-Anwendungen vorgesehen ist. Standardmäßig reduziert das Betriebssystem die Intensität eines Audiostreams, wenn ein Kommunikationsstream, z. b. ein Telefonanruf, über den Computer auf dem Kommunikationsgerät empfangen wird. Die Volumeoptionen werden vom Benutzer in <strong>der Systemsteuerung</strong> festgelegt. In den Windows SDK wurden neue APIs hinzugefügt, die es Anwendungen ermöglichen, das standardmäßige Ducking-Verhalten zu ersetzen. Weitere Informationen zum Implementieren eines benutzerdefinierten Ducking-Features finden Sie unter <a href="providing-a-custom-ducking-experience.md">Bereitstellen eines benutzerdefinierten Ducking-Verhaltens</a>. <br/></td>
</tr>
<tr class="even">
<td>Streamrouting (neu)</td>
<td>In Windows 7 wurden die kernweb-APIs verbessert, um einen Audiostream nahtlos von einem vorhandenen Gerät an einen neuen standardaudioendpunkt zu übertragen. Allgemeine Audio-API-Sätze, die kernaudio-APIs verwenden, wie z. b. Media Foundation, DirectSound und Wave-APIs, implementieren das Stream-Routing Feature. Medienanwendungen, die diese API-Sätze zum Wiedergeben oder Erfassen eines Streams verwenden, verwenden die Standard Implementierung und müssen die Anwendung nicht ändern. Wenn Ihre Medien Anwendung jedoch kernaudioapis direkt verwendet, muss die Anwendung die Implementierung des streamroutings bereitstellen. Hierzu muss die Anwendung neue Ereignisse verarbeiten, die hinzugefügt wurden und einen WASAPI-Client Benachrichtigen, wenn das Standardgerät verbunden oder entfernt wird. Weitere Informationen zu dieser Funktion finden Sie unter <a href="stream-routing.md">streamrouting</a>.</td>
</tr>
<tr class="odd">
<td>Geschützter benutzermodusaudiodatei (Puma) (verbessert)</td>
<td>Puma wurde für Windows 7 aktualisiert, um die folgenden Features bereitzustellen:
<ul>
<li>Festlegen von Bits (Serial Copy Management System) an S/PDIF-Endpunkten und HDCP-Bits (High-Bandwidth Digital Content Protection) auf High-Definition Multimedia Interface (HDMI)-Endpunkten.</li>
<li>Aktivieren von SCMS-und HDMI-Schutzsteuer Elementen außerhalb einer geschützten Umgebung (PE).</li>
</ul>
Weitere Informationen zu den Verbesserungen finden Sie unter <a href="protected-user-mode-audio--puma-.md">geschützter benutzermodusaudiodatei (Puma)</a>.<br/></td>
</tr>
<tr class="even">
<td>Die <strong>WAVEFORMATEXTENSIBLE</strong> -Struktur wurde auf die <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> Struktur erweitert (neu).</td>
<td>In Windows 7 wurde eine neue Struktur hinzugefügt, um IEC 61937-Übertragungen zu unterstützen. <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> erweitert die <strong>WAVEFORMATEXTENSIBLE</strong> -Struktur so, dass zwei Sätze von audiostreammerkmalen gespeichert werden: das codierte Audioformat vor der Übertragung und die Merkmale des Audiostreams, nachdem er decodiert wurde. Die neue Struktur gibt explizit die effektive Anzahl von Kanälen, die Stichprobengröße und die Datenrate eines nicht-PCM-Formats an. Mit diesen Informationen kann eine Anwendung die Qualitätsstufe des nicht-PCM-Streams ableiten, nachdem Sie dekomprimiert und wiedergegeben wurde. Weitere Informationen finden Sie unter <a href="representing-formats-for-iec-61937-transmissions.md">darstellen von Formaten für IEC 61937</a>-Übertragungen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>Iaudioclient:: Initialize</strong></a> (verbessert)</td>
<td>Die <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>iaudioclient:: Initialize</strong></a> -Methode wurde verbessert, um bestimmte Fehler anzuzeigen, die beim Öffnen eines Audiostreams auftreten können. Die neuen Fehlercodes lauten wie folgt:
<ul>
<li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li>
<li>AUDCLNT_E_BUFFER_SIZE_ERROR</li>
<li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li>
</ul>
Weitere Informationen zu diesen Fehlern finden Sie im Abschnitt "Rückgabewert" in <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>iaudioclient:: Initialize</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>Iaudiocaptureclient:: GetBuffer</strong></a> und <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>iaudiorenderclient:: GetBuffer</strong></a> (verbessert)</td>
<td>Die <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>iaudiocaptureclient:: GetBuffer</strong></a> -Methode und die <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>iaudiorenderclient:: GetBuffer</strong></a> -Methode wurden verbessert, um den AUDCLNT_E_BUFFER_ERROR-Fehlercode zurückzugeben, der angibt, dass der Endpunkt Puffer im exklusiven Modus nicht abgerufen wurde. Weitere Informationen finden Sie unter Hinweise in <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>iaudiocaptureclient:: GetBuffer</strong></a> und <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>iaudiorenderclient:: GetBuffer</strong></a>.</td>
</tr>
<tr class="odd">
<td>Jack-Erkennungsfunktion (verbessert)</td>
<td>Eine neue Schnittstelle in Windows 7, <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2</strong></a>, erweitert " <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>iksjackdescription</strong></a>". Mithilfe der neuen Schnittstelle kann der audiostapel oder eine Anwendung zusätzliche Jack-Informationen erhalten. Dies schließt die Erkennungsfunktion von Jack ein und gibt an, ob sich das Format des Geräts dynamisch geändert hat.</td>
</tr>
<tr class="even">
<td>Windows-Beispiele (neu)</td>
<td>Der Windows SDK wurden neue Beispiele hinzugefügt, die die Verwendung der kernaudioapis veranschaulichen. Weitere Informationen finden Sie unter <a href="sdk-samples-that-use-the-core-audio-apis.md">SDK-Beispiele, die die Kerndatei-APIs verwenden</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="major-new-interfaces"></a>Wichtige neue Schnittstellen

Die folgenden Schnittstellen sind neu in Windows 7:

-   [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)
-   [**Iaudioclock-Anpassung**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)
-   [**Iaudioendpointvolumeex**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)
-   [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)
-   [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)
-   [**Iaudiosessionenumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)
-   [**Iaudiosessionnotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)
-   [**Iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)
-   [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)
-   [**Informationen zu "iksjacksink"**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu den Windows Core-audioapis](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




