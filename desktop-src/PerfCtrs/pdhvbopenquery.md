---
description: Die pdhvbopenquery-Funktion erstellt und Initialisiert eine eindeutige Abfrage Struktur, die verwendet wird, um die Erfassung von Leistungsdaten zu verwalten.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: Pdhvbopenquery-Funktion
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
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131677"
---
# <a name="pdhvbopenquery-function"></a>Pdhvbopenquery-Funktion

Die **pdhvbopenquery** -Funktion erstellt und Initialisiert eine eindeutige Abfrage Struktur, die verwendet wird, um die Erfassung von Leistungsdaten zu verwalten.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion "pdhvbopenquery" ( \_ ByVal queryhandle "Long" \_ )

## <a name="parameters"></a>Parameter

<dl> <dt>

*Queryhandle* 
</dt> <dd>

Variable, die gelöscht wird (0 entspricht), bevor die Funktion aufgerufen wird, und, wenn die Funktion erfolgreich ist, enthält die eindeutige ID der erstellten und geöffneten Abfrage. Dieses Handle wird in den nachfolgenden Aufrufen anderer PDH-Funktionen verwendet, um die Abfrage zu identifizieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird eine **lange** ganze Zahl zurückgegeben, \_ die der Fehler Erfolgs-und einem neuen Handle in der *queryhandle* -Variablen entspricht.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md). Die folgenden Werte sind möglich.



| Rückgabecode                                                                                                     | Beschreibung                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Ungültiges PDH- \_ \_ Argument**</dt> </dl>           | Das Argument ist ungültig oder falsch.<br/>             |
| <dl> <dt>**PDH-Speicher Belegungs \_ \_ \_ Fehler**</dt> </dl> | Ein temporärer Speicherpuffer konnte nicht zugeordnet werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhclosequery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

