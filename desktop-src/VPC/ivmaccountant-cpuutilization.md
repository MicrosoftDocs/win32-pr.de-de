---
title: Ivmaccountant cpunutzungseigenschaft (vpccominterfaces. h)
description: Ruft den Prozentsatz der aktuellen CPU-Auslastung für diesen virtuellen Computer ab.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- Cpunutzungseigenschaft virtueller PC
- Cpunutzungseigenschaft Virtual PC, ivmaccountant-Schnittstelle
- Ivmaccountant Interface Virtual PC, cpunutzungseigenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e38c223f47678cdb9c2d49e06452d014083c94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957127"
---
# <a name="ivmaccountantcpuutilization-property"></a>Ivmaccountant:: cpunutzungseigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Prozentsatz der aktuellen CPU-Auslastung für diesen virtuellen Computer ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Prozentsatz der aktuellen CPU-Auslastung.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>          |
| <dl> <dt>S \_ Falsch</dt> <dt>1</dt> </dl>                    | Der virtuelle Computer wird nicht ausgeführt.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmaccountant**](ivmaccountant.md)
</dt> </dl>

 

