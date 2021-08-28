---
title: IVMVirtualPC MaximumParallelPortsPerVM-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die maximale Anzahl paralleler Ports pro virtuellem Computer ab.
ms.assetid: c5baac59-386c-4373-a560-460750178894
keywords:
- MaximumParallelPortsPerVM -Eigenschaft Virtueller PC
- MaximumParallelPortsPerVM-Eigenschaft Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC interface Virtual PC , MaximumParallelPortsPerVM property
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumParallelPortsPerVM
- IVMVirtualPC.get_MaximumParallelPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1449f3a32c606d6a326cb67d3169506408ee47dfc007d22970281c70d0a78b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056548"
---
# <a name="ivmvirtualpcmaximumparallelportspervm-property"></a>IVMVirtualPC::MaximumParallelPortsPerVM (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die maximale Anzahl paralleler Ports pro virtuellem Computer ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MaximumParallelPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a>Eigenschaftswert

Die maximale Anzahl paralleler Ports pro virtuellem Computer.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                           | Bedeutung                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                                | Der Parameter ist **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT</dt> <dt>0XA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

