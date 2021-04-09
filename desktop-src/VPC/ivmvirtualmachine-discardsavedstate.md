---
title: Methode ' ivmvirtualmachine verwerdsavedstate ' (vpccominterfaces. h)
description: Verwirft alle gespeicherten Zustandsinformationen für eine gespeicherte virtuelle Maschine.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- Verwerdsavedstate-Methode, Virtual PC
- Verwerdsavedstate-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, verwerdsavedstate-Methode
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
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040737"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a>Ivmvirtualmachine::D iscardsavedstate-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Verwirft alle gespeicherten Zustandsinformationen für eine gespeicherte virtuelle Maschine.

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
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>           | Die Konfiguration ist unbekannt.<br/>                               |
| <dl> <dt>**VM \_ E \_ VM \_**</dt> mit <dt>0xa0040500</dt> </dl>           | Der virtuelle Computer wird ausgeführt.<br/>                             |
| <dl> <dt>**VM \_ E \_ VM \_ nicht \_ gespeicherten \_ Status**</dt> <dt>0xa00400501</dt> </dl> | Der virtuelle Computer wird nicht ausgeführt, hat aber keinen gespeicherten Zustand.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>           | Ein unerwarteter Fehler ist aufgetreten.<br/>                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

