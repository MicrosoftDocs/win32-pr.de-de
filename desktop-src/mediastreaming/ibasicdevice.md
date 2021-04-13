---
title: Ibasicdevice-Schnittstelle
description: Kapselt die Methoden und Ereignisse, die erforderlich sind, um ein DLNA-Gerät zu modellieren.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- Ibasicdevice-Schnittstelle Medien Streaming-API
- Ibasicdevice-Schnittstelle Medien Streaming-API, beschrieben
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104391207"
---
# <a name="ibasicdevice-interface"></a>Ibasicdevice-Schnittstelle

Kapselt die Methoden und Ereignisse, die erforderlich sind, um ein DLNA-Gerät zu modellieren.

## <a name="members"></a>Member

Die **ibasicdevice** -Schnittstelle erbt von [**iinspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable). **Ibasicdevice** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ibasicdevice** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                 | BESCHREIBUNG                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**\_connectionstatuschge hinzufügen**](ibasicdevice-add-connectionstatuschanged.md)       | Registriert einen Ereignishandler für das [**connectionstatuschangi-Ereignis**](connectionstatuschanged.md) .<br/>                |
| [**Canwake-Geräte**](ibasicdevice-canwakedevices.md)                                  | Ruft einen Wert ab, der angibt, ob das Gerät aktiviert werden kann.<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | Gibt einen-Enumerationswert zurück, der angibt, ob das Gerät derzeit online, offline oder im Ruhezustand ist, aber wach stellbar ist.<br/> |
| [**Beschreibung**](ibasicdevice-description.md)                                        | Ruft eine Beschreibung des Geräts ab.<br/>                                                                              |
| [**Discoveredoncurrentnetwork**](ibasicdevice-discoveredoncurrentnetwork.md)          | Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.<br/>                                           |
| [**FriendlyName**](ibasicdevice-friendlyname.md)                                      | Ruft den anzeigen amen des Geräts ab.<br/>                                                                               |
| [**Icons**](ibasicdevice-icons.md)                                                    | Gibt einen Vektor von [**ideviceicon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) -Schnittstellen zurück.<br/>                                                  |
| [**IpAddresses**](ibasicdevice-ipaddresses.md)                                        | Gibt einen Vektor von IP-Adressen zurück.<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | Ruft den Herstellernamen des Geräts ab.<br/>                                                                           |
| [**ManufacturerUrl**](ibasicdevice-manufacturerurl.md)                                | Ruft die Hersteller-URL des Geräts ab.<br/>                                                                            |
| [**ModelName**](ibasicdevice-modelname.md)                                            | Ruft den Modellnamen des Geräts ab.<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | Ruft die Modellnummer des Geräts ab.<br/>                                                                                |
| [**Modelurl**](ibasicdevice-modelurl.md)                                              | Ruft die Modell-URL des Geräts ab.<br/>                                                                                   |
| [**Physicaladressen**](ibasicdevice-physicaladdresses.md)                            | Gibt einen Vektor physischer Adressen zurück.<br/>                                                                             |
| [**Presentationurl**](ibasicdevice-presentationurl.md)                                | Ruft die Präsentations-URL des Geräts ab.<br/>                                                                            |
| [**Remotestreamingurls**](ibasicdevice-remotestreamingurls.md)                        | Gibt einen Vektor von Remotestreaming-URLs zurück.<br/>                                                                          |
| [**\_connectionstatuschge entfernen**](ibasicdevice-remove-connectionstatuschanged.md) | Hebt die Registrierung eines Ereignis Handlers für das [**connectionstatuschge**](connectionstatuschanged.md) -Ereignis auf.<br/>              |
| [**SerialNumber**](ibasicdevice-serialnumber.md)                                      | Ruft die Seriennummer des Geräts ab.<br/>                                                                               |
| [**type**](ibasicdevice-type.md)                                                      | Ruft einen Enumerationswert ab, der den Gerätetyp des DLNA-Geräts angibt.<br/>                                       |
| [**Uniquedevicename**](ibasicdevice-uniquedevicename.md)                              | Ruft den eindeutigen Gerätenamen (User Name, udn) des Geräts ab.<br/>                                                                    |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

