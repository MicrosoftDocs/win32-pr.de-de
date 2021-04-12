---
title: Ivmvirtualpcevents oneventlogger-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass Windows Virtual PC ein Ereignis protokolliert.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Oneventlogger-Methode Virtual PC
- Oneventlogger-Methode Virtual PC, ivmvirtualpcevents-Schnittstelle
- Ivmvirtualpcevents Interface Virtual PC, oneventlogger-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518005"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>Ivmvirtualpcevents:: oneventlogger-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass Windows Virtual PC ein Ereignis protokolliert.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*logmessageid* \[ in\]
</dt> <dd>

Der Meldungs Bezeichner der Ereignisprotokoll Meldung, die protokolliert wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn Windows Virtual PC eine Meldung im Windows-Ereignisprotokoll protokolliert. Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das Ereignis vom Typ " **vmvirtualpcevent Ereignis \_ protokolliert** " zu erhalten, das von [**ivmvirtualpc**](ivmvirtualpc.md)stammt.

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

 

