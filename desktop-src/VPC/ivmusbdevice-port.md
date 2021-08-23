---
title: IVMUSBDevice Port-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft den Bezeichner des Ports ab, an dem das Gerät verbunden ist.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Porteigenschaft Virtueller PC
- Porteigenschaft Virtual PC, IVMUSBDevice-Schnittstelle
- IVMUSBDevice-Schnittstelle Virtueller PC, Port-Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5b564f1e8c75ecbf5bb140d17218df83bc5b23f5de219c819dc5c4f31f7be14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998710"
---
# <a name="ivmusbdeviceport-property"></a>IVMUSBDevice::P ort-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Bezeichner des Ports ab, an dem das Gerät verbunden ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Portbezeichner. Dieser Wert wird vom USB-Connectortreiber zugewiesen.

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

 

