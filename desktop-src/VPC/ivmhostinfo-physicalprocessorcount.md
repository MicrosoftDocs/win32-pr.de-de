---
title: IVMHostInfo PhysicalProcessorCount-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Anzahl der physischen Prozessoren auf dem Hostcomputer ab.
ms.assetid: b8f805a6-2962-4a48-94e9-bd76220974f0
keywords:
- PhysicalProcessorCount-Eigenschaft Virtueller PC
- PhysicalProcessorCount-Eigenschaft Virtueller PC, IVMHostInfo-Schnittstelle
- IVMHostInfo-Schnittstelle Virtueller PC, PhysicalProcessorCount-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.PhysicalProcessorCount
- IVMHostInfo.get_PhysicalProcessorCount
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce989392825261ecc0e898e2632f4556bc4023f9e8ad54c4b2de8cfaf5ad1bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123720"
---
# <a name="ivmhostinfophysicalprocessorcount-property"></a>IVMHostInfo::P hysicalProcessorCount-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Anzahl der physischen Prozessoren auf dem Hostcomputer ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_PhysicalProcessorCount(
  [out, retval] long *processorCount
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der physischen Prozessoren.

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
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

