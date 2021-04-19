---
title: Ivmusbdevice-Schnittstelle (vpccominterfaces. h)
description: Definiert die Schnittstelle für ein USB-Gerät, das dem Host zugeordnet ist. Sie können ein USB-Gerät an einen virtuellen Computer anfügen, um das Gerät auf dem virtuellen Computer zu verwenden.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Ivmusbdevice Interface Virtual PC
- Virtueller Computer für ivmusbdevice Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338342"
---
# <a name="ivmusbdevice-interface"></a>Ivmusbdevice-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Schnittstelle für ein USB-Gerät, das dem Host zugeordnet ist. Sie können ein USB-Gerät an einen virtuellen Computer anfügen, um das Gerät auf dem virtuellen Computer zu verwenden.

## <a name="members"></a>Member

Die **ivmusbdevice** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmusbdevice** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmusbdevice** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp          | BESCHREIBUNG                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**"AttachedTo VM"**](ivmusbdevice-attachedtovm.md)<br/>             | Schreibgeschützt<br/> | Der Name des virtuellen Computers, an den das USB-Gerät angefügt wird.<br/> |
| [**DeviceClass**](ivmusbdevice-deviceclass.md)<br/>               | Schreibgeschützt<br/> | Die Geräteklasse des USB-Geräts.<br/>                                  |
| [**Devicestring**](ivmusbdevice-devicestring.md)<br/>             | Schreibgeschützt<br/> | Der Name des USB-Geräts.<br/>                                          |
| [**Hubid**](ivmusbdevice-hubid.md)<br/>                           | Schreibgeschützt<br/> | Der Bezeichner des Hubs, mit dem das Gerät verbunden ist.<br/>          |
| [**Manufacturerstring**](ivmusbdevice-manufacturerstring.md)<br/> | Schreibgeschützt<br/> | Der Name des Herstellers des USB-Geräts.<br/>                             |
| [**Port**](ivmusbdevice-port.md)<br/>                             | Schreibgeschützt<br/> | Der Bezeichner des Ports, mit dem das Gerät verbunden ist.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.<br/>               |



 

