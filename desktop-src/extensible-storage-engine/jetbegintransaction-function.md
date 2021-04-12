---
description: Weitere Informationen finden Sie in der jetbegintransaction-Funktion.
title: JetBeginTransaction-Funktion
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342668"
---
# <a name="jetbegintransaction-function"></a>JetBeginTransaction-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbegintransaction-function"></a>JetBeginTransaction-Funktion

Die **jetbegintransaction** -Funktion bewirkt, dass eine Sitzung eine Transaktion eingibt und einen neuen Sicherungspunkt erstellt. Diese Funktion kann in einer einzelnen Sitzung mehrmals aufgerufen werden, um die Erstellung zusätzlicher Speicherpunkte zu verursachen. Diese Speicherpunkte können verwendet werden, um Änderungen am Status der Datenbank selektiv beizubehalten oder zu verwerfen.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

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
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
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
<td><p>Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
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


Bei Erfolg wird die angegebene Sitzung innerhalb einer Transaktion ausgeführt. Wenn sich die Sitzung zuvor in einer Transaktion befand, wird ein neuer Sicherungspunkt erstellt.

Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Die Datenbank-Engine stellt ein Snapshot-Isolations Modell für Ihre Transaktionen bereit. Dies bedeutet Folgendes: Wenn eine Sitzung zum ersten Mal in einen Transaktionszustand gelangt, wird die gesamte Datenbank in der Zeit zu Beginn der Transaktion fixiert. Eine Sitzung muss keine Daten Sperren, da Sie stets auf die entsprechende Version dieser Daten zugreifen kann. Dies bedeutet, dass eine Sitzung, die Daten aktualisiert, niemals eine andere Sitzung daran hindern wird, diese Daten zu lesen.

Eine weitere Konsequenz der Verwendung der Momentaufnahme Isolation ist das Sperr Modell, das für Updates verwendet wird. Die Datenbank-Engine gibt eine Schreibsperre für ein bestimmtes Datenelement an die erste Sitzung aus, die Sie anfordert. Diese Schreibsperre wird aufgehoben, wenn die Transaktion entweder vollständig committet oder abgebrochen wurde, sodass die Sitzung nicht mehr in einer Transaktion ausgeführt wird. Während eine Sitzung eine Schreibsperre enthält, wird jede andere Sitzung, die dieselbe Schreibsperre anfordert, nicht blockiert, bis die Schreibsperre verfügbar ist. Stattdessen schlägt diese zweite Sitzung sofort mit JET_errWriteConflict fehl. Um diesen Konflikt zu lösen, muss die zweite Sitzung die Transaktion vollständig abbrechen (oder Committe). warten Sie einige Zeit, bis die erste Sitzung einen Commit oder Abbruch der Transaktion durchgeführt hat, und beginnen Sie dann erneut.

Zur Unterstützung der Momentaufnahmenisolation speichert die Datenbank-Engine alle Versionen aller geänderten Daten im Arbeitsspeicher, seit die älteste aktive Transaktion in einer Sitzung zum ersten Mal gestartet wurde. Dies hat wichtige Auswirkungen auf Ihre Anwendung. Jedes Verhalten, das eine große Anzahl von Versionen im Arbeitsspeicher aufführt, kann dazu führen, dass die Instanz die maximale Versionsspeicher Größe abbaut (Weitere Informationen finden Sie unter [JET_paramMaxVerPages](./resource-parameters.md) in [System Parametern](./extensible-storage-engine-system-parameters.md) ). Dieses Verhalten umfasst, ist aber nicht auf sehr große Updates in einer einzelnen Transaktion und sehr lang andauernden Transaktionen beschränkt. Daher ist es sehr wichtig, die Versionsspeicher Größe für die erwartete Transaktions Last der Anwendung ordnungsgemäß zu konfigurieren. Es ist auch wichtig, die Anzahl der Updates, die in einer einzelnen Transaktion ausgeführt werden, zu begrenzen. Außerdem ist es wichtig, Transaktionen so kurz wie möglich in Szenarien mit hoher Auslastung zu erstellen.

Es wird dringend empfohlen, dass die Anwendung immer im Kontext einer Transaktion ist, wenn Sie ESE-APIs aufrufen, die Daten abrufen oder aktualisieren. Wenn dies nicht erfolgt, umschließt die Datenbank-Engine automatisch jeden ESE-API-Aufrufe dieses Typs in einer Transaktion für die Anwendung. Die Kosten für diese sehr kurzen Transaktionen können in einigen Fällen schnell addiert werden.

Das Standardverhalten der Engine besteht darin, die Verwendung einer Sitzung von dem Zeitpunkt, an dem der erste Aufruf von **jetbegintransaction** erfolgt, auf denselben Thread einzuschränken, bis zu dem Zeitpunkt, zu dem der übereinstimmende Aufruf von [jetcommittransaction](./jetcommittransaction-function.md) oder [jetrollback](./jetrollback-function.md) erfolgt. Dieses Verhalten kann geändert werden, um diese Einschränkung zu entfernen, indem ein benutzerdefinierter Sitzungs Kontext mithilfe von [jetort](./jetsetsessioncontext-function.md) und [jetresessioncontext](./jetresetsessioncontext-function.md)festgelegt wird.

Die Datenbank-Engine unterstützt auch Transaktions Schema Änderungen. Beispielsweise ist es möglich, eine neue Transaktion zu starten, eine Tabelle zu erstellen, einige Spalten hinzuzufügen, einen Index zu erstellen oder zwei zu erstellen und dann die Transaktion abzubrechen. Die soeben hinzugefügten Schema Elemente werden aus der Datenbank entfernt. Es ist auch möglich, Schema Änderungen und normale Datenbankupdates in derselben Transaktion zu mischen.

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
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[Jetcommittransaction](./jetcommittransaction-function.md)  
[Jetgetsystemparameter](./jetgetsystemparameter-function.md)  
[Jetresessioncontext](./jetresetsessioncontext-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetabessioncontext](./jetsetsessioncontext-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
