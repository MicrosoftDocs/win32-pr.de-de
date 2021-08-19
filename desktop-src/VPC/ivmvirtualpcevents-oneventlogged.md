---
title: IVMVirtualPCEvents OnEventLogged-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass Windows Virtual PC ein Ereignis protokolliert.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- OnEventLogged-Methode Virtueller PC
- OnEventLogged-Methode Virtueller PC, IVMVirtualPCEvents-Schnittstelle
- IVMVirtualPCEvents-Schnittstelle Virtueller PC , OnEventLogged-Methode
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
ms.openlocfilehash: f4994f37cd0e6f83162171fbbdacbf2247a8d472cd49b5750aa2d1b735e4b554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998520"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>IVMVirtualPCEvents::OnEventLogged-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass Windows Virtual PC ein Ereignis protokolliert.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*logMessageID* \[ In\]
</dt> <dd>

Der Nachrichtenbezeichner der protokollierten Ereignisprotokollmeldung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn Windows Virtual PC eine Nachricht im Windows Ereignisprotokoll protokolliert. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das **Ereignis vmVirtualPCEvent \_ EventLogged** zu erhalten, das von [**IVMVirtualPC**](ivmvirtualpc.md)stammt.

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

 

