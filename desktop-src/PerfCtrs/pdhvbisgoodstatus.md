---
description: Die pdhvbisgoodstatus-Funktion testet einen Statuswert, um zu bestimmen, ob es sich um einen Erfolgs-oder Fehlercode handelt. Wenn der Statuswert ein erfolgreicher Wert ist, ist der Rückgabewert ungleich 0 (null). Wenn es sich um einen Fehlerstatus Code handelt, ist der Rückgabewert 0 (null).
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: Pdhvbisgoodstatus-Funktion
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
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349222"
---
# <a name="pdhvbisgoodstatus-function"></a>Pdhvbisgoodstatus-Funktion

Die **pdhvbisgoodstatus** -Funktion testet einen Statuswert, um zu bestimmen, ob es sich um einen Erfolgs-oder Fehlercode handelt. Wenn der Statuswert ein erfolgreicher Wert ist, ist der Rückgabewert ungleich 0 (null). Wenn es sich um einen Fehlerstatus Code handelt, ist der Rückgabewert 0 (null).

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion "pdhvbisgoodstatus" ( \_ ByVal statusvalue "Long" \_ )

## <a name="parameters"></a>Parameter

<dl> <dt>

*Statuswert* 
</dt> <dd>

Status Wert, der von einer anderen PDH-Funktion zurückgegeben wird, die getestet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt 0 (null) zurück, wenn der Statuscode ein Fehlerstatus Code ist. Er gibt einen Wert ungleich 0 (null) zurück, wenn der Statuscode ein Erfolgsstatus Code ist

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhvbgetdoublecountervalue**](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




