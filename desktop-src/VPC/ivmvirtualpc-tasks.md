---
title: IVMVirtualPC Tasks-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft eine Auflistung von Aufgaben ab.
ms.assetid: bba9c4b4-c933-43c8-9fbc-f2beb59867cf
keywords:
- Tasks-Eigenschaft Virtueller PC
- Tasks-Eigenschaft Virtual PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, Tasks-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualPC.Tasks
- IVMVirtualPC.get_Tasks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03e0992ff177f33c1f47ac78d0ffec94d59c330b810a796aa78530b9092b71e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056538"
---
# <a name="ivmvirtualpctasks-property"></a>IVMVirtualPC::Tasks-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft eine Auflistung von Aufgaben ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Tasks(
  [out, retval] IVMTaskCollection **taskCollection
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Auflistung von [**IVMTask-Objekten.**](ivmtask.md) Siehe [**IVMTaskCollection**](ivmtaskcollection.md).

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

 

