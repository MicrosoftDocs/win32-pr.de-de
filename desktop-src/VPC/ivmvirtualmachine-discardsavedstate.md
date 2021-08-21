---
title: IVMVirtualMachine DiscardSavedState-Methode (VPCCOMInterfaces.h)
description: Verwirft alle gespeicherten Zustandsinformationen für einen gespeicherten virtuellen Computer.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- DiscardSavedState-Methode – Virtueller PC
- DiscardSavedState-Methode Virtual PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC, DiscardSavedState-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff30406328ae13004505440ae2fb8b18b2e1fdf8ac19dcbfbe77b063e54df688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471980"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a>IVMVirtualMachine::D iscardSavedState-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Verwirft alle gespeicherten Zustandsinformationen für einen gespeicherten virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                           | BESCHREIBUNG                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                 | Der Vorgang wurde durchgeführt.<br/>                               |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>           | Die Konfiguration ist unbekannt.<br/>                               |
| <dl> <dt>**VM \_ E \_ VM \_ RUNNING**</dt> <dt>0xA0040500</dt> </dl>           | Der virtuelle Computer wird ausgeführt.<br/>                             |
| <dl> <dt>**VM \_ E \_ VM NO SAVED STATE \_ \_ \_ 0XA00400501**</dt> <dt></dt> </dl> | Der virtuelle Computer wird nicht ausgeführt, hat aber keinen gespeicherten Zustand.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>           | Ein unerwarteter Fehler ist aufgetreten.<br/>                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

