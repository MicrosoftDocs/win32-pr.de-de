---
title: IVMTask WaitForCompletion-Methode (VPCCOMInterfaces.h)
description: Wartet, bis der Task abgeschlossen ist oder das angegebene Time out-Intervall verstreicht.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- WaitForCompletion-Methode Virtueller PC
- WaitForCompletion-Methode Virtueller PC, IVMTask-Schnittstelle
- IVMTask-Schnittstelle Virtueller PC, WaitForCompletion-Methode
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd77019c98e48f4707ac173f825823d5637a1d83c5eb1583f4ee68874e84bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752701"
---
# <a name="ivmtaskwaitforcompletion-method"></a>IVMTask::WaitForCompletion-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Wartet, bis der Task abgeschlossen ist oder das angegebene Time out-Intervall verstreicht.

## <a name="syntax"></a>Syntax


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Timeout* \[ In\]
</dt> <dd>

Die Zeit in Millisekunden, die diese Methode auf den Abschluss der Aufgabe wartet, bevor sie die Steuerung an den Aufrufer zurücksendet. Der Wert -1 gibt an, dass die Methode wartet, bis die Aufgabe abgeschlossen ist, ohne dass ein Time out erfolgt. Andere gültige Timeoutwerte liegen zwischen 0 und 4.000.000 Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | Beschreibung                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>         |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>      | Der *Timeoutparameter* ist ungültig.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>     |



 

## <a name="remarks"></a>Hinweise

Die **WaitForCompletion-Methode versetzt** den aktuellen Ausführungsthread in den Ruhezustand, bis er zurückgegeben wird. Die Angabe einer unendlichen Wartezeit (Timeout = -1) wird nicht empfohlen, es sei denn, es ist absolut wichtig, dass die Aufgabe unter allen Umständen abgeschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask ist als ab72b222-6e9c-48ae-aa54-85e3e635767c definiert.<br/>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

