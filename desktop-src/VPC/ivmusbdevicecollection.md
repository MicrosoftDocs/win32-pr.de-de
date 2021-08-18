---
title: IVMUSBDeviceCollection-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert die Sammlung von USB-Geräten, die an das Hostsystem angeschlossen sind. Um ein IVMUSBDeviceCollection-Objekt zu erhalten, verwenden Sie die IVMVirtualPC USBDeviceCollection-Eigenschaft.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- IVMUSBDeviceCollection-Schnittstelle Virtueller PC
- IVMUSBDeviceCollection-Schnittstelle Virtueller PC , beschrieben
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
ms.openlocfilehash: 1daf5df827bd9d890ede26242957adb2da8a025e8b1d272254e145b12f5aee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752539"
---
# <a name="ivmusbdevicecollection-interface"></a>IVMUSBDeviceCollection-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert die Sammlung von USB-Geräten, die an das Hostsystem angeschlossen sind. Um ein **IVMUSBDeviceCollection-Objekt zu** erhalten, verwenden Sie die [**IVMVirtualPC::USBDeviceCollection-Eigenschaft.**](ivmvirtualpc-usbdevicecollection.md)

## <a name="members"></a>Member

Die **IVMUSBDeviceCollection-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMUSBDeviceCollection** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IVMUSBDeviceCollection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                        | Zugriffstyp          | Beschreibung                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                                        |
| [**Anzahl**](ivmusbdevicecollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der USB-Geräte in dieser Sammlung.<br/>                            |
| [**Element**](ivmusbdevicecollection-item.md)<br/>          | Schreibgeschützt<br/> | Das USB-Geräteobjekt, das dem angegebenen Index entspricht (1-basiert).<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection ist als 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749 definiert.<br/>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

