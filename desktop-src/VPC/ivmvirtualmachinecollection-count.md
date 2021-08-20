---
title: IVMVirtualMachineCollection Count-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Anzahl der virtuellen Computer in dieser Sammlung ab.
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Count-Eigenschaft Virtueller PC
- Count-Eigenschaft Virtual PC, IVMVirtualMachineCollection-Schnittstelle
- IVMVirtualMachineCollection-Schnittstelle Virtueller PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7012b6cb60af21b79c2daeb082755975810208e75d949160962525d450966546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118843293"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a>IVMVirtualMachineCollection::Count (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Anzahl der virtuellen Computer in dieser Sammlung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der virtuellen Computer.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                           |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                  |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection ist als 59f31786-2a3d-4fbf-9896-d85338ca0da1 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)
</dt> </dl>

 

