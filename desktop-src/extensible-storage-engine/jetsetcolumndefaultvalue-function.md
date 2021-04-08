---
description: Weitere Informationen finden Sie in der jetsetcolumndefaultvalue-Funktion.
title: Jetsetcolumndefaultvalue-Funktion
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
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862196"
---
# <a name="jetsetcolumndefaultvalue-function"></a>Jetsetcolumndefaultvalue-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetsetcolumndefaultvalue-function"></a>Jetsetcolumndefaultvalue-Funktion

Die **jetsetcolumndefaultvalue** -Funktion kann verwendet werden, um den Standardwert einer vorhandenen Spalte zu ändern.

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

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*DBID*

Die Datenbank, die für diesen-Befehl verwendet werden soll.

*sztablename*

Der Name der Tabelle, in der die betroffene Spalte enthalten ist.

*szcolumnname*

Der Name der Spalte, deren Standardwert geändert wird.

*pvData*

Der Eingabepuffer, der den neuen Standardwert enthält.

*cbData*

Die Größe des Eingabe Puffers, der den neuen Standardwert enthält.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identisch mit JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnInUse</p></td>
<td><p>Diese angegebene Spalte wird derzeit von einem Index verwendet.</p>
<p><strong>Jetsetcolumndefaultvalue</strong> kann den Standardwert einer Spalte, auf die in der Definition eines Indexes verwiesen wird, nicht ändern. Dies liegt daran, dass dadurch der Inhalt des Indexes geändert werden kann.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Diese angegebene Spalte ist für diese Tabelle nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>Die angegebene Datenbank-ID war ungültig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Einer der angegebenen Objektnamen war ungültig. Alle Objektnamen müssen mit demselben Regelsatz übereinstimmen. Nachfolgend sind diese Regeln aufgeführt:</p>
<ul>
<li><p>Objektnamen müssen aus ASCII-Zeichen bestehen.</p></li>
<li><p>Objektnamen müssen mindestens ein Zeichen lang sein.</p></li>
<li><p>Objektnamen dürfen nicht mehr als JET_cbNameMost (64) Zeichen lang sein.</p></li>
<li><p>Objektnamen dürfen nicht mit einem Leerzeichen beginnen.</p></li>
<li><p>Objektnamen dürfen keine ASCII-Steuerzeichen (0x00 bis 0x1F) enthalten.</p></li>
<li><p>Objektnamen dürfen keine Ausrufezeichen (!), Punkte (.), linke eckige Klammer ([) oder rechte eckige Klammer (]) enthalten.</p></li>
<li><p>Nach der Validierung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet. Dies bedeutet, dass Objektnamen keines der Leerzeichen enthalten dürfen.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>Die Spalte konnte nicht auf NULL festgelegt werden. Dies geschieht für <strong>jetsetcolumndefaultvalue</strong> in folgenden Fällen:</p>
<ul>
<li><p><em>cbData</em> ist 0 (null).</p></li>
<li><p><strong>pvData</strong> ist NULL.</p></li>
</ul>
<p>Daher ist es nicht möglich, den Standardwert einer Spalte (zurück) auf NULL oder auf einen Wert der Länge 0 (null) festzulegen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Diese angegebene Tabelle ist für diese Datenbank nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Diese angegebene Tabelle wird von einer anderen Sitzung verwendet.</p>
<p><strong>Jetsetcolumndefaultvalue</strong> erfordert exklusiven Zugriff auf eine Tabelle, um den Standardwert der Spalte für Releases vor Windows Server 2003 zu ändern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Es ist nicht zulässig, ein Update zu versuchen, wenn es innerhalb des Gültigkeits Bereichs einer schreibgeschützten Transaktion liegt. Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> -Aufrufvorgang mit JET_bitTransactionReadOnly gestartet wurde. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Eine andere Sitzung hat den Datensatz bereits für das Update gesperrt. Das von dieser Sitzung versuchte Update schlägt fehl.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Standardwert der angegebenen Spalte in der angegebenen Tabelle in der angegebenen Datenbank dauerhaft in den neuen Standardwert geändert.

Bei einem Fehler tritt keine Änderung am Daten Bank Status auf.

#### <a name="remarks"></a>Bemerkungen

Es ist nicht möglich, den Standardwert einer Spalte in einer Vorlagen Tabelle zu ändern.

Der Standardwert einer Spalte wird von der Datenbank-Engine für lange Text-und lange Binär Spalten automatisch auf 255 Byte gekürzt.

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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>jetsetcolumndefaultvaluew</strong> (Unicode) und <strong>jetsetcolumndefaultvaluea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[Jetstopservice](./jetstopservice-function.md)
