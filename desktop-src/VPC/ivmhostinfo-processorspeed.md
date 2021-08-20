---
title: IVMHostInfo ProcessorSpeed-Eigenschaft (VPCCOMInterfaces.h)
description: Geschwindigkeit des Hostprozessors in Megahertz (MHz) oder Gigahertz (GHz).
ms.assetid: 2d5e3f2e-8e81-4527-bd7f-52bf5b1f56ef
keywords:
- ProcessorSpeed-Eigenschaft Virtueller PC
- ProcessorSpeed-Eigenschaft Virtueller PC, IVMHostInfo-Schnittstelle
- IVMHostInfo-Schnittstelle Virtueller PC, ProcessorSpeed-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeed
- IVMHostInfo.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4257e62b98c595fc9bd5e1580c585eb1a469d4f833ec32c6c8c7a13caf64bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123732"
---
# <a name="ivmhostinfoprocessorspeed-property"></a>IVMHostInfo::P rocessorSpeed-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Geschwindigkeit des Hostprozessors in Megahertz (MHz) oder Gigahertz (GHz) ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Prozessorgeschwindigkeit in Megahertz oder Gigahertz.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

