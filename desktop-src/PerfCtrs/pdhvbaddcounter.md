---
description: Die pdhvbaddcounter-Funktion erstellt einen Counter-Eintrag im angegebenen Abfrageobjekt und gibt nach erfolgreichem Abschluss ein Handle für diesen Wert zurück.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: Pdhvbaddcounter-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347588"
---
# <a name="pdhvbaddcounter-function"></a>Pdhvbaddcounter-Funktion

Die **pdhvbaddcounter** -Funktion erstellt einen Counter-Eintrag im angegebenen Abfrageobjekt und gibt nach erfolgreichem Abschluss ein Handle für diesen Wert zurück.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion pdhvbaddcounter ( \_ ByVal queryhandle als Long, \_ ByVal counterpath As String, \_ ByVal counterhandle so Long \_ ) wie Long

## <a name="parameters"></a>Parameter

<dl> <dt>

*Queryhandle* 
</dt> <dd>

Die ID der Abfrage, der dieser Counter zugewiesen werden soll. Dieser Wert wird von der [**pdhvbopenquery**](pdhvbopenquery.md) -Funktion zurückgegeben.

</dd> <dt>

*CounterPath* 
</dt> <dd>

Eine Text Zeichenfolge, die den Namen des der Abfrage hinzu zufügenden Zählers angibt. Der Inhalt dieser Zeichenfolge muss ein gültiger Counter-Pfad sein, der vom-gegen Browser oder von einer anderen Quelle abgerufen wird.

</dd> <dt>

*Counter handle* 
</dt> <dd>

Eindeutiger Verweis, der diesen Counter in der Abfrage identifiziert. Diese Variable muss mit 0 (null) initialisiert werden, bevor die-Funktion aufgerufen wird. Sie enthält einen gültigen Wert bei Rückgabe nur, wenn die Funktion erfolgreich abgeschlossen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird eine **lange** ganze Zahl zurückgegeben, \_ die der Fehler Erfolgs-und einem neuen Handle in der *Counter handle* -Variablen entspricht.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md). Die folgenden Werte sind möglich.



| Rückgabecode                                                                                                     | Beschreibung                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**Ungültiges PDH- \_ \_ Argument**</dt> </dl>           | Mindestens eines der Argumente ist ungültig oder falsch.<br/>              |
| <dl> <dt>**PDH-Speicher Belegungs \_ \_ \_ Fehler**</dt> </dl> | Ein Arbeitsspeicher Puffer konnte nicht zugeordnet werden.<br/>                            |
| <dl> <dt>**Ungültiges PDH- \_ \_ handle**</dt> </dl>             | Das Abfrage Handle ist ungültig.<br/>                                     |
| <dl> <dt>**PDH \_ cstatus \_ kein \_ Counter**</dt> </dl>        | Der angegebene gegen Wert wurde nicht gefunden.<br/>                               |
| <dl> <dt>**PDH \_ cstatus \_ No- \_ Objekt**</dt> </dl>         | Das angegebene Objekt wurde nicht gefunden.<br/>                           |
| <dl> <dt>**PDH \_ cstatus \_ kein \_ Computer**</dt> </dl>        | Ein Computer Eintrag konnte nicht erstellt werden.<br/>                             |
| <dl> <dt>**PDH \_ cstatus ungültiger \_ \_ counterName**</dt> </dl>   | Es wurde eine leere Zeichenfolge für den Namen des Counter-namens angegeben.<br/>                   |
| <dl> <dt>**PDH- \_ Funktion wurde \_ nicht \_ gefunden.**</dt> </dl>        | Die Berechnungsfunktion für diesen Counter konnte nicht bestimmt werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhvbopenquery**](pdhvbopenquery.md)
</dt> </dl>

 

