---
title: IVMVirtualPCEvents OnVMStateChange-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass sich der Zustand eines virtuellen Computers geändert hat. | IVMVirtualPCEvents OnVMStateChange-Methode (VPCCOMInterfaces.h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- OnVMStateChange-Methode Virtueller PC
- OnVMStateChange-Methode Virtueller PC, IVMVirtualPCEvents-Schnittstelle
- IVMVirtualPCEvents-Schnittstelle Virtueller PC , OnVMStateChange-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63516e80ce4f3b830229fdb4cd574e95378c0569a4855a73c1c528af2ec8b48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032980"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>IVMVirtualPCEvents::OnVMStateChange-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass sich der Zustand eines virtuellen Computers geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualMachineConfig* \[ In\]
</dt> <dd>

Der Name des virtuellen Computers.

</dd> <dt>

*virtualMachineState* \[ In\]
</dt> <dd>

Der neue Status des virtuellen Computers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das **\_ VMStateChanged-Ereignis vmVirtualPCEvent** zu erhalten, das von [**IVMVirtualPC**](ivmvirtualpc.md)stammt. Verwenden Sie zum Überwachen eines bestimmten virtuellen Computers die [**IVMVirtualMachineEvents::OnStateChange-Methode.**](ivmvirtualmachineevents-onstatechange.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents ist als efed1ef1-3c09-41f7-a9c2-7e29fa286c9d definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

