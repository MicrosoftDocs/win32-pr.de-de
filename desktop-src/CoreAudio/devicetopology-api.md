---
description: Debug-opology-API
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: Debug-opology-API
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 472c02cd59ca0cadd922cbe398a768c97cfab73a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106373556"
---
# <a name="devicetopology-api"></a>Debug-opology-API

Weitere Informationen finden Sie im [Microsoft High Quality Voice Capture DMO-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray).

Die Geräte-API (Debug-API) bietet Client Anwendungen die Möglichkeit, die funktionalen hardwaretopologien von audiorendering und Erfassungs Geräten zu durchlaufen. Über die Schnittstellen und Methoden in der devicetopology-API können Clients die funktionalen Untereinheiten (z. b. die volumesteuerung) ermitteln, die auf den Daten Pfaden liegen, die zu und von [audioendpunktgeräten](audio-endpoint-devices.md)führen. Clients können die internen Topologien von audioadaptern und audioendpunktgeräten durchlaufen und über die Verbindungen hinweg wechseln, die ein Gerät mit einem anderen verbinden. Weitere Informationen finden Sie unter [Device Topologien](device-topologies.md).

Die Header Datei "devicetopology. h" definiert die Schnittstellen in der devicetopology-API.

Um auf die API-Schnittstellen der devicetopology zuzugreifen, Ruft ein Client zuerst einen Verweis auf die [**idevicetopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) -Schnittstelle für ein audioendpunktgerät ab, indem er die folgenden Schritte ausführen:

1.  Mithilfe einer der in der [**immdevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)beschriebenen Verfahren erhalten Sie einen Verweis auf die **immdevice** -Schnittstelle für ein audioendpunktgerät.
2.  Aufrufen der Methode " [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) " mit dem Parameter " *IID* ", der auf **refID** IID \_ idevicetopology festgelegt ist.

Der Client kann Verweise auf andere Schnittstellen in der devicetopology-API abrufen, indem er die Methoden in der [**idevicetopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) -Schnittstelle aufruft.

Die devicetopology-API implementiert die folgenden Schnittstellen.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iaudioautogaincontrol**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Bietet Zugriff auf ein Hardware-Steuerelement zum automatischen gewinnen (Automatic Access Control, AGC)                                                                                                                                                               |
| [**Iaudiobass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Ermöglicht den Zugriff auf ein Steuerelement auf der Basis von Hardware.                                                                                                                                                                         |
| [**Iaudiochannelconfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Ermöglicht den Zugriff auf ein Hardware-Channel-Konfigurations Steuerelement.                                                                                                                                                              |
| [**Iaudioinputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Ermöglicht den Zugriff auf ein Hardware-Multiplexer-Steuerelement (Eingabeauswahl).                                                                                                                                                       |
| [**Iaudioloudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Bietet Zugriff auf ein Steuerelement für die "Lautstärke"-Kompensierung.                                                                                                                                                                     |
| [**Iaudiomidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Ermöglicht den Zugriff auf ein Hardware-Midrange-Steuerelement.                                                                                                                                                                     |
| [**Iaudiomute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Ermöglicht den Zugriff auf ein Hardware stumm Steuerelement.                                                                                                                                                                               |
| [**Iaudiooutputselector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Ermöglicht den Zugriff auf ein Hardware-Demultiplexer-Steuerelement (Ausgabe Auswahl).                                                                                                                                                    |
| [**Iaudiopeakmeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Bietet Zugriff auf ein Hardware-Spitzenwert-Steuerelement.                                                                                                                                                                         |
| [**Iaudiotreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Bietet Zugriff auf ein Steuerelement auf Hardwareebene.                                                                                                                                                                       |
| [**Iaudiovolumelevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Ermöglicht den Zugriff auf ein Hardware Volume-Steuerelement.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Stellt einen Verbindungspunkt zwischen Komponenten dar.                                                                                                                                                                      |
| [**Icontrolinterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Stellt eine Steuerelement Schnittstelle in einem Teil (subunit oder Connector) dar.                                                                                                                                                          |
| [**Idevicespecificproperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Stellt eine gerätespezifische Eigenschaft eines Connector oder einer Untereinheit dar.                                                                                                                                                          |
| [**Idevicetopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Bietet Zugriff auf die Topologie eines Audiogeräts.                                                                                                                                                                       |
| [**"Iksformatsupport"**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Enthält Informationen zu den Audiodateiformaten, die von einer Software konfigurierten e/a-Verbindung (in der Regel ein DMA-Kanal) zwischen dem Audiogerät und dem Systemspeicher unterstützt werden.                                        |
| [**"Iksjackdescription"**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Enthält Informationen zu den Buben oder internen Connectors, die eine physische Verbindung zwischen einem Gerät auf einem Audioadapter und einem externen oder internen Endpunkt Gerät (z. b. einem Mikrofon oder CD-Player) bereitstellen. |
| [**Ipart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Stellt einen Teil (Connector oder Untereinheit) einer Geräte Topologie dar.                                                                                                                                                            |
| [**Ipartslist**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Stellt eine Liste von Teilen (Connectors und Untereinheiten) dar.                                                                                                                                                                     |
| [**Iperchanneldblevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Stellt eine generische Schnittstelle für die Steuerelement-Steuerelement-Schnittstelle dar, die die Kanalsteuerung über die Volumeebene in Dezimalstellen eines Audiostreams oder eines Häufigkeits Bandes in einem Audiostream bereitstellt.                                        |
| [**Isubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Stellt eine Hardware Untereinheit (z. b. ein Steuerelement auf volumebene) dar, die im Daten Pfad zwischen einem Client und einem audioendpunktgerät liegt.                                                                             |



 

Devicetopology-API-Clients, für die Benachrichtigungen über Steuerungs Änderungs Ereignisse in Connectors und Untereinheiten erforderlich sind, müssen die folgende Schnittstelle implementieren.



| Schnittstelle                                            | BESCHREIBUNG                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**Icontrolchangenotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Stellt Benachrichtigungen bereit, wenn sich der Status eines Teils (Connector oder subunit) ändert. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gerätetopologien](device-topologies.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 
