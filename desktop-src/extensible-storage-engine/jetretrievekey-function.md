---
description: 'Weitere Informationen finden Sie unter: jetretrievekey-Funktion'
title: JetRetrieveKey-Funktion
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050463"
---
# <a name="jetretrievekey-function"></a>JetRetrieveKey-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetretrievekey-function"></a>JetRetrieveKey-Funktion

Die **jetretrievekey** -Funktion Ruft den Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors ab. Diese Schlüssel werden durch Aufrufe von [jetmakekey](./jetmakekey-function.md)erstellt. Der abgerufene Schlüssel kann dann verwendet werden, um den Cursor mithilfe eines [JetSeek](./jetseek-function.md)-Aufrufes effizient an denselben Index Eintrag zurückzugeben.

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pvData*

Der Ausgabepuffer, der den Schlüssel empfängt.

*cbmax*

Die maximale Größe des Ausgabepuffers in Bytes.

*pcbactual*

Empfängt die tatsächliche Größe des Schlüssels in Byte.

Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des Schlüssels nicht zurückgegeben.

Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des Schlüssels weiterhin zurückgegeben. Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.

*grbit*

Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Wenn angegeben, gibt die Engine den Suchschlüssel für den Cursor zurück. Der Suchschlüssel wird mithilfe eines oder mehrerer vorheriger Aufrufe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt, um diesen Schlüssel mithilfe von <a href="gg294103(v=exchg.10).md">JetSeek</a> zu suchen oder einen Index Bereich mithilfe von <a href="gg294112(v=exchg.10).md">jetsetindexrange</a>festzulegen.</p></td>
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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Es ist kein aktueller Suchschlüssel für den Cursor vorhanden. Dies geschieht für <strong>jetretrievekey</strong> , wenn JET_bitRetrieveCopy angegeben wird und ein Suchschlüssel für diesen Cursor nicht mithilfe eines vorherigen Aufrufes von <a href="gg269329(v=exchg.10).md">jetmakekey</a>erstellt wurde. Der Suchschlüssel wird durch einen vorherigen-Aufrufvorgang für eine beliebige Navigations-API auf dem Cursor außer <a href="gg294117(v=exchg.10).md">jetmove</a>gelöscht.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Der Cursor ist nicht in einem Datensatz positioniert. Dafür sind viele verschiedene Gründe möglich. Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</p></td>
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
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um den gesamten Schlüssel zu empfangen. Der Ausgabepuffer wurde mit dem gleichen Wert wie der Schlüssel gefüllt. Die tatsächliche Größe des Schlüssels wurde auch zurückgegeben, wenn dies angefordert wurde.</p>
<p><strong>Hinweis</strong>   Dieser Fehler wird nicht zurückgegeben, wenn JET_bitRetrieveCopy angegeben wird. Weitere Informationen finden Sie im Abschnitt "Hinweise".</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird der Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors im Ausgabepuffer zurückgegeben. Wenn JET_wrnBufferTruncated zurückgegeben wird, enthält der Ausgabepuffer den großen Teil des Schlüssels, der in den bereitgestellten Speicherplatz passt, und die tatsächliche Größe des Schlüssels ist genau. Es erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler werden der Status des Ausgabepuffers und die tatsächliche Größe des Schlüssels nicht definiert. Es erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Schlüssel sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Allerdings können die folgenden Eigenschaften für alle ESENT-Schlüssel bekannt sein:

  - Schlüssel können miteinander verglichen werden, indem die [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) -Funktion verwendet wird, um ihre relative Reihenfolge im Ursprungs Index für die Tabelle der Quell Indexeinträge festzulegen.

  - Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.

  - Ein Schlüssel ist immer kleiner oder gleich JET_cbKeyMost (255) Bytes in der Länge vor Windows Vista. Unter Windows Vista und späteren Versionen können Schlüssel größer sein. Die maximale Größe eines Schlüssels ist gleich dem aktuellen Wert JET_paramKeyMost.

Zusätzlich zu den oben genannten Eigenschaften von ESENT-Schlüsseln ist es wichtig zu beachten, dass sich ein Suchschlüssel von dem Schlüssel für einen Index Eintrag unterscheidet. Ein Suchschlüssel ist möglicherweise länger als ein normaler Schlüssel. Diese zusätzliche Länge tritt auf, wenn beim Erstellen des Suchschlüssels eine Platzhalter Option verwendet wird. Weitere Informationen finden Sie unter [jetmakekey](./jetmakekey-function.md) .

Es gibt einen wichtigen Fehler in dieser API, der in allen Releases vorhanden ist. Wenn der Suchschlüssel mit der Verwendung von JET_bitRetrieveCopy angefordert wird und der Ausgabepuffer zu klein ist, um den gesamten Schlüssel zu empfangen, wird JET_wrnBufferTruncated nicht zurückgegeben. Stattdessen wird JET_errSuccess zurückgegeben. Es ist wichtig sicherzustellen, dass die tatsächliche Größe des Schlüssels, der mit *pcbactual* zurückgegeben wird, kleiner oder gleich der Größe des Ausgabepuffers ist. Wenn die tatsächliche Größe größer ist als die Größe des Ausgabepuffers, sollte der **Aufrufer von jetretrievekey** so reagieren, als ob JET_wrnBufferTruncated stattdessen zurückgegeben würden.

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
[JET_TABLEID](./jet-tableid.md)  
[Jetmakekey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[Jetsetindexrange](./jetsetindexrange-function.md)
