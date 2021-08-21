---
title: IVMVirtualMachineEvents OnHeartbeatStopped-Methode (VPCCOMInterfaces.h)
description: Empfängt die Benachrichtigung, dass der Heartbeat eines virtuellen Computers beendet wurde.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- OnHeartbeatStopped-Methode Virtueller PC
- OnHeartbeatStopped-Methode Virtual PC , IVMVirtualMachineEvents-Schnittstelle
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC, OnHeartbeatStopped-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad4af982899f2f5f5dce6d78569323fbb6a85168c81b7c88c3ee0c62b3a39f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056588"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a>IVMVirtualMachineEvents::OnHeartbeatStopped-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt die Benachrichtigung, dass der Heartbeat eines virtuellen Computers beendet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn das Gastbetriebssystem für diesen virtuellen Computer plötzlich beendet wurde. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das Ereignis vmVirtualMachineEvent HeartbeatStopped zu erhalten, das \_ von [**IVMVirtualMachine**](ivmvirtualmachine.md)stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents ist als 9d84f560-bb67-4961-bd12-a4da780c67e4 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

