---
title: Ivmvirtualmachineevents onhardplefault-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass ein virtueller Computer einen dreifachen Fehler verursacht hat.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- Onseriplefault-Methode virtueller PC
- Onseriplefault-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onseriplefault-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d635b9009ecadecb7aed4a921a9c609ef69505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518563"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a>Ivmvirtualmachineevents:: onhardplefault-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass ein virtueller Computer einen dreifachen Fehler verursacht hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn ein virtueller Computer einen dreifachen Fehler aufweist. Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das vmvirtualmachineevent-Ereignis vom Typ "vmvirtualmachineevent" zu erhalten, das \_ von [**ivmvirtualmachine**](ivmvirtualmachine.md)

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

 

