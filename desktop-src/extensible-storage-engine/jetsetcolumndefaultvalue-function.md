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
ms.openlocfilehash: ff0f704c30737d6cfc2d8bd823da8207e8d7d8c3fb4458687baf8bc400718304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117703848"
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

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identisch mit JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnInUse</p></td>
<td><p>Diese angegebene Spalte wird derzeit von einem Index verwendet.</p>
<p><strong>JetSetColumnDefaultValue</strong> kann den Standardwert einer Spalte, auf die in der Definition eines Index verwiesen wird, nicht ändern. Dies liegt daran, dass dies den Inhalt des Indexes ändern könnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Diese angegebene Spalte ist für diese Tabelle nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>Die angegebene Datenbank-ID war ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Einer der angegebenen Objektnamen war ungültig. Alle Objektnamen müssen demselben Satz von Regeln entsprechen. Nachfolgend sind diese Regeln aufgeführt:</p>
<ul>
<li><p>Objektnamen müssen aus ASCII-Zeichen bestehen.</p></li>
<li><p>Objektnamen müssen mindestens ein Zeichen lang sein.</p></li>
<li><p>Objektnamen dürfen die Länge JET_cbNameMost (64) Zeichen nicht überschreiten.</p></li>
<li><p>Objektnamen beginnen möglicherweise nicht mit einem Leerzeichen.</p></li>
<li><p>Objektnamen dürfen keine ASCII-Steuerzeichen enthalten (0x00 bis 0x1F).</p></li>
<li><p>Objektnamen dürfen kein Ausrufezeichen (!), Punkt (.), linke Klammer ([) oder rechte Klammer (]) enthalten.</p></li>
<li><p>Nach der Überprüfung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (falls möglich) für den Objektnamen verwendet. Dies bedeutet, dass Objektnamen möglicherweise auch kein Leerzeichen enthalten.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>Die Spalte konnte nicht auf NULL festgelegt werden. Dies geschieht für <strong>JetSetColumnDefaultValue in den:</strong></p>
<ul>
<li><p><em>cbData</em> ist 0 (null).</p></li>
<li><p><strong>pvData</strong> ist NULL.</p></li>
</ul>
<p>Daher ist es nicht möglich, den Standardwert einer Spalte (zurück) auf NULL oder einen Wert der Länge 0 (null) zu setzen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Diese angegebene Tabelle ist für diese Datenbank nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht gleichzeitig für mehrere Threads verwendet werden. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Diese angegebene Tabelle wird von einer anderen Sitzung verwendet.</p>
<p><strong>JetSetColumnDefaultValue</strong> erfordert exklusiven Zugriff auf eine Tabelle, um den Standardwert der Spalte für Releases vor Windows Server 2003 zu ändern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Es ist unzulässig, ein Update innerhalb des Bereichs einer schreibgeschützten Transaktion zu versuchen. Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem Aufruf von <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> mit JET_bitTransactionReadOnly. Dieser Fehler wird nur von xp Windows und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Eine andere Sitzung hat den Datensatz zuvor für das Update gesperrt. Das von dieser Sitzung versuchte Update ist fehlgeschlagen.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Standardwert der angegebenen Spalte in der angegebenen Tabelle in der angegebenen Datenbank dauerhaft in den neuen Standardwert geändert.

Bei einem Fehler erfolgt keine Änderung des Datenbankstatus.

#### <a name="remarks"></a>Hinweise

Es ist nicht möglich, den Standardwert einer Spalte in einer Vorlagentabelle zu ändern.

Die Datenbank-Engine schneidigt den Standardwert einer Spalte automatisch auf 255 Byte für lange Textspalten und lange binäre Spalten ab.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>JetSetColumnDefaultValueW</strong> (Unicode) und <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
