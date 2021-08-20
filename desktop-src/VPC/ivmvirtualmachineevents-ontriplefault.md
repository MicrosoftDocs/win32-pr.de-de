---
title: IVMVirtualMachineEvents OnTripleFault-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass ein virtueller Computer dreifach fehlerhaft ist.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- 'OnTripleFault-Methode : Virtueller PC'
- OnTripleFault-Methode Virtual PC, IVMVirtualMachineEvents-Schnittstelle
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC, OnTripleFault-Methode
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
ms.openlocfilehash: d9328ceff18256621a590bf0f235aca8ff12b142e4cdedf389d9d270bfde9bad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122690"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a>IVMVirtualMachineEvents::OnTripleFault-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass ein virtueller Computer dreifach fehlerhaft ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn ein virtueller Computer dreifach fehlerhaft ist. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das TripleFault-Ereignis vmVirtualMachineEvent zu erhalten, das von \_ [**IVMVirtualMachine stammt.**](ivmvirtualmachine.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents ist als 9d84f560-bb67-4961-bd12-a4da780c67e4 definiert.<br/>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

