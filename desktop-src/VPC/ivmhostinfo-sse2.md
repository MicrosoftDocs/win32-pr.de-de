---
title: IVMHostInfo SSE2-Eigenschaft (VPCCOMInterfaces.h)
description: Bestimmt, ob der Prozessor den SSE2-Anweisungssatz unterstützt. | IVMHostInfo SSE2-Eigenschaft (VPCCOMInterfaces.h)
ms.assetid: 1db5583c-fb8e-400e-87d3-3c4309696307
keywords:
- SSE2-Eigenschaft Virtueller PC
- SSE2-Eigenschaft Virtueller PC, IVMHostInfo-Schnittstelle
- IVMHostInfo-Schnittstelle Virtueller PC, SSE2-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE2
- IVMHostInfo.get_SSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e8edd30f7821ed8ea0daafade504a5194bf2a2583c1a36e5bb10831ef63f29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959120"
---
# <a name="ivmhostinfosse2-property"></a>IVMHostInfo::SSE2-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Bestimmt, ob der Prozessor den SSE2-Anweisungssatz unterstützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a>Eigenschaftswert

**TRUE,** wenn SSE2-Anweisungen vom Hostprozessor unterstützt werden, **andernfalls FALSE.**

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

