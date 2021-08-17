---
title: IVMVirtualPC-UpTime-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Anzahl der Sekunden ab, die die Windows Virtual PC-Anwendung ausgeführt wurde.
ms.assetid: 3007a961-2e8c-4674-aab6-4424d0d73eca
keywords:
- UpTime-Eigenschaft Virtueller PC
- UpTime-Eigenschaft Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, UpTime-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualPC.UpTime
- IVMVirtualPC.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff1d71777db92ba84905fd1908d0c0334d098479ce4210c7407ee129c609ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752009"
---
# <a name="ivmvirtualpcuptime-property"></a>IVMVirtualPC::UpTime-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Anzahl der Sekunden ab, die die Windows Virtual PC-Anwendung ausgeführt wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl von Sekunden, in denen die Windows Virtual PC-Anwendung ausgeführt wurde.

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
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

