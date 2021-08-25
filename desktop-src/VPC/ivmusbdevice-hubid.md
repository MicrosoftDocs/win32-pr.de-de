---
title: IVMUSBDevice HubID-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft den Bezeichner des Hubs ab, mit dem das Gerät verbunden ist.
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- HubID-Eigenschaft Virtueller PC
- HubID-Eigenschaft Virtual PC, IVMUSBDevice-Schnittstelle
- IVMUSBDevice-Schnittstelle Virtueller PC, HubID-Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d36047722206c2dfd52f4fc14c8e98270db4cab2d62f0694ea3f44bac10449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958709"
---
# <a name="ivmusbdevicehubid-property"></a>IVMUSBDevice::HubID (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Bezeichner des Hubs ab, mit dem das Gerät verbunden ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Hubbezeichner. Dieser Wert wird vom USB-Connectortreiber zugewiesen.

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
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice ist als 63C1258C-5721-4070-B86B-A6CE2AFEC0B3 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

