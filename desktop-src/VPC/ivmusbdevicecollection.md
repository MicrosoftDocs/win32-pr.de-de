---
title: Ivmusbdevicecollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung von USB-Geräten, die mit dem Host System verbunden sind. Wenn Sie ein ivmusbdebug-Objekt abrufen möchten, verwenden Sie die ivmvirtualpc-Eigenschaft.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Ivmusbdebug-Schnittstelle virtueller PC
- Ivmusbdebug Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341003"
---
# <a name="ivmusbdevicecollection-interface"></a>Ivmusbdebug ecollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Sammlung von USB-Geräten, die mit dem Host System verbunden sind. Verwenden Sie zum Abrufen eines **ivmusbdebug** -Objekts die [**ivmvirtualpc::**](ivmvirtualpc-usbdevicecollection.md) Start-Eigenschaft.

## <a name="members"></a>Member

Die **ivmusbdebug** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmusbdebug ecollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmusbdecodecollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                        | Zugriffstyp          | BESCHREIBUNG                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmusbdevicecollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                        |
| [**Countdown**](ivmusbdevicecollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der USB-Geräte in dieser Sammlung.<br/>                            |
| [**Element**](ivmusbdevicecollection-item.md)<br/>          | Schreibgeschützt<br/> | Das USB-Geräte Objekt, das dem angegebenen Index (1-basiert) entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmusbdevicecollection ist als 4f-cd6a5--ID definiert. d1c-9s4d-e90abb8b3749<br/>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmusbdevice**](ivmusbdevice.md)
</dt> <dt>

[**Ivmvirtualpc:: Start Message**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

