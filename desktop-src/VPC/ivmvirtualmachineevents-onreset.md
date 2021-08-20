---
title: IVMVirtualMachineEvents OnReset-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass ein virtueller Computer zurückgesetzt wurde.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- OnReset-Methode Virtueller PC
- OnReset-Methode Virtueller PC, IVMVirtualMachineEvents-Schnittstelle
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC, OnReset-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4101885469de59a7cd2740dc07db44101ce130df037540306f4afdab78c80fd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122903"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a>IVMVirtualMachineEvents::OnReset-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass ein virtueller Computer zurückgesetzt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnReset();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn der virtuelle Computer zurückgesetzt wurde. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um Benachrichtigungen über das Ereignis vmVirtualMachineEvent Reset zu erhalten, das \_ von [**IVMVirtualMachine**](ivmvirtualmachine.md)stammt.

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

 

