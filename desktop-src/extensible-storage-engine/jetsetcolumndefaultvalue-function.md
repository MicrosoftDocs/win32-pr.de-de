---
description: 'Weitere Informationen finden Sie unter: JetSetColumnDefaultValue-Funktion'
title: JetSetColumnDefaultValue-Funktion
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b4c624e985cbbef41d3e2a96133af97de6ea250e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984383"
---
# <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue-Funktion

Die **JetSetColumnDefaultValue-Funktion** kann verwendet werden, um den Standardwert einer vorhandenen Spalte zu ändern.

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*Dbid*

Die Datenbank, die für diesen Aufruf verwendet werden soll.

*szTableName*

Der Name der Tabelle, die die betroffene Spalte enthält.

*szColumnName*

Der Name der Spalte, deren Standardwert geändert wird.

*pvData*

Der Eingabepuffer, der den neuen Standardwert enthält.

*cbData*

Die Größe des Eingabepuffers, der den neuen Standardwert enthält.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Identisch mit JET_errNullInvalid.</p> | 
| <p>JET_errColumnInUse</p> | <p>Diese angegebene Spalte wird derzeit von einem Index verwendet.</p><p><strong>JetSetColumnDefaultValue</strong> kann den Standardwert einer Spalte, auf die in der Definition eines Index verwiesen wird, nicht ändern. Dies liegt daran, dass dies den Inhalt des Indexes ändern könnte.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Diese angegebene Spalte ist für diese Tabelle nicht vorhanden.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>Die angegebene Datenbank-ID war ungültig.</p> | 
| <p>JET_errInvalidName</p> | <p>Einer der angegebenen Objektnamen war ungültig. Alle Objektnamen müssen demselben Satz von Regeln entsprechen. Nachfolgend sind diese Regeln aufgeführt:</p><ul><li><p>Objektnamen müssen aus ASCII-Zeichen bestehen.</p></li><li><p>Objektnamen müssen mindestens ein Zeichen lang sein.</p></li><li><p>Objektnamen dürfen die Länge JET_cbNameMost (64) Zeichen nicht überschreiten.</p></li><li><p>Objektnamen beginnen möglicherweise nicht mit einem Leerzeichen.</p></li><li><p>Objektnamen dürfen keine ASCII-Steuerzeichen enthalten (0x00 bis 0x1F).</p></li><li><p>Objektnamen dürfen kein Ausrufezeichen (!), Punkt (.), linke Klammer ([) oder rechte Klammer (]) enthalten.</p></li><li><p>Nach der Überprüfung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (falls möglich) für den Objektnamen verwendet. Dies bedeutet, dass Objektnamen möglicherweise auch kein Leerzeichen enthalten.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNullInvalid</p> | <p>Die Spalte konnte nicht auf NULL festgelegt werden. Dies geschieht für <strong>JetSetColumnDefaultValue in den:</strong></p><ul><li><p><em>cbData</em> ist 0 (null).</p></li><li><p><strong>pvData</strong> ist NULL.</p></li></ul><p>Daher ist es nicht möglich, den Standardwert einer Spalte (zurück) auf NULL oder einen Wert der Länge 0 (null) zu setzen.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Diese angegebene Tabelle ist für diese Datenbank nicht vorhanden.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTableInUse</p> | <p>Diese angegebene Tabelle wird von einer anderen Sitzung verwendet.</p><p><strong>JetSetColumnDefaultValue</strong> erfordert exklusiven Zugriff auf eine Tabelle, um den Standardwert der Spalte für Releases vor Windows Server 2003 zu ändern.</p> | 
| <p>JET_errTermInProgress</p> | <p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Es ist unzulässig, ein Update innerhalb des Bereichs einer schreibgeschützten Transaktion zu versuchen. Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem Aufruf von <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> mit JET_bitTransactionReadOnly. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errWriteConflict</p> | <p>Eine andere Sitzung hat den Datensatz zuvor für das Update gesperrt. Das von dieser Sitzung versuchte Update ist fehlgeschlagen.</p> | 



Bei Erfolg wird der Standardwert der angegebenen Spalte in der angegebenen Tabelle in der angegebenen Datenbank dauerhaft in den neuen Standardwert geändert.

Bei einem Fehler erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Bemerkungen

Es ist nicht möglich, den Standardwert einer Spalte in einer Vorlagentabelle zu ändern.

Die Datenbank-Engine schneidigt den Standardwert einer Spalte automatisch auf 255 Byte für lange Textspalten und lange binäre Spalten ab.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JetSetColumnDefaultValueW</strong> (Unicode) und <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
