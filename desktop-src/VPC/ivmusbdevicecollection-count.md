---
title: Ivmusbdevicecollection Count-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der USB-Geräte in dieser Sammlung ab.
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmusbdebug ecollection-Schnittstelle
- Ivmusbdebug Interface Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477049"
---
# <a name="ivmusbdevicecollectioncount-property"></a>Ivmusbdebug:: count (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Anzahl der USB-Geräte in dieser Sammlung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der USB-Geräte.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>        |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



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

[**Ivmusbde vicecollection**](ivmusbdevicecollection.md)
</dt> </dl>

 

