---
title: Ivmtask waitforcompletion-Methode (vpccominterfaces. h)
description: Wartet, bis die Aufgabe beendet oder das angegebene Timeout Intervall abläuft.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Waitforcompletion-Methode Virtual PC
- Waitforcompletion-Methode Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, waitforcompletion-Methode
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
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341411"
---
# <a name="ivmtaskwaitforcompletion-method"></a>Ivmtask:: waitforcompletion-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Wartet, bis die Aufgabe beendet oder das angegebene Timeout Intervall abläuft.

## <a name="syntax"></a>Syntax


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Timeout* \[ in\]
</dt> <dd>

Die Zeit in Millisekunden, die diese Methode auf den Abschluss der Aufgabe wartet, bevor die Steuerung an den Aufrufer zurückgegeben wird. Der Wert-1 gibt an, dass die Methode wartet, bis die Aufgabe abgeschlossen ist, ohne dass ein Timeout eintritt. Weitere gültige Timeout Werte liegen im Bereich von 0 bis 4 Millionen Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>         |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>      | Der *Timeout* -Parameter ist ungültig.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Die **waitforcompletion** -Methode versetzt den aktuellen Ausführungs Thread in den Standbymodus, bis er zurückgegeben wird. Das Angeben einer unendlichen Wartezeit (Timeout =-1) wird nur empfohlen, wenn es absolut wichtig ist, dass die Aufgabe unter einem beliebigen Umstand abgeschlossen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmtask**](ivmtask.md)
</dt> </dl>

 

