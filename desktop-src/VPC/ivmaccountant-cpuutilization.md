---
title: IVMAccountant CPUUtilization-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft den Prozentsatz der aktuellen CPU-Auslastung für diesen virtuellen Computer ab.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- CPUUtilization-Eigenschaft Virtueller PC
- CPUUtilization-Eigenschaft Virtueller PC, IVMAccountant-Schnittstelle
- IVMAccountant-Schnittstelle Virtueller PC, CPUUtilization-Eigenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba54d7ec3a3fc447a49e9a72addd72fc5e3929b486c8fd4271276a40a7041f4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007308"
---
# <a name="ivmaccountantcpuutilization-property"></a>IVMAccountant::CPUUtilization-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den Prozentsatz der aktuellen CPU-Auslastung für diesen virtuellen Computer ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Prozentsatz der aktuellen CPU-Auslastung.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>       |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | Der virtuelle Computer wird nicht ausgeführt.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant ist als 6376c067-7f57-4d63-b754-06e2e4f51d73 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

