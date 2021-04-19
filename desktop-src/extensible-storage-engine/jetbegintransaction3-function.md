---
description: 'Weitere Informationen finden Sie hier: JetBeginTransaction3-Funktion'
title: JetBeginTransaction3-Funktion
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346677"
---
# <a name="jetbegintransaction3-function"></a>JetBeginTransaction3-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetBeginTransaction3** -Funktion bewirkt, dass eine Sitzung eine Transaktion eingibt und einen neuen Sicherungspunkt erstellt. Diese Funktion kann mehrmals in einer einzelnen Sitzung aufgerufen werden, um zusätzliche Speicherpunkte zu erstellen. Diese Speicherpunkte können verwendet werden, um die Änderungen an der Datenbank selektiv beizubehalten oder zu verwerfen.

Die **JetBeginTransaction3** -Funktion wurde im Windows 8-Betriebssystem eingeführt.

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*trxid*

Ein optionaler Bezeichner, der vom Benutzer zur Identifizierung der Transaktion bereitgestellt wird.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der in der folgenden Tabelle aufgeführten aufrufoptions Werte angibt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Wert</p></th>
<th><p>Bedeutung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitTransactionReadOnly</p></td>
<td><p>Die Datenbank wird von der Transaktion nicht geändert. Wenn ein Update versucht wird, schlägt dieser Vorgang mit JET_errTransReadOnly Antwort Codes fehl. Diese Option wird ignoriert, es sei denn, Sie wird angefordert, wenn die angegebene Sitzung nicht bereits in einer Transaktion vorhanden ist. Diese Option ist ab Windows XP in Versionen des Windows-Betriebssystems verfügbar.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion beendet wurden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Rückgabecode wird von Windows-Versionen ab Windows XP zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden. Dieser Fehler wird von Windows-Versionen ab Windows XP zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep</p></td>
<td><p>Eine neue Transaktion kann nicht gestartet werden, da die Sitzung bereits die maximale Speicherpunkt Tiefe hat, die von der Datenbank-Engine zulässig ist.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird die angegebene Sitzung innerhalb einer Transaktion ausgeführt. Wenn sich die Sitzung zuvor in einer Transaktion befunden hat, wird ein neuer Sicherungspunkt erstellt.

Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Weitere Informationen zur Funktionsweise von Transaktionen finden Sie unter [jetbegintransaction](./jetbegintransaction-function.md).

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2012.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Siehe auch

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[Jetbegintransaction](./jetbegintransaction-function.md)  
[Jetcommittransaction](./jetcommittransaction-function.md)  
[Jetgetsystemparameter](./jetgetsystemparameter-function.md)  
[Jetresessioncontext](./jetresetsessioncontext-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetabessioncontext](./jetsetsessioncontext-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
