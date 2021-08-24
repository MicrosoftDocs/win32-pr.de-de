---
title: IVMVirtualPC SuggestedMaximumMemoryPerVM-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die empfohlene maximal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte ab, um bedingungen mit geringem Arbeitsspeicher auf dem Host zu vermeiden.
ms.assetid: 533cca40-f41d-4717-87ae-d8072414a637
keywords:
- SuggestedMaximumMemoryPerVM-Eigenschaft Virtueller PC
- SuggestedMaximumMemoryPerVM-Eigenschaft Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , SuggestedMaximumMemoryPerVM-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualPC.SuggestedMaximumMemoryPerVM
- IVMVirtualPC.get_SuggestedMaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb2a14ad6d48c3d156ebffd6ea0c5ae6c4cd52f94790152d373fdc7cf47e118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768040"
---
# <a name="ivmvirtualpcsuggestedmaximummemorypervm-property"></a>IVMVirtualPC::SuggestedMaximumMemoryPerVM-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die empfohlene maximal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte ab, um bedingungen mit geringem Arbeitsspeicher auf dem Host zu vermeiden.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SuggestedMaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Eigenschaftswert

Die empfohlene maximal zulässige Menge an physischem Arbeitsspeicher pro virtuellem Computer in Megabyte.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                           | Bedeutung                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                                | Der Parameter ist **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>VM \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED</dt> <dt>0xA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

