---
description: Die PdhVbIsGoodStatus-Funktion testet einen Statuswert, um zu ermitteln, ob es sich um einen Erfolgs- oder Fehlercode handelt. Wenn der Statuswert erfolgreich ist, ist der Rückgabewert ungleich null. Wenn es sich um einen Fehlerstatuscode handelt, ist der Rückgabewert 0 (null).
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: e0b142da988143d7304a6b9b01bc5163e741fdaff77d7e0d796882607fc73044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683770"
---
# <a name="pdhvbisgoodstatus-function"></a>PdhVbIsGoodStatus-Funktion

Die **PdhVbIsGoodStatus-Funktion** testet einen Statuswert, um zu ermitteln, ob es sich um einen Erfolgs- oder Fehlercode handelt. Wenn der Statuswert erfolgreich ist, ist der Rückgabewert ungleich null. Wenn es sich um einen Fehlerstatuscode handelt, ist der Rückgabewert 0 (null).

> [!IMPORTANT]
> Die funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der unter [Leistungsindikatorfunktionen beschriebenen Funktionen.](performance-counters-functions.md)

Funktion PdhVbIsGoodStatus( \_ ByVal StatusValue as long \_ ) as long

## <a name="parameters"></a>Parameter

<dl> <dt>

*StatusValue* 
</dt> <dd>

Statuswert, der von einer anderen PDH-Funktion zurückgegeben wird, die getestet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt 0 (null) zurück, wenn der Statuscode ein Fehlerstatuscode ist. Sie gibt einen Wert ungleich 0 (null) zurück, wenn der Statuscode ein Erfolgsstatuscode ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




