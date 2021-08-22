---
title: IVMVirtualMachine DiscardUndoDisks-Methode (VPCCOMInterfaces.h)
description: Verwirft die virtuellen Rückgängigdatenträger.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- DiscardUndoDisks-Methode Virtueller PC
- DiscardUndoDisks-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC , DiscardUndoDisks-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997019bf25b4bcc37266c1ba39d5b1420ae44b800127f3e91bc5d9fcb4b76691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471942"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a>IVMVirtualMachine::D iscardUndoDisks-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Verwirft die virtuellen Rückgängigdatenträger.

## <a name="syntax"></a>Syntax


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                            | Beschreibung                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | Der Vorgang wurde durchgeführt.<br/>                                                                        |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | Die Konfiguration ist unbekannt.<br/>                                                                        |
| <dl> <dt>**VM \_ \_E-VM, \_ AUF DER 0XA004020B AUSGEFÜHRT ODER GESPEICHERT \_ \_ WIRD**</dt> <dt></dt> </dl> | Die virtuellen Rückgängigdatenträger können nicht verworfen werden, während der virtuelle Computer ausgeführt wird oder sich in einem gespeicherten Zustand befindet.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

