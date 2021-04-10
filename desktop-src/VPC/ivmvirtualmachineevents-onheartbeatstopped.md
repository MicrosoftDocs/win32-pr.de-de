---
title: Ivmvirtualmachineevents onheartbeatbeendete-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass der Takt einer virtuellen Maschine beendet wurde.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- Onheartbeatbeendete-Methode Virtual PC
- Onheartbeatbeendete-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onheartbeatbeendete-Methode
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
ms.openlocfilehash: 1ade783d2d182439d5c500dcc114c74c8278ba6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956951"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a>Ivmvirtualmachineevents:: onheartbeatbeendete-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass der Takt einer virtuellen Maschine beendet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn das Gast Betriebssystem für diesen virtuellen Computer abrupt beendet wurde. Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das \_ vom [**ivmvirtualmachine**](ivmvirtualmachine.md)-Ereignis empfangene vmvirtualmachineevent heartbeatbeendeten-Ereignis zu erhalten.

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

 

