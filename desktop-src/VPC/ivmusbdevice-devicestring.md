---
title: Ivmusbdevice devicestring-Eigenschaft (vpccominterfaces. h)
description: Ruft den Namen des USB-Geräts ab.
ms.assetid: 2ae82e2a-b33a-4039-acdb-958b094b1045
keywords:
- Devicestring-Eigenschaft virtueller PC
- Devicestring-Eigenschaft Virtual PC, ivmusbdevice-Schnittstelle
- Ivmusbdevice Interface Virtual PC, devicestring (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceString
- IVMUSBDevice.get_DeviceString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ed76f55f5b1218db70991f5917edf6d5b7b655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858952"
---
# <a name="ivmusbdevicedevicestring-property"></a>Ivmusbdevice::D Eigenschaft "evicestring"

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Namen des USB-Geräts ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DeviceString(
  [out, retval] BSTR *deviceName
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des USB-Geräts.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                            | Bedeutung                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | Die Methode wurde erfolgreich abgeschlossen.<br/> |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl> | Der-Parameter ist **null**.<br/>         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmusbdevice ist als 63c1258c-5721-4070-B86B-A6CE2AFEC0B3 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmusbdevice**](ivmusbdevice.md)
</dt> </dl>

 

