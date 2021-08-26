---
description: Die PdhVbOpenQuery-Funktion erstellt und initialisiert eine eindeutige Abfragestruktur, die zum Verwalten der Sammlung von Leistungsdaten verwendet wird.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 70d207696f68b9ef86ba0bae1f596826bd6e400d05d011b330f67241e186f5eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962390"
---
# <a name="pdhvbopenquery-function"></a>PdhVbOpenQuery-Funktion

Die **PdhVbOpenQuery-Funktion** erstellt und initialisiert eine eindeutige Abfragestruktur, die zum Verwalten der Sammlung von Leistungsdaten verwendet wird.

> [!IMPORTANT]
> Die in diesem Thema beschriebene Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der in [Leistungsindikatorfunktionen beschriebenen](performance-counters-functions.md)Funktionen.

Funktion PdhVbOpenQuery( \_ ByVal QueryHandle as Long \_ ) As Long

## <a name="parameters"></a>Parameter

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Variable, die gelöscht wird (gleich 0), bevor die Funktion aufgerufen wird, und, wenn die Funktion erfolgreich ist, enthält die eindeutige ID der Abfrage, die erstellt und geöffnet wird. Dieses Handle wird in den nachfolgenden Aufrufen anderer PDH-Funktionen verwendet, um die Abfrage zu identifizieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt  wird, gibt sie eine Long-Ganzzahl zurück, die error success entspricht, \_ und ein neues Handle in der *QueryHandle-Variablen.*

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehlercode](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode.](pdh-error-codes.md) Im Folgenden sind mögliche Werte angegeben.



| Rückgabecode                                                                                                     | Beschreibung                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**\_UNGÜLTIGES \_ PDH-ARGUMENT**</dt> </dl>           | Das Argument ist ungültig oder falsch.<br/>             |
| <dl> <dt>**\_ \_ \_ PDH-SPEICHERBELEGUNGSFEHLER**</dt> </dl> | Ein temporärer Speicherpuffer konnte nicht zugeordnet werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

