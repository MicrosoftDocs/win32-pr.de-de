---
title: Ivmvirtualmachineevents onrequestshutdown-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren durchgeführt wurde.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Onrequestshutdown-Methode virtueller PC
- Onrequestshutdown-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onrequestshutdown-Methode
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
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477403"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a>Ivmvirtualmachineevents:: onrequestshutdown-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass eine Anforderung zum Herunterfahren durchgeführt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird immer dann aufgerufen, wenn die Sitzung des virtuellen Computers gerade heruntergefahren wird. Das Client Programm muss diese Schnittstellen Methode implementieren, um eine Benachrichtigung über das " **vmvirtualmachineevent \_ requestshutdown** "-Ereignis zu erhalten, das von [**ivmvirtualmachine**](ivmvirtualmachine.md)stammt.

Diese Ereignis Benachrichtigung wird nur gesendet, wenn die Sitzung der virtuellen Computer gerade heruntergefahren wird. Die Routinen zum Herunterfahren des Betriebssystems, wie z. b. [**ivmguestos:: Shutdown**](ivmguestos-shutdown.md), lösen dieses Ereignis nicht direkt aus, es sei denn, Sie versuchen auch, ein Software ausschalten der virtuellen Hardware auszuführen.

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

 

