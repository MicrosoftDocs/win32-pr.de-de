---
description: 'Weitere Informationen zu: JetGetLock-Funktion'
title: JetGetLock-Funktion
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51509f4027d4748f32b8c9dfb8756433b5f93935
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984833"
---
# <a name="jetgetlock-function"></a>JetGetLock-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetlock-function"></a>JetGetLock-Funktion

Die **JetGetLock-Funktion** bietet eine Möglichkeit, eine Zeile explizit zu aktualisieren, eine Schreibsperre zu schreiben oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung aktualisiert wird( Lesesperre). Normalerweise werden Zeilenschreibsperren implizit als Ergebnis der Aktualisierung von Zeilen eingerichtet. Lesesperren sind aufgrund der Datensatzversionsierung in der Regel nicht erforderlich. In einigen Fällen möchte eine Transaktion jedoch möglicherweise explizit eine Zeile sperren, um die Serialisierung zu erzwingen, oder um sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ist, da die erforderlichen Sperren bereits eingerichtet wurden.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet wird.

*tableid*

Der Cursor, der für diesen Aufruf verwendet wird.

*grbit*

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Elemente enthalten:


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitReadLock</p> | <p>Dieses Flag bewirkt, dass eine Lesesperre für den aktuellen Datensatz eingerichtet wird. Lesesperren sind nicht kompatibel mit Schreibsperren, die bereits von anderen Sitzungen gehalten werden, sind aber mit Lesesperren kompatibel, die von anderen Sitzungen gehalten werden.</p> | 
| <p>JET_bitWriteLock</p> | <p>Dieses Flag bewirkt, dass eine Schreibsperre für den aktuellen Datensatz eingerichtet wird. Schreibsperren sind nicht mit Schreib- oder Lesesperren kompatibel, die von anderen Sitzungen gehalten werden, sind jedoch mit Lesesperren kompatibel, die von derselben Sitzung gehalten werden.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Das angegebene <em>Grbit</em> ist weder JET_bitReadLock noch JET_bitWriteLock. Es muss eines dieser beiden Flags sein.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Der Cursor muss sich in einem Datensatz befindet, um eine Sperre zu erhalten. Sperren sind immer für Datensätze aktiviert.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Sperren können nur von Sitzungen in einer Transaktion eingerichtet werden.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Cursor kann nicht schreibbar sein und erhält eine Schreibsperre.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Die Sitzung muss über Schreibberechtigungen verfügen, um die Schreibsperre zu erhalten.</p> | 
| <p>JET_errWriteConflict</p> | <p>Der Fehler, der zurückgegeben wird, wenn eine in Konflikt geratene Sperre angefordert wird.</p> | 



Bei Erfolg hat die Sitzung die angeforderte Sperre abgerufen.

Bei einem Fehler hat die Sitzung die angeforderte Sperre nicht abgerufen.

#### <a name="remarks"></a>Bemerkungen

Schreibsperren können nicht mit Sitzungen oder Cursorn mit schreibgeschützten Berechtigungen abgerufen werden, auch wenn die Sitzung und der Cursor letztendlich keinen Aktualisierungsvorgang ausführen. Sowohl die Sitzung als auch der Cursor müssen über Schreibberechtigungen verfügen, um eine Schreibsperre zu erhalten.

Lese- und Schreibsperren sind ein Mittel zur pessimistischen Sperrung. Bei der pessimistischen Sperrung wird erwartet, dass mehrere gleichzeitige Sitzungen in Konflikt geraten und Sperren im Voraus eingerichtet werden, um sicherzustellen, dass ihre Vorgänge erfolgreich sind.

Die meisten Vorgänge sind aufgrund impliziter Sperren serialisierbar. Einige Vorgänge werden jedoch nicht durchgeführt. Betrachten Sie die beiden Transaktionen, um dies zu veranschaulichen:

T1 : R(A), U(B)

T2 : R(B), U(A)

Durch die Versionsangaben auf Datensatzebene wird sichergestellt, dass bei gleichzeitiger Ausführung jeder Transaktion die ursprünglichen Werte für A und B angezeigt werden. Es gibt keine serielle Ausführungsreihenfolge, die die gleichen Ergebnisse für A und B erzeugen kann, falls die Ergebnisse von den gelesenen Daten abhängig sind. Damit die Anwendung diese Transaktion serialisierbar machen kann, sollte sie eine explizite Lesesperre für A und B in jeder Transaktion erhalten, wenn der Wert gelesen wird.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
