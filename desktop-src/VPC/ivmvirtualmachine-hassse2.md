---
title: IVMVirtualMachine HasSSE2-Eigenschaft (VPCCOMInterfaces.h)
description: Bestimmt, ob der Prozessor den SSE2-Anweisungssatz unterstützt. | IVMVirtualMachine HasSSE2-Eigenschaft (VPCCOMInterfaces.h)
ms.assetid: da9860cf-d1e4-4dc4-8c4c-1b83104ffbc6
keywords:
- HasSSE2-Eigenschaft Virtueller PC
- HasSSE2-Eigenschaft Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC , HasSSE2-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE2
- IVMVirtualMachine.get_HasSSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f64dde4b075652899d50f4bbb41caafafdd69ec8ea9ea80d3eb165bcf14cafc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592650"
---
# <a name="ivmvirtualmachinehassse2-property"></a>IVMVirtualMachine::HasSSE2-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Bestimmt, ob der Prozessor den SSE2-Anweisungssatz unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_HasSSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a>Eigenschaftswert

**TRUE,** wenn der Prozessor den SSE2-Anweisungssatz unterstützt hat, andernfalls **FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

