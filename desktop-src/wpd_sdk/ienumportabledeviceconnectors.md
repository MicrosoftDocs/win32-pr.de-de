---
description: Unterstützt die Enumeration von IPortableDeviceConnector-Schnittstellen, die MTP-/Bluetooth-Geräte darstellen, die mit dem PC gekoppelt wurden.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: IEnumPortableDeviceConnectors-Schnittstelle (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 024d9a813cb20a511c1c23a414625aa78416c530521777ab2c1abaab1c4b4bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117652754"
---
# <a name="ienumportabledeviceconnectors-interface"></a>IEnumPortableDeviceConnectors-Schnittstelle

Die **IEnumPortableDeviceConnectors-Schnittstelle** unterstützt die Enumeration von [**IPortableDeviceConnector-Schnittstellen,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) die MTP/Bluetooth-Geräte darstellen, die mit dem PC gekoppelt wurden. Beachten Sie, dass dadurch alle zuvor gekoppelten Geräte abgerufen werden, einschließlich geräte, die gekoppelt, aber getrennt sind. Um festzustellen, ob ein Gerät noch verbunden ist, fragen Sie die **DEVPKEY \_ MTPBTH \_ IsConnected-Eigenschaft** für dieses Gerät ab.

## <a name="members"></a>Member

Die **IEnumPortableDeviceConnectors-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumPortableDeviceConnectors** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEnumPortableDeviceConnectors-Schnittstelle** verfügt über diese Methoden.



| Methode                                               | Beschreibung                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](ienumportabledeviceconnectors-clone.md) | Erstellt eine Kopie der aktuellen **IEnumPortableDeviceConnectors-Schnittstelle.**<br/>                                                       |
| [**Weiter**](ienumportabledeviceconnectors-next.md)   | Ruft das nächste oder mehrere [**IPortableDeviceConnector-Objekte**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) in der Enumerationssequenz ab.<br/> |
| [**Zurücksetzen**](ienumportabledeviceconnectors-reset.md) | Setzt die Enumerationsfolge auf den Anfang zurück.<br/>                                                                                |
| [**Überspringen**](ienumportabledeviceconnectors-skip.md)   | Überspringt die angegebene Anzahl von Geräten in der Enumerationssequenz.<br/>                                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



 

