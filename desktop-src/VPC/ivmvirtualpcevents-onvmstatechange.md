---
title: Ivmvirtualpcevents onvmstatechange-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat. | Ivmvirtualpcevents onvmstatechange-Methode (vpccominterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Onvmstatechange-Methode Virtual PC
- Onvmstatechange-Methode Virtual PC, ivmvirtualpcevents-Schnittstelle
- Ivmvirtualpcevents Interface Virtual PC, onvmstatechange-Methode
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
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363927"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>Ivmvirtualpcevents:: onvmstatechange-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass sich der Zustand einer virtuellen Maschine geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*virtualmachineconfig* \[ in\]
</dt> <dd>

Der Name des virtuellen Computers.

</dd> <dt>

*virtualmachinestate* \[ in\]
</dt> <dd>

Der neue Zustand der virtuellen Maschine.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das **\_ vmstatechanged** -Ereignis von [**ivmvirtualpc**](ivmvirtualpc.md)empfangen zu können. Um einen bestimmten virtuellen Computer zu überwachen, verwenden Sie die [**ivmvirtualmachineevents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmvirtualpcevents ist als efed1ef1-3c09-41f7-a9c2-7e29fa286c9d definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpcevents**](ivmvirtualpcevents.md)
</dt> </dl>

 

