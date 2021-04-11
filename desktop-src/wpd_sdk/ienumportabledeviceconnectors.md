---
description: Unterstützt die Enumeration von iportabledeviceconnector-Schnittstellen, die MTP/Bluetooth-Geräte darstellen, die mit dem PC gekoppelt wurden.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Ienumportabledeviceconnectors-Schnittstelle (devpkey. h)
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
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216071"
---
# <a name="ienumportabledeviceconnectors-interface"></a>Ienumportabledebug Controller-Schnittstelle

Die **ienumportabledeviceconnectors** -Schnittstelle unterstützt die Enumeration von [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Schnittstellen, die MTP/Bluetooth-Geräte darstellen, die mit dem PC gekoppelt wurden. Beachten Sie, dass dadurch alle zuvor gekoppelten Geräte abgerufen werden, einschließlich Geräte, die gekoppelt, aber nicht getrennt sind. Um festzustellen, ob ein Gerät weiterhin verbunden ist, Fragen Sie die **devpkey-Eigenschaft \_ mtpbth \_ IsConnected** für dieses Gerät ab.

## <a name="members"></a>Member

Die **ienumportabledebug Controller** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienumportabletoviceconnectors** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ienumportabledeviceconnectors** -Schnittstelle verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](ienumportabledeviceconnectors-clone.md) | Erstellt eine Kopie der aktuellen **ienumportabledebug Controller** -Schnittstelle.<br/>                                                       |
| [**Weiter**](ienumportabledeviceconnectors-next.md)   | Ruft das nächste oder mehrere [**iportabledeviceconnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) -Objekte in der enumerationssequenz ab.<br/> |
| [**Zurücksetzen**](ienumportabledeviceconnectors-reset.md) | Setzt die Enumerationsfolge auf den Anfang zurück.<br/>                                                                                |
| [**Überspringen**](ienumportabledeviceconnectors-skip.md)   | Überspringt die angegebene Anzahl von Geräten in der enumerationssequenz.<br/>                                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portablede viceconnectapi. idl</dt> </dl>                                                                |
| Bibliothek<br/>                  | <dl> <dt>Portabledeviceguids. lib</dt> </dl>                                                                     |



 

