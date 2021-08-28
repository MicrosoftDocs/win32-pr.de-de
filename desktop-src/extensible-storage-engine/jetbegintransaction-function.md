---
description: 'Weitere Informationen zu: JetBeginTransaction-Funktion'
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
ms.openlocfilehash: 991f80ab346ae039c6222a508374de806d0faf2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479266"
---
# <a name="jetbegintransaction-function"></a>JetBeginTransaction-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetbegintransaction-function"></a>JetBeginTransaction-Funktion

Die **JetBeginTransaction-Funktion** bewirkt, dass eine Sitzung eine Transaktion eingibt und einen neuen Sicherungspunkt erstellt. Diese Funktion kann in einer einzelnen Sitzung mehr als einmal aufgerufen werden, um die Erstellung zusätzlicher Speicherpunkte zu verursachen. Diese Sicherungspunkte können verwendet werden, um Änderungen am Zustand der Datenbank selektiv beizubehalten oder zu verwerfen.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parameter

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, als Ergebnis eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService</a>aufgetreten sind.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da für die instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p><p>Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errNotInitialized</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz noch nicht initialisiert wurde.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da ein Wiederherstellungsvorgang für die Instanz ausgeführt wird, die der Sitzung zugeordnet ist.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Dieselbe Sitzung kann nicht für mehrere Threads gleichzeitig verwendet werden. Dieser Fehler wird nur von Windows XP und späteren Versionen zurückgegeben.</p> | 
| <p>JET_errTermInProgress</p> | <p>Es ist nicht möglich, den Vorgang abzuschließen, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Eine neue Transaktion kann nicht gestartet werden, da die Sitzung bereits die maximale Speicherpunkttiefe erreicht, die von der Datenbank-Engine zugelassen wird.</p> | 



Bei Erfolg befindet sich die bereitgestellte Sitzung innerhalb einer Transaktion. Wenn sich die Sitzung zuvor innerhalb einer Transaktion befand, wird ein neuer Speicherpunkt erstellt.

Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert. Es wird keine Änderung am Datenbankzustand vorgenommen.

#### <a name="remarks"></a>Hinweise

Die Datenbank-Engine stellt ein Momentaufnahmeisolationsmodell für ihre Transaktionen bereit. Dies bedeutet, dass, wenn eine Sitzung zum ersten Mal in einen Transaktionszustand wechselt, die gesamte Datenbank zu Beginn der Transaktion eingefroren wird. Eine Sitzung muss keine Daten lesen, da sie immer auf die entsprechende Version dieser Daten zugreifen kann. Dies bedeutet, dass eine Sitzung, die Daten aktualisiert, niemals verhindert, dass eine andere Sitzung diese Daten liest.

Eine weitere Auswirkung der Verwendung der Momentaufnahmeisolation ist das Sperrmodell, das für Updates verwendet wird. Die Datenbank-Engine vergibt eine Schreibsperre für einen bestimmten Datenteil an die erste Sitzung, die sie anfordert. Diese Schreibsperre wird aufgehoben, wenn für die Transaktion entweder ein Commit ausgeführt oder vollständig abgebrochen wird, sodass sich die Sitzung nicht mehr in einer Transaktion befindet. Während eine Sitzung eine Schreibsperre enthält, wird jede andere Sitzung, die dieselbe Schreibsperre anfordert, erst dann blockiert, wenn die Schreibsperre verfügbar ist. Stattdessen schlägt diese zweite Sitzung sofort mit JET_errWriteConflict fehl. Um diesen Konflikt zu lösen, muss die zweite Sitzung ihre Transaktion vollständig abbrechen (oder committen), einige kurze Zeit warten, bis die erste Sitzung einen Commit oder Abbruch ihrer Transaktion ausgeführt hat, und dann von vorn beginnen.

Zur Unterstützung der Momentaufnahmeisolation speichert die Datenbank-Engine alle Versionen aller geänderten Daten im Arbeitsspeicher, seit die älteste aktive Transaktion in einer Sitzung zum ersten Mal gestartet wurde. Dies hat wichtige Auswirkungen auf Ihre Anwendung. Jedes Verhalten, das dazu führt, dass eine große Anzahl von Versionen im Arbeitsspeicher erstellt wird, kann dazu führen, dass die Instanz ihre maximale Größe des Versionsspeichers erschöpft (weitere Informationen finden Sie unter [JET_paramMaxVerPages](./resource-parameters.md) in [Systemparametern).](./extensible-storage-engine-system-parameters.md) Ein solches Verhalten umfasst, ist aber nicht auf sehr große Updates in einer einzelnen Transaktion und sehr lang andauernde Transaktionen beschränkt. Daher ist es sehr wichtig, die Größe des Versionsspeichers für die erwartete Transaktionslast der Anwendung ordnungsgemäß zu konfigurieren. Es ist auch wichtig, die Anzahl der Updates, die in einer einzelnen Transaktion ausgeführt werden, mit großer Sorgfalt zu begrenzen. Darüber hinaus ist es wichtig, Transaktionen in Szenarien mit hoher Auslastung so kurz wie möglich zu gestalten.

Es wird dringend empfohlen, dass sich die Anwendung immer im Kontext einer Transaktion befindet, wenn ESE-APIs aufgerufen werden, die Daten abrufen oder aktualisieren. Wenn dies nicht erfolgt, umschließt die Datenbank-Engine automatisch jeden ESE-API-Aufruf dieses Typs in einer Transaktion im Auftrag der Anwendung. Die Kosten dieser sehr kurzen Transaktionen können sich in einigen Fällen schnell summieren.

Das Standardverhalten der Engine besteht darin, die Verwendung einer Sitzung auf denselben Thread von dem Zeitpunkt des ersten Aufrufs von **JetBeginTransaction** bis zu dem Zeitpunkt, zu dem der entsprechende Aufruf von [JetCommitTransaction](./jetcommittransaction-function.md) oder [JetRollback](./jetrollback-function.md) erfolgt, einzuschränken. Dieses Verhalten kann geändert werden, um diese Einschränkung durch Festlegen eines benutzerdefinierten Sitzungskontexts mit [JetSetSessionContext](./jetsetsessioncontext-function.md) und [JetResetSessionContext](./jetresetsessioncontext-function.md)zu entfernen.

Die Datenbank-Engine unterstützt auch Transaktionsschemaänderungen. Beispielsweise ist es möglich, eine neue Transaktion zu starten, eine Tabelle zu erstellen, einige Spalten hinzuzufügen, einen oder zwei Indizes zu erstellen und dann die Transaktion abzubricht. Die soeben hinzugefügten Schemaelemente werden aus der Datenbank entfernt. Es ist auch möglich, Schemaänderungen und gewöhnliche Datenbankupdates in derselben Transaktion zu kombinieren.

#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
