---
description: 'Weitere Informationen zu: JetBeginSession-Funktion'
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
ms.openlocfilehash: 0852de04f3969e3e30debc7ba7ff4f3aedf7ac4084b17f91feed8984fe4e1467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251614"
---
# <a name="jetbeginsession-function"></a>JetBeginSession-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbeginsession-function"></a>JetBeginSession-Funktion

Die **JetBeginSession-Funktion** startet eine Sitzung und initialisiert und gibt ein ESE-Sitzungshandle zurück ([JET_SESID](./jet-sesid.md)). Sitzungen steuern den gesamten Zugriff auf die Datenbank und werden zum Steuern des Transaktionsumfangs verwendet. Die Sitzung kann zum Starten, Committen oder Abbrechen von Transaktionen verwendet werden. Die Sitzung wird auch zum Anfügen, Erstellen oder Öffnen einer Datenbank verwendet. Die Sitzung wird als Kontext für alle DDL- und DML-Vorgänge verwendet. Um die Parallelität und den parallelen Zugriff auf die Datenbank zu erhöhen, können mehrere Sitzungen gestartet werden.

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Die Datenbankinstanz, die für diesen Aufruf verwendet werden soll.

*psesid*

Zeiger auf die Variable, die das Sitzungshandle bei erfolgreicher Rückgabe initialisiert.

*szUserName*

Dieser Parameter ist reserviert.

*szPassword*

Dieser Parameter ist reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion ermöglicht die Rückgabe aller [JET_ERR,](./jet-err.md)die in dieser API definiert sind. Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p>
<p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, weil kein Arbeitsspeicher zugeordnet werden konnte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>Die Anzahl der Sitzungen, die die Engine dem Client den Start erlaubt, ist begrenzt. Dieser Wert kann mithilfe von <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> mit der JET_paramMaxSessions Konstante geändert werden. Die Standardanzahl von Sitzungen beträgt 16. Ausführliche Informationen zu JET_paramMaxSessions finden Sie unter <a href="gg294139(v=exchg.10).md">Systemparameter.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird das Sitzungshandle initialisiert und kann für Datenbankvorgänge verwendet werden.

Bei einem Fehler sind keine Sitzungen verfügbar, oder eine neue Sitzung konnte nicht initialisiert werden.

#### <a name="remarks"></a>Hinweise

Bei der Verwendung von Sitzungen über verschiedene Threads hinweg muss sorgfältig darauf geachtet werden. Eine Sitzung verfolgt, für welchen Thread sie während [JetBeginTransaction,](./jetbegintransaction-function.md) [JetCommitTransaction](./jetcommittransaction-function.md)oder [JetRollback](./jetrollback-function.md)verwendet wurde, und löst einen Fehler aus, wenn er in mehreren Threads mit einer geöffneten Transaktion verwendet wird. [JetResetSessionContext](./jetresetsessioncontext-function.md)und [JetSetSessionContext](./jetsetsessioncontext-function.md) können dieses Verhalten ändern. Da die Sitzung immer noch ein serialisierter Kontext ist und mehrere Datenbankvorgänge nicht gleichzeitig, sondern nur seriell für eine einzelne Sitzung ausgeführt werden können. Sie können jedoch mehrere Sitzungen verwenden, um gleichzeitigen Datenbankzugriff zu erhalten. Sitzungen können innerhalb einer Transaktion threadübergreifend verwendet werden, indem die Sitzungskontexte festgelegt und zurückgesetzt werden.

Das Sitzungshandle sollte mit [JetEndSession](./jetendsession-function.md)geschlossen werden.

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
<td><p>Deklariert in Esent.h.</p></td>
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
<td><p>Implementiert als <strong>JetBeginSessionW</strong> (Unicode) und <strong>JetBeginSessionA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetDupSession](./jetdupsession-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
