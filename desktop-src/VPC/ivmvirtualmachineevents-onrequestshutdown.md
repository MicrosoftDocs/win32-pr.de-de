---
title: IVMVirtualMachineEvents OnRequestShutdown-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren gestellt wurde.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- 'OnRequestShutdown-Methode: Virtueller PC'
- 'OnRequestShutdown-Methode: Virtueller PC, IVMVirtualMachineEvents-Schnittstelle'
- IVMVirtualMachineEvents-Schnittstelle Virtueller PC, OnRequestShutdown-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929c9a293e760a12ace62766cbd7a0c016980fc2399cdde494402a272d90fe0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123170"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a>IVMVirtualMachineEvents::OnRequestShutdown-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren gestellt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird immer dann aufgerufen, wenn die Sitzung des virtuellen Computers heruntergefahren wird. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das **Ereignis vmVirtualMachineEvent \_ RequestShutdown** zu erhalten, das von [**IVMVirtualMachine stammt.**](ivmvirtualmachine.md)

Diese Ereignisbenachrichtigung wird nur gesendet, wenn die Sitzung der virtuellen Computer gerade heruntergefahren wird. Routinen zum Herunterfahren des Betriebssystems, z. B. [**IVMGuestOS::Shutdown,**](ivmguestos-shutdown.md)führen dieses Ereignis nur dann direkt aus, wenn sie versuchen, eine Softwareabschaltung der virtuellen Hardware durchzuführen.

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

 

