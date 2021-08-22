---
title: IVMUSBDevice DeviceClass-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Geräteklasse des USB-Geräts ab.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- DeviceClass-Eigenschaft Virtueller PC
- DeviceClass-Eigenschaft Virtueller PC, IVMUSBDevice-Schnittstelle
- IVMUSBDevice-Schnittstelle Virtueller PC, DeviceClass-Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f192c81e8dff1d0b1f124393c9eceb9f6268ac43043337399dedb9cdcbebb3be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006910"
---
# <a name="ivmusbdevicedeviceclass-property"></a>IVMUSBDevice::D eviceClass-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Geräteklasse des USB-Geräts ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Geräteklasse. Eine Liste der Werte finden Sie unter [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                            | Bedeutung                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | Die Methode wurde erfolgreich abgeschlossen.<br/> |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl> | Der Parameter ist **NULL.**<br/>         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice ist als 63C1258C-5721-4070-B86B-A6CE2AFEC0B3 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

