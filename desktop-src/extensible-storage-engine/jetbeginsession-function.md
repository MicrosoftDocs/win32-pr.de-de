---
description: 'Weitere Informationen zu: jetbeginsession-Funktion'
title: JetBeginSession-Funktion
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351075"
---
# <a name="jetbeginsession-function"></a>JetBeginSession-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbeginsession-function"></a>JetBeginSession-Funktion

Die **jetbeginsession** -Funktion startet eine Sitzung und initialisiert und gibt ein ESE-Sitzungs handle ([JET_SESID](./jet-sesid.md)) zurück. Sitzungen steuern den gesamten Zugriff auf die Datenbank und werden verwendet, um den Umfang der Transaktionen zu steuern. Die Sitzung kann verwendet werden, um Transaktionen zu starten, zu übertragen oder abzubrechen. Die Sitzung wird auch zum Anfügen, erstellen oder Öffnen einer Datenbank verwendet. Die Sitzung wird als Kontext für alle DDL-und DML-Vorgänge verwendet. Um Parallelität und parallelen Zugriff auf die Datenbank zu erhöhen, können mehrere Sitzungen gestartet werden.

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Die Daten Bank Instanz, die für diesen-Befehl verwendet werden soll.

*psetup-sid*

Ein Zeiger auf die Variable, die vom Sitzungs Handle bei erfolgreicher Rückgabe initialisiert wird.

*szusername*

Dieser Parameter ist reserviert.

*szPassword*

Dieser Parameter ist reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion ermöglicht die Rückgabe von [JET_ERR](./jet-err.md)s, die in dieser API definiert sind. Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang konnte nicht ausgeführt werden, da kein Arbeitsspeicher zugeordnet werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>Die Anzahl der Sitzungen, die die Engine für den Start des Clients zulässt, ist begrenzt. Dieser Wert kann mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit der JET_paramMaxSessions-Konstante geändert werden. Die Standard Anzahl von Sitzungen ist 16. Weitere Informationen zu JET_paramMaxSessions finden Sie unter <a href="gg294139(v=exchg.10).md">System Parameter</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird das Sitzungs Handle initialisiert und kann für Daten Bank Vorgänge verwendet werden.

Bei einem Fehler sind keine Sitzungen verfügbar, oder eine neue Sitzung konnte nicht initialisiert werden.

#### <a name="remarks"></a>Bemerkungen

Bei der Verwendung von Sitzungen über verschiedene Threads muss sorgfältig vorgegangen werden. In einer Sitzung wird nachverfolgt, in welchem Thread Sie während [jetbegintransaction](./jetbegintransaction-function.md), [jetcommittransaction](./jetcommittransaction-function.md)oder [jetrollback](./jetrollback-function.md)verwendet wurde, und es wird ein Fehler ausgelöst, wenn Sie für mehrere Threads mit einer geöffneten Transaktion verwendet wird. Das [jetresessioncontext](./jetresetsessioncontext-function.md)-Objekt [kann dieses](./jetsetsessioncontext-function.md) Verhalten ändern. Da es sich bei der Sitzung immer noch um einen serialisierten Kontext handelt, können mehrere Daten Bank Vorgänge nicht gleichzeitig in einer einzelnen Sitzung ausgeführt werden, sondern nur seriell. Sie können jedoch mehrere-Sitzungen verwenden, um gleichzeitigen Datenbankzugriff zu erreichen. Sitzungen können innerhalb einer Transaktion Thread übergreifend verwendet werden, indem Sie die Sitzungs Kontexte festlegen und zurücksetzen.

Das Sitzungs Handle muss mit [jetendsession](./jetendsession-function.md)geschlossen werden.

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
<td><p>Implementiert als <strong>jetbeginsessionw</strong> (Unicode) und <strong>jetbeginsessiona</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[Jetbegintransaction](./jetbegintransaction-function.md)  
[Jetcommittransaction](./jetcommittransaction-function.md)  
[Jetdupsession](./jetdupsession-function.md)  
[Jetendsession](./jetendsession-function.md)  
[Jetresessioncontext](./jetresetsessioncontext-function.md)  
[Jetrollback](./jetrollback-function.md)  
[Jetabessioncontext](./jetsetsessioncontext-function.md)  
[Jetstopservice](./jetstopservice-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
