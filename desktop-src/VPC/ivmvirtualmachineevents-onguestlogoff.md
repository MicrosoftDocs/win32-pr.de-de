---
title: Ivmvirtualmachineevents onguestlogoff-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass sich ein Benutzer vom Gast Betriebssystem abgemeldet hat.
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- Onguestlogoff-Methode Virtual PC
- Onguestlogoff-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onguestlogoff-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce5100c3901b3de32a769b6bae0e16fcffe26a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949378"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a>Ivmvirtualmachineevents:: onguestlogoff-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass sich ein Benutzer vom Gast Betriebssystem abgemeldet hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*logofftype* \[ in\]
</dt> <dd>

Der Wert aus der [**vmlogofftype**](vmlogofftype.md) -Enumeration, der den Typ der Abmeldung beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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
</dt> <dt>

[**Vmlogofftype**](vmlogofftype.md)
</dt> </dl>

 

