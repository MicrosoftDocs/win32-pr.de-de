---
title: IBasicDevice-Schnittstelle
description: Kapselt die Methoden und Ereignisse, die zum Modellieren eines DLNA-Geräts erforderlich sind.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- Media Streaming-API der IBasicDevice-Schnittstelle
- IBasicDevice-Schnittstelle Medienstreaming-API , beschrieben
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25a60a3f722faac473b6f779de2d609cbdfc4ecb257d671136a8ef80535fdf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060360"
---
# <a name="ibasicdevice-interface"></a>IBasicDevice-Schnittstelle

Kapselt die Methoden und Ereignisse, die zum Modellieren eines DLNA-Geräts erforderlich sind.

## <a name="members"></a>Member

Die **IBasicDevice-Schnittstelle** erbt von [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable). **IBasicDevice** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBasicDevice-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                 | BESCHREIBUNG                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**\_ConnectionStatusChanged hinzufügen**](ibasicdevice-add-connectionstatuschanged.md)       | Registriert einen Ereignishandler für das [**ConnectionStatusChanged-Ereignis.**](connectionstatuschanged.md)<br/>                |
| [**CanWakeDevices**](ibasicdevice-canwakedevices.md)                                  | Ruft einen Wert ab, der angibt, ob das Gerät reaktiviert werden kann.<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | Gibt einen Enumerationswert zurück, der angibt, ob das Gerät derzeit online, außerhalb oder im Ruhezustand, aber reaktivierbar ist.<br/> |
| [**Beschreibung**](ibasicdevice-description.md)                                        | Ruft eine Beschreibung des Geräts ab.<br/>                                                                              |
| [**DiscoveredOnCurrentNetwork**](ibasicdevice-discoveredoncurrentnetwork.md)          | Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.<br/>                                           |
| [**Friendlyname**](ibasicdevice-friendlyname.md)                                      | Ruft den Anzeigenamen des Geräts ab.<br/>                                                                               |
| [**Symbole**](ibasicdevice-icons.md)                                                    | Gibt einen Vektor von [**IDeviceIcon-Schnittstellen**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) zurück.<br/>                                                  |
| [**Ipaddresses**](ibasicdevice-ipaddresses.md)                                        | Gibt einen Vektor von IP-Adressen zurück.<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | Ruft den Herstellernamen des Geräts ab.<br/>                                                                           |
| [**ManufacturerUrl**](ibasicdevice-manufacturerurl.md)                                | Ruft die Hersteller-URL des Geräts ab.<br/>                                                                            |
| [**ModelName**](ibasicdevice-modelname.md)                                            | Ruft den Modellnamen des Geräts ab.<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | Ruft die Modellnummer des Geräts ab.<br/>                                                                                |
| [**ModelUrl**](ibasicdevice-modelurl.md)                                              | Ruft die Modell-URL des Geräts ab.<br/>                                                                                   |
| [**PhysicalAddresses**](ibasicdevice-physicaladdresses.md)                            | Gibt einen Vektor physischer Adressen zurück.<br/>                                                                             |
| [**PresentationUrl**](ibasicdevice-presentationurl.md)                                | Ruft die Präsentations-URL des Geräts ab.<br/>                                                                            |
| [**RemoteStreamingUrls**](ibasicdevice-remotestreamingurls.md)                        | Gibt einen Vektor von Remotestreaming-URLs zurück.<br/>                                                                          |
| [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) | Aufheben der Registrierung eines Ereignishandlers für das [**ConnectionStatusChanged-Ereignis.**](connectionstatuschanged.md)<br/>              |
| [**Serialnumber**](ibasicdevice-serialnumber.md)                                      | Ruft die Seriennummer des Geräts ab.<br/>                                                                               |
| [**type**](ibasicdevice-type.md)                                                      | Ruft einen Enumerationswert ab, der den Gerätetyp des DLNA-Geräts angibt.<br/>                                       |
| [**UniqueDeviceName**](ibasicdevice-uniquedevicename.md)                              | Ruft den eindeutigen Gerätenamen (UDN) des Geräts ab.<br/>                                                                    |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

