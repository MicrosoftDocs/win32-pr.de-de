---
title: Ivmvirtualpc-Eigenschaft ("upccominterfaces. h")
description: Eine Aufzähl Bare Auflistung aller USB-Geräte, die mit dem Host verbunden sind.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- Die Eigenschaft "" für den virtuellen PC
- Eigenschaften von "" "" "" "" "".
- Ivmvirtualpc Interface Virtual PC, Eigenschaft "-BDE vicecollection"
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0428862cdd53ef6e657624d5dbd3e15c2445042f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742040"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a>Ivmvirtualpc:: aufbdebug ecollection (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft eine Aufzähl Bare Auflistung aller mit dem Host verbundenen USB-Geräte ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Verweis auf einen [**ivmusbtovicecollection**](ivmusbdevicecollection.md) -Zeiger, der eine Auflistung von [**ivmusbdevice**](ivmusbdevice.md) -Objekten darstellt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                                | Bedeutung                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                   | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                                     | Der-Parameter ist **null**.<br/>                                                           |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                             | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>VM \_ E \_ USB- \_ Enumeration Fehler \_ \_ Weitere \_ Geräte</dt> <dt>0xa0040930</dt> </dl> | Es sind mehr als 16 USB-Geräte mit dem Host verbunden.<br/>                                  |
| <dl> <dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt> </dl>      | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpc**](ivmvirtualpc.md)
</dt> </dl>

 

