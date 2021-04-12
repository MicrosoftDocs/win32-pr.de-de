---
title: Ivmvirtualmachineevents onadditionsavailable-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass Integrations Komponenten auf einem virtuellen Computer verfügbar sind.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- Onadditionsavailable-Methode virtueller PC
- Onadditionsavailable-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onadditionsavailable-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193b44f533079bc957cbb8b297409641814b6e21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478672"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a>Ivmvirtualmachineevents:: onadditionsavailable-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass Integrations Komponenten auf einem virtuellen Computer verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnAdditionsAvailable();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachineevents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

