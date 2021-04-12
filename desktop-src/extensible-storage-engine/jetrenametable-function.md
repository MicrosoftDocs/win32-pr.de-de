---
description: 'Weitere Informationen zu: jetrenametable-Funktion'
title: Jetrenametable-Funktion
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348768"
---
# <a name="jetrenametable-function"></a>Jetrenametable-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetrenametable-function"></a>Jetrenametable-Funktion

Die **jetrenametable** -Funktion kann verwendet werden, um den Namen einer vorhandenen Tabelle zu ändern.

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*DBID*

Die Datenbank, die für diesen-Befehl verwendet werden soll.

*szName*

Der aktuelle Name der Tabelle, die umbenannt wird.

*sznamenew*

Der neue Name für die Tabelle, die umbenannt wird.

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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Die angegebene Datenbank war ungültig.</p>
<p>Dieser Fehler wird nur in Windows 2000 zurückgegeben, wenn versucht wird, einen Tabellen Umbenennungs Vorgang für die temporäre Datenbank auszuführen. JET_errInvalidDatabaseId wird in späteren Versionen für diesen Fall zurückgegeben.</p></td>
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
<li><p>Objektnamen dürfen keine Ausrufezeichen (!), Punkte (.), linke eckige Klammer ([) oder rechte eckige Klammer (]) enthalten. nach der Validierung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet. Dies bedeutet, dass Objektnamen keine Leerzeichen enthalten dürfen.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde. Dies kann bei <strong>jetrenametable</strong> vorkommen, wenn:</p>
<ul>
<li><p><em>szName</em> ist NULL.</p></li>
<li><p><em>sznamenew</em> ist NULL.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
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
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Ein Update kann nicht innerhalb des Gültigkeits Bereichs einer schreibgeschützten Transaktion durchgeführt werden. Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> -Aufrufvorgang mit JET_bitTransactionReadOnly gestartet wurde.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Name der angegebenen Tabelle in der angegebenen Datenbank dauerhaft in den neuen Namen geändert.

Bei einem Fehler tritt keine Änderung am Daten Bank Status auf.

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
<td><p>Implementiert als <strong>jetrenametablew</strong> (Unicode) und <strong>jetrenametablea</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
