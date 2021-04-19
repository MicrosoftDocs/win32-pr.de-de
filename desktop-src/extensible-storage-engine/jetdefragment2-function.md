---
description: 'Weitere Informationen finden Sie hier: JetDefragment2-Funktion'
title: JetDefragment2-Funktion
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106360248"
---
# <a name="jetdefragment2-function"></a>JetDefragment2-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetdefragment2-function"></a>JetDefragment2-Funktion

Die **JetDefragment2** -Funktion startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern, wobei ein Rückruf Parameter verfügbar ist, um den Fortschritt der Defragmentierung zu melden. Dies erfolgt, um das Daten Bank Wachstum einzuschränken, indem die vorhandene Datenträger Zuordnung effizienter in der Datenbank verwendet wird. Außerdem kann der Arbeits Satz reduziert werden, indem sichergestellt wird, dass die Daten stärker verpackt werden. Schließlich kann die Anwendung die Anwendungsleistung verbessern, indem allgemeine Vorgänge durch eine bessere Datenorganisation beschleunigt werden.

**Windows XP:**  **JetDefragment2** wird in Windows XP eingeführt.

**JetDefragment2** enthält außerdem einen Rückruf Funktionsparameter, der verwendet wird, um einen Bericht über den Status des Defragmentierungsvorgangs zu berichten.

Die Daten Bank Defragmentierung ist ein Online Vorgang und unterbricht keine reguläre Datenbankaktivität, wie z. b. Abfrage Vorgänge oder Datenaktualisierungen. **JetDefragment2** macht auch keine Kopie aller vorhandenen Daten. Stattdessen wird eine Datenbank an Ort und Stelle zerlegt. Schließlich stellt **JetDefragment2** den internen Daten Bank Speicher für die erneute Verwendung wieder her, gibt jedoch keinen zusätzlichen Speicherplatz im Dateisystem des Betriebssystems frei.

Das resultierende Format der Daten kann viel effizienter sein, ist aber nicht in der Regel optimal. Die Defragmentierung ist auf das Freigeben von Datenbankseiten zur erneuten Verwendung beschränkt, die bereits logisch gelöschte Daten enthalten. Die Defragmentierung sorgt auch dafür, dass Datenbankseiten in einigen Fällen wieder verwendet werden können, indem Daten von zwei Seiten kombiniert werden, wenn Sie auf eine einzelne Seite passen.

Dieser Vorgang unterscheidet sich von [jetcompact](./jetcompact-function.md) , wodurch eine Kopie einer schreibgeschützten Datenbank in ein sehr optimales Formular umgewandelt wird.

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*DBID*

Die zu zerfragmentdatenbank.

*sztablename*

Nicht verwendeter Parameter. Die Defragmentierung wird für die gesamte Datenbank ausgeführt, die durch die angegebene Datenbank-ID beschrieben wird.

*pcpass*

Wenn eine Online Defragmentierung gestartet wird, wird durch diesen optionalen Eingabeparameter die maximale Anzahl von Defragmentierungs Läufen festgelegt. Wenn Sie eine Online Defragmentierung beenden, wird dieser optionale Ausgabepuffer auf die Anzahl der durchgeführten Durchgänge festgelegt.

Wenn dieser Parameter auf NULL festgelegt ist, ist die Anzahl der Online Defragmentierungs Überläufen unbegrenzt.

*pcseconds*

Beim Starten einer Online Defragmentierung-Aufgabe legt dieser optionale Eingabeparameter die maximale Zeit für die Defragmentierung fest. Wenn Sie eine Online Defragmentierung beenden, wird dieser optionale Ausgabepuffer auf die für die Defragmentierung verwendete Zeitspanne festgelegt.

Wenn dieser Parameter auf NULL festgelegt ist oder *pcseconds* auf einen negativen Wert zeigt, ist die maximale Zeit für die Defragmentierung unbegrenzt.

*Rückruf*

Rückruffunktion, die regelmäßig Aufrufe aufruft, um den Fortschritt zu melden.

*grbit*

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

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
<td><p>JET_bitDefragmentAvailSpaceTreesOnly</p></td>
<td><p>Diese Option wird verwendet, um den verfügbaren Speicherplatz der ESE-Daten Bank Speicher Belegung zu defragmentieren. Der Daten Bankbereich ist in zwei Typen unterteilt: eigener Speicherplatz und verfügbarer Speicherplatz. Der Speicherplatz ist einer Tabelle oder einem Index zugeordnet, während der verfügbare Speicherplatz für die Verwendung innerhalb der Tabelle bzw. des Indexes bereit ist. Der verfügbare Speicherplatz ist weitaus dynamischer als das Verhalten und erfordert eine Online Defragmentierung, die größer ist als der Speicherplatz im Besitz von Tabellen oder Indexdaten.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>Diese Option wird verwendet, um eine neue defragmentierungsaufgabe zu starten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>Diese Option wird verwendet, um eine vorhandene Defragmentierungs Aufgabe zu beenden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBTree</p></td>
<td><p>Diese Option wird verwendet, um eine B-Struktur zu defragmentieren.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>Die für die Defragmentierung gewählte Datenbank ist schreibgeschützt und kann in keiner Weise aktualisiert werden, einschließlich der Defragmentierung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDistributedTransactionAlreadyPreparedToCommit</p></td>
<td><p>Die angegebene Sitzung befindet sich im Status "vorbereitet für Commit" und kann erst dann neue Updates starten, wenn für die aktuelle Transaktion ein Commit oder ein Rollback ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>Die angegebene Datenbank-ID stimmt nicht mit einer bekannten Datenbank in der Instanz von identisch.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</p></td>
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
<td><p>Die angegebene Sitzung verfügt nur über schreibgeschützte Berechtigungen und kann keine Aufgabe starten, die möglicherweise ein Update ausführt, einschließlich Defragmentierung.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeicher nicht ausreicht, um alle ausstehenden Updates zu speichern.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragAlreadyRunning</p></td>
<td><p>Die JET_bitDefragmentBatchStart-Option wurde übergeben, aber eine defragmentierungsaufgabe führt bereits Defragmentierung für die angegebene Datenbank aus.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragNotRunning</p></td>
<td><p>Die JET_bitDefragmentBatchStop-Option wurde erfolgreich ausgeführt, aber zurzeit wird keine defragmentierungsaufgabe ausgeführt.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird die angeforderte Aktion zum Starten einer defragmentierungsaufgabe für eine bestimmte Daten mit den angegebenen Optionen ausgeführt, oder die Aktion zum Beenden einer vorhandenen defragmentierungsaufgabe wird ausgeführt.

Bei einem Fehler wird die angeforderte Aktion zum Starten oder Beenden eines Online defragmentierungsauftrags nicht durchgeführt. Es treten keine anderen Nebeneffekte auf.

#### <a name="remarks"></a>Bemerkungen

Die Online Defragmentierung wird sowohl durch eine Parametereinstellung als auch durch diese API gesteuert. Der Standardwert für den Systemparameter ist JET_OnlineDefragAll. Dies bedeutet, dass die Defragmentierung für alle unterstützten Datenstrukturen aktiviert ist. Mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md)ist es jedoch möglich, die Online Defragmentierung zu deaktivieren oder Sie selektiv nur für Daten Bank Raumstrukturen, nur Datenbanken, Streamingdateien oder eine beliebige Kombination dieser Optionen zu aktivieren. Wenn die Systemeinstellung für die Online Defragmentierung auf eine veraltete Einstellung festgelegt ist, wird die Einstellung von **JetDefragment2** als JET_OnlineDefragAll behandelt.

Es kann höchstens eine Aufgabe für jede Datenbank ausgeführt werden. Der Task wird in dem Prozess, der ESE gehostet, als Thread ausgeführt.

Die Sitzung, mit der die Online Defragmentierung-Aufgabe gestartet wird, kann anschließend für Daten Bank Vorgänge verwendet werden, während der Defragmentierungstask fortgesetzt wird, da die Defragmentierungs Aufgabe eine eigene Sitzung zuordnet. Die angegebene Sitzung wird nur verwendet, um die Berechtigungen zu überprüfen, die der Startzeit der Aufgabe zugeordnet sind, und wird nicht tatsächlich für die Defragmentierungsvorgänge selbst verwendet.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
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
<td><p>Implementiert als <strong>JetDefragment2W</strong> (Unicode) und <strong>JetDefragment2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[Jetcompact](./jetcompact-function.md)  
[Jetdebug](./jetdefragment-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)  
[Jetstopservice](./jetstopservice-function.md)
