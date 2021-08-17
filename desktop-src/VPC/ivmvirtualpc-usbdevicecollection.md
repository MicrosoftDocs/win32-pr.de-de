---
title: IVMVirtualPC USBDeviceCollection-Eigenschaft (VPCCOMInterfaces.h)
description: Eine aufzählbare Sammlung aller USB-Geräte, die mit dem Host verbunden sind.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- USBDeviceCollection-Eigenschaft Virtueller PC
- USBDeviceCollection-Eigenschaft Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, USBDeviceCollection-Eigenschaft
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
ms.openlocfilehash: 2880a6f7adb60605e37fe78481613016d17fdbbd2e27f1a6add4ce031030deea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136523"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a>IVMVirtualPC::USBDeviceCollection-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft eine aufzählbare Sammlung aller USB-Geräte ab, die mit dem Host verbunden sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Verweis auf einen [**IVMUSBDeviceCollection-Zeiger,**](ivmusbdevicecollection.md) der eine Auflistung von [**IVMUSBDevice-Objekten**](ivmusbdevice.md) darstellt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                                | Bedeutung                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                   | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                                     | Der Parameter ist **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                             | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>VM \_ E \_ USB ENUMERATION FAILED MORE \_ \_ \_ \_ DEVICES</dt> <dt>0xA0040930</dt> </dl> | Mehr als 16 USB-Geräte sind mit dem Host verbunden.<br/>                                  |
| <dl> <dt>VM \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED</dt> <dt>0xA0040951</dt> </dl>      | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

