---
title: Ivmtask Cancel-Methode (vpccominterfaces. h)
description: Bricht die Aufgabe ab.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Methode "Virtual PC Abbrechen"
- Cancel-Methode Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, Cancel-Methode
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341237"
---
# <a name="ivmtaskcancel-method"></a>Ivmtask:: Cancel-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Bricht die Aufgabe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen </dl>            | Die Aufgabe kann nicht abgebrochen werden.<br/>      |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmtask**](ivmtask.md)
</dt> </dl>

 

