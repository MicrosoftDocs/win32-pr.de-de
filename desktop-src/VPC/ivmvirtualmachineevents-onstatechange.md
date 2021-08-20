---
title: IVMVirtualMachineEvents OnStateChange-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass sich der Zustand eines virtuellen Computers geändert hat. | IVMVirtualMachineEvents OnStateChange-Methode (VPCCOMInterfaces.h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- OnStateChange-Methode Virtueller PC
- OnStateChange-Methode Virtual PC , IVMVirtualMachineEvents-Schnittstelle
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC, OnStateChange-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf966d2439f3095051331b5412bc92cca9ba76e6f98c9777402ba449f2e7f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122700"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a>IVMVirtualMachineEvents::OnStateChange-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass sich der Zustand eines virtuellen Computers geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualMachineState* \[ In\]
</dt> <dd>

Der neue Status des virtuellen Computers. Eine Liste der Werte finden Sie unter [**VMVMState**](vmvmstate.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn sich der Zustand für diesen virtuellen Computer ändert. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das Ereignis vmVirtualMachineEvent StateChanged zu erhalten, das \_ von [**IVMVirtualMachine**](ivmvirtualmachine.md)stammt.

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

 

