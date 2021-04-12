---
title: Ivmvirtualpc maximumfloppydrivespervm-Eigenschaft (vpccominterfaces. h)
description: Hiermit wird die maximale Anzahl von Diskettenlaufwerken pro virtuellem Computer abgerufen.
ms.assetid: f0dc351b-73de-4b6b-a953-5d5b683c4e31
keywords:
- Maximumfloppydrivespervm-Eigenschaft virtueller PC
- Maximumfloppydrivespervm-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, maximumfloppydrivespervm (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumFloppyDrivesPerVM
- IVMVirtualPC.get_MaximumFloppyDrivesPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecc0d672affce5364e1658d5198681268109a1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105639"
---
# <a name="ivmvirtualpcmaximumfloppydrivespervm-property"></a>Ivmvirtualpc:: maximumfloppydrivespervm-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Hiermit wird die maximale Anzahl von Diskettenlaufwerken pro virtuellem Computer abgerufen.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MaximumFloppyDrivesPerVM(
  [out, retval] long *maxDrives
);
```



## <a name="property-value"></a>Eigenschaftswert

Die maximale Anzahl von Diskettenlaufwerken pro virtuellem Computer.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                           | Bedeutung                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                                | Der-Parameter ist **null**.<br/>                                                           |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt> </dl> | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |



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

 

