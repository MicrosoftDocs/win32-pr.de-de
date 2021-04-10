---
title: Ivmvirtualpc maximumserialportspervm-Eigenschaft (vpccominterfaces. h)
description: Hiermit wird die maximale Anzahl von seriellen Anschlüssen pro virtuellem Computer abgerufen.
ms.assetid: e7b874df-105e-4ca8-90ec-2368071dafa0
keywords:
- Maximumserialportspervm-Eigenschaft virtueller PC
- Maximumserialportspervm-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, maximumserialportspervm (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumSerialPortsPerVM
- IVMVirtualPC.get_MaximumSerialPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63aa00c56add6bc48f4c33626a84a854b025c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102790"
---
# <a name="ivmvirtualpcmaximumserialportspervm-property"></a>Ivmvirtualpc:: maximumserialportspervm (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Hiermit wird die maximale Anzahl von seriellen Anschlüssen pro virtuellem Computer abgerufen.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MaximumSerialPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a>Eigenschaftswert

Die maximale Anzahl von seriellen Anschlüssen pro virtuellem Computer.

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

 

