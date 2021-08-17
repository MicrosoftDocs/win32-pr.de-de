---
description: DeviceTopology-API
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: DeviceTopology-API
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 3b79def9f1cb1f5ec9342074b813e50993cbc37e7a7af2a9e0b577c730156247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406755"
---
# <a name="devicetopology-api"></a>DeviceTopology-API

Weitere Informationen finden [Sie im Microsoft-Beispiel DMO Voice Capture.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray)

Die DeviceTopology-API bietet Clientanwendungen die Möglichkeit, die funktionalen Hardwaretopologien von Audiorendering- und Erfassungsgeräten zu durchlaufen. Über die Schnittstellen und Methoden in der DeviceTopology-API können Clients die funktionalen Untereinheiten (z. B. die Volumesteuerung) entdecken, die entlang der Datenpfade liegen, die zu und von Audioendpunktgeräten [führen.](audio-endpoint-devices.md) Clients können die internen Topologien von Audioadaptergeräten und Audioendpunktgeräten durchlaufen und die Verbindungen durchlaufen, die ein Gerät mit einem anderen verbinden. Weitere Informationen finden Sie unter [Gerätetopologien](device-topologies.md).

Die Headerdatei Devicetopology.h definiert die Schnittstellen in der DeviceTopology-API.

Um auf die Schnittstellen der DeviceTopology-API zuzugreifen, erhält ein Client zunächst mit den folgenden Schritten einen Verweis auf die [**IDeviceTopology-Schnittstelle**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) für ein Audioendpunktgerät:

1.  Mithilfe einer der in [**IMMDevice Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)beschriebenen Techniken erhalten Sie einen Verweis auf die **IMMDevice-Schnittstelle** für ein Audioendpunktgerät.
2.  Rufen Sie die [**IMMDevice::Activate-Methode auf,**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) bei der der *Parameter iid* auf **REFIID** IID \_ IDeviceTopology festgelegt ist.

Der Client kann Verweise auf die anderen Schnittstellen in der DeviceTopology-API abrufen, indem er die Methoden in der [**IDeviceTopology-Schnittstelle**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) aufruft.

Die DeviceTopology-API implementiert die folgenden Schnittstellen.



| Schnittstelle                                                  | Beschreibung                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Ermöglicht den Zugriff auf eine Hardware automatic gain control (AGC).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Ermöglicht den Zugriff auf ein Hardwaresteuersystem auf Hardwareebene.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Ermöglicht den Zugriff auf ein Hardwarekanalkonfigurations-Steuerelement.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Ermöglicht den Zugriff auf ein Hardware-Multiplexer-Steuerelement (Eingabeselektor).                                                                                                                                                       |
| [**IAudioGuidedness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Ermöglicht den Zugriff auf ein "Lautheit"-Kompensationssteuer steuerelement.                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Ermöglicht den Zugriff auf ein Hardware-Midrange-Level-Steuerelement.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Ermöglicht den Zugriff auf ein Hardwaremute-Steuerelement.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Ermöglicht den Zugriff auf ein Hardwaredemultiplexer-Steuerelement (Ausgabeauswahl).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Ermöglicht den Zugriff auf ein Hardware-Peak-Meter-Steuerelement.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Ermöglicht den Zugriff auf eine Hardwaresteuerung auf Trebleebene.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Ermöglicht den Zugriff auf eine Hardware-Volumesteuerung.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Stellt einen Verbindungspunkt zwischen Komponenten dar.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Stellt eine Steuerelementschnittstelle auf einem Teil (Untereinheit oder Connector) dar.                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Stellt eine gerätespezifische Eigenschaft eines Connectors oder einer Untereinheit dar.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Ermöglicht den Zugriff auf die Topologie eines Audiogeräts.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Stellt Informationen zu den Audiodatenformaten zur Verfügung, die von einer softwarekonfigurierten E/A-Verbindung (in der Regel ein DMA-Kanal) zwischen dem Audiogerät und dem Systemspeicher unterstützt werden.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Enthält Informationen zu den Buchsen oder internen Connectors, die eine physische Verbindung zwischen einem Gerät auf einem Audioadapter und einem externen oder internen Endpunktgerät (z. B. einem Mikrofon oder CD-Player) bereitstellen. |
| [**Ipart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Stellt einen Teil (Connector oder Untereinheit) einer Gerätetopologie dar.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Stellt eine Liste von Teilen (Connectors und Untereinheiten) dar.                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Stellt eine generische Untereinheit-Steuerelementschnittstelle dar, die kanalspezifische Steuerung über die Lautstärke in Dezibel eines Audiostreams oder eines Frequenzbands in einem Audiostream ermöglicht.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Stellt eine Hardwareuntereinheit (z. B. ein Steuerelement auf Volumeebene) dar, die sich im Datenpfad zwischen einem Client und einem Audioendpunktgerät befindet.                                                                             |



 

DeviceTopology-API-Clients, die Benachrichtigungen über Ereignisse zur Steuerungsänderung in Connectors und Untereinheiten erfordern, sollten die folgende Schnittstelle implementieren.



| Schnittstelle                                            | Beschreibung                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Stellt Benachrichtigungen zum Ändern des Status eines Teils (Connector oder Untereinheit) zur |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gerätetopologien](device-topologies.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 
