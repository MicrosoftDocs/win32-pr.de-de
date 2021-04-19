---
title: Ivmdvddrive busnumber-Eigenschaft (vpccominterfaces. h)
description: Ruft die Busnummer ab, an die dieses Gerät angefügt wird.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Busnumber-Eigenschaft virtueller PC
- Busnumber-Eigenschaft Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, busnumber-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345314"
---
# <a name="ivmdvddrivebusnumber-property"></a>Ivmdvddrive:: busnumber (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Busnummer ab, an die dieses Gerät angefügt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Busnummer. Beispielsweise würde dieser Wert auf einem IDE-Bus entweder den primären oder den sekundären Standort darstellen.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                       | Bedeutung                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | Der Vorgang wurde durchgeführt.<br/>                                          |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>            | Der-Parameter ist **null**.<br/>                                             |
| <dl> <dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt> </dl> | Der Busstandort für dieses DVD-Laufwerk wurde nicht ordnungsgemäß initialisiert.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdvddrive**](ivmdvddrive.md)
</dt> </dl>

 

