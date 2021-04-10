---
description: 'Diese Programmier Referenz für das Core-audiosdk umfasst die folgenden Schnittstellen:'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Kernaudioschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eed875bad93bed1625a175bd74b849f139a0140
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125774"
---
# <a name="core-audio-interfaces"></a>Kernaudioschnittstellen

Diese Programmier Referenz für das Core-audiosdk umfasst die folgenden Schnittstellen:

## <a name="mmdevice-api"></a>Mmdevice-API

Mit der API von Windows Multimedia Device (mmdevice) können audioclients [audioendpunktgeräte](audio-endpoint-devices.md)ermitteln, deren Funktionen ermitteln und Treiber Instanzen für diese Geräte erstellen. Die Header Datei "mmdeviceapi. h" definiert die Schnittstellen in der mmdevice-API. Weitere Informationen finden Sie unter Informationen [zur mmdevice-API](mmdevice-api.md).

In der folgenden Tabelle sind die mmdevice-Schnittstellen aufgelistet, die mit dem Core audiosdk für Windows Vista verfügbar sind.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Stellt ein Audiogerät dar.                                                                                                                                                                    |
| [**Immde vicecollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Stellt eine Auflistung von Audiogeräten dar.                                                                                                                                                      |
| [**Immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Stellt Methoden zum Auflisten von Audiogeräten bereit.                                                                                                                                                |
| [**Immendpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Stellt ein audioendpunktgerät dar.                                                                                                                                                           |
| [**Immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Stellt Benachrichtigungen bereit, wenn ein audioendpunktgerät hinzugefügt oder entfernt wird, wenn sich der Zustand oder die Eigenschaften eines Geräts ändern oder wenn die Standard Rolle, die einem Gerät zugewiesen ist, geändert wird. |



 

## <a name="wasapi"></a>WASAPI

Mithilfe der Windows-audiositzungs-API (WASAPI) können Client Anwendungen den Fluss von Audiodaten zwischen der Anwendung und einem [audioendpunkt-Gerät](audio-endpoint-devices.md)verwalten. Header Dateien AudioClient. h und audiopolicy. h definieren die WASAPI-Schnittstellen. Weitere Informationen finden Sie unter Informationen [zu WASAPI](wasapi.md).

In der folgenden Tabelle sind die WASAPI-Schnittstellen aufgelistet, die mit dem Core-audiosdk für Windows Vista und höher verfügbar sind.



| Schnittstelle                                                                                    | BESCHREIBUNG                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iactivateaudiointerfaceasyncoperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Stellt einen asynchronen Vorgang dar, der eine [WASAPI](wasapi.md) -Schnittstelle aktiviert und eine Methode zum Abrufen der Ergebnisse der Aktivierung bereitstellt.<br/> Gilt ab Windows 8.<br/> |
| [**Iactivateaudiointerfacecompletionhandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Stellt einen Rückruf bereit, um anzugeben, dass die Aktivierung einer [WASAPI](wasapi.md) -Schnittstelle beendet ist.<br/> Gilt ab Windows 8.<br/>                                                  |
| [**Iaudiocaptureclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Ermöglicht einem Client das Lesen von Eingabedaten aus einem Erfassungs Endpunkt Puffer.                                                                                                                                       |
| [**Iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Ermöglicht es einem Client, einen Audiostream zwischen einer Audioanwendung und der Audioengine oder dem Hardware Puffer eines audioendpunktgeräts zu erstellen und zu initialisieren.                                           |
| [**Iaudioclock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Ermöglicht einem Client, die Datenrate eines Streams und die aktuelle Position im Stream zu überwachen.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Ermöglicht einem Client, die aktuelle Geräte Position zu erhalten.<br/>                                                                                                                                           |
| [**Iaudioclock-Anpassung**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Ermöglicht einem Client, die Stichprobenrate eines Streams festzulegen.<br/>                                                                                                                                           |
| [**Iaudiorenderclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Ermöglicht einem Client das Schreiben von Ausgabedaten in einen Rendering-Endpunkt Puffer.                                                                                                                                     |
| [**Iaudiosessioncontrol**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Ermöglicht einem Client, die Steuerelement Parameter für eine Audiositzung zu konfigurieren und Ereignisse in der Sitzung zu überwachen.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Ermöglicht es einem Client, Informationen über die Audiositzung zu erhalten.<br/>                                                                                                                                   |
| [**Iaudiosessionmanager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Ermöglicht einem Client den Zugriff auf die Sitzungs Steuerelemente und volumesteuerelemente für prozessübergreifende und prozessspezifische audiositzungen.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Verwaltet alle Unterverzeichnisse einschließlich Enumeration und Benachrichtigung von Unterverzeichnissen. Außerdem wird die Unterstützung für das Ducking von Benachrichtigungen bereitstellt.<br/>                                                                   |
| [**Iaudiosessionenumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Ermöglicht einem Client das Aufzählen von audiositzungen.<br/>                                                                                                                                                  |
| [**Iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Ermöglicht einem Client, die volumeebenen für alle Kanäle in einem Audiostream zu steuern und zu überwachen.                                                                                                     |
| [**Ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Ermöglicht einem Client das Steuern der volumeebenen für alle Kanäle in der Audiositzung, zu der der Stream gehört.                                                                                    |
| [**Isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Ermöglicht einem Client, die Master Volume-Ebene einer Audiositzung zu steuern.                                                                                                                                  |
| [**Iaudiosessionevents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Bietet Benachrichtigungen zu Sitzungs bezogenen Ereignissen, wie z. b. Änderungen der Volumeebene, des anzeigen Amens und des Sitzungs Zustands.                                                                                    |
| [**Iaudiosessionnotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Sendet Benachrichtigungen, wenn Sitzungs Änderungen auftreten. <br/>                                                                                                                                               |
| [**Iaudiovolumeducknotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Sendet Benachrichtigungen zu ausstehenden systemducking-Änderungen.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>Debug-opology-API

Die Geräte-API (Debug-API) bietet Client Anwendungen die Möglichkeit, die funktionalen hardwaretopologien von audiorendering und Erfassungs Geräten zu durchlaufen. Die Header Datei "devicetopology. h" definiert die Schnittstellen in der devicetopology-API. Weitere Informationen finden Sie unter [Device Topologien](device-topologies.md) und [**devicetopology API**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology).

In der folgenden Tabelle sind die Schnittstellen der devicetopology aufgeführt, die mit dem Core-audiosdk für Windows Vista und höher verfügbar sind.



| Schnittstelle                                                           | BESCHREIBUNG                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iaudioautogaincontrol**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Bietet Zugriff auf ein Hardware-Steuerelement zum automatischen gewinnen (Automatic Access Control, AGC)                                                                                                                                                               |
| [**Iaudiobass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Ermöglicht den Zugriff auf ein Steuerelement auf der Basis von Hardware.                                                                                                                                                                         |
| [**Iaudiochannelconfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Ermöglicht den Zugriff auf ein Hardware-Channel-Konfigurations Steuerelement.                                                                                                                                                              |
| [**Iaudioinputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Ermöglicht den Zugriff auf ein Hardware-Multiplexer-Steuerelement (Eingabeauswahl).                                                                                                                                                       |
| [**Iaudioloudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Bietet Zugriff auf ein Steuerelement für die "Lautstärke"-Kompensierung.                                                                                                                                                                     |
| [**Iaudiomidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Ermöglicht den Zugriff auf ein Hardware-Midrange-Steuerelement.                                                                                                                                                                     |
| [**Iaudiomute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Ermöglicht den Zugriff auf ein Hardware stumm Steuerelement.                                                                                                                                                                               |
| [**Iaudiooutputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Ermöglicht den Zugriff auf ein Hardware-Demultiplexer-Steuerelement (Ausgabe Auswahl).                                                                                                                                                    |
| [**Iaudiopeakmeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Bietet Zugriff auf ein Hardware-Spitzenwert-Steuerelement.                                                                                                                                                                         |
| [**Iaudiotreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Bietet Zugriff auf ein Steuerelement auf Hardwareebene.                                                                                                                                                                       |
| [**Iaudiovolumelevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Ermöglicht den Zugriff auf ein Hardware Volume-Steuerelement.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Stellt einen Verbindungspunkt zwischen Komponenten dar.                                                                                                                                                                      |
| [**Icontrolinterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Stellt eine Steuerelement Schnittstelle in einem Teil (subunit oder Connector) dar.                                                                                                                                                          |
| [**Idevicespecificproperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Stellt eine gerätespezifische Eigenschaft eines Connector oder einer Untereinheit dar.                                                                                                                                                          |
| [**Idevicetopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Bietet Zugriff auf die Topologie eines Audiogeräts.                                                                                                                                                                       |
| [**"Iksformatsupport"**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Enthält Informationen zu den Audiodateiformaten, die von einer Software konfigurierten e/a-Verbindung (in der Regel ein DMA-Kanal) zwischen dem Audiogerät und dem Systemspeicher unterstützt werden.                                        |
| [**"Iksjackdescription"**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Enthält Informationen zu den Buben oder internen Connectors, die eine physische Verbindung zwischen einem Gerät auf einem Audioadapter und einem externen oder internen Endpunkt Gerät (z. b. einem Mikrofon oder CD-Player) bereitstellen. |
| [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Bietet bequemen Zugriff auf die Eigenschaft " **ksproperty \_ Jack \_ DESCRIPTION2** " eines Connector auf ein Endpunkt Gerät.<br/>                                                                                            |
| [**Informationen zu "iksjacksink"**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Stellt Informationen zur Jack-Senke bereit, wenn der Jack von der Hardware unterstützt wird.<br/>                                                                                                                             |
| [**Ipart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Stellt einen Teil (Connector oder Untereinheit) einer Geräte Topologie dar.                                                                                                                                                            |
| [**Ipartslist**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Stellt eine Liste von Teilen (Connectors und Untereinheiten) dar.                                                                                                                                                                     |
| [**Iperchanneldblevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Stellt eine generische Schnittstelle für die Steuerelement-Steuerelement-Schnittstelle dar, die die Kanalsteuerung über die Volumeebene in Dezimalstellen eines Audiostreams oder eines Häufigkeits Bandes in einem Audiostream bereitstellt.                                        |
| [**Isubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Stellt eine Hardware Untereinheit (z. b. ein Steuerelement auf volumebene) dar, die im Daten Pfad zwischen einem Client und einem audioendpunktgerät liegt.                                                                             |
| [**Icontrolchangenotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Stellt Benachrichtigungen bereit, wenn sich der Status eines Teils (Connector oder subunit) ändert.                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>Endpointvolume-API

Die endpointvolume-API ermöglicht spezialisierten Clients das Steuern und Überwachen der volumeebenen von [audioendpunktgeräten](audio-endpoint-devices.md). Die Header Datei "endpointvolume. h" definiert die Schnittstellen in der endpointvolume-API. Weitere Informationen finden Sie unter [**endpointvolume-API**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .

In der folgenden Tabelle sind die endpointvolume-Schnittstellen aufgelistet, die mit dem Core-audiosdk für Windows Vista verfügbar sind.



| **Interface**                                                        | **Beschreibung**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Stellt die volumesteuerelemente im Audiostream zu oder von einem audioendpunktgerät dar.           |
| [**Iaudioendpointvolumeex**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Stellt volumesteuerelemente für den Audiostream an einen oder von einem Geräte Endpunkt bereit.<br/>             |
| [**Iaudiometerinformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Stellt einen Spitzen Zähler für den Audiostream zu oder von einem audioendpunktgerät dar.                  |
| [**Iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Stellt Benachrichtigungen bereit, wenn die Volumeebene oder der stumm Schaltung-Status eines audioendpunktgeräts geändert wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

