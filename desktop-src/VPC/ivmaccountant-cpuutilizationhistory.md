---
title: IVMAccountant CPUUtilizationHistory-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die aktuelle CPU-Auslastung dieses virtuellen Computers ab (als Array von Prozentwerten).
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- CPUUtilizationHistory-Eigenschaft Virtueller PC
- CPUUtilizationHistory-Eigenschaft Virtueller PC, IVMAccountant-Schnittstelle
- IVMAccountant-Schnittstelle Virtueller PC, CPUUtilizationHistory -Eigenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81014d1f72fa6bb0266ed113f40044b46ba15673aec97fdf763a81f6f22f94c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007290"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a>IVMAccountant::CPUUtilizationHistory (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die aktuelle CPU-Auslastung dieses virtuellen Computers ab (als Array von Prozentwerten).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a>Eigenschaftswert

Die aktuelle CPU-Nutzung dieses virtuellen Computers. Diese Daten werden als Array von 60 Elementen zurückgegeben, die den Prozentsatz der CPU-Auslastung pro Sekunde in der letzten Minute darstellen. Der Variant-Typ ist VT \_ ARRAY \| VT \_ UI1.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                           |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>                                              |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | Der virtuelle Computer wird nicht ausgeführt. Alle 60 Arrayelemente sind auf 0 festgelegt.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant ist als 6376c067-7f57-4d63-b754-06e2e4f51d73 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

