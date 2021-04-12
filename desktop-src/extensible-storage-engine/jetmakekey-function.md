---
description: 'Weitere Informationen finden Sie unter: jetmakekey-Funktion'
title: JetMakeKey-Funktion
TOCTitle: JetMakeKey Function
ms:assetid: 8c1cff2f-2f24-4990-a9d8-fb4f822e50b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269329(v=EXCHG.10)
ms:contentKeyID: 32765619
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMakeKey
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3d121ed83f096baad249aab8677bb9f5e72e301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217851"
---
# <a name="jetmakekey-function"></a>JetMakeKey-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetmakekey-function"></a>JetMakeKey-Funktion

Die **jetmakekey** -Funktion erstellt Suchschlüssel, die dann verwendet werden können, um einen Satz von Einträgen in einem Index durch einige einfache Suchkriterien für Ihre Schlüssel Spaltenwerte zu suchen. Ein Suchschlüssel ist auch eine der systeminternen Eigenschaften eines Cursors und wird von den [JetSeek](./jetseek-function.md) -und [jetsetindexrange](./jetsetindexrange-function.md) -Vorgängen verwendet, um Indexeinträge zu suchen, die mit diesen Suchkriterien für den aktuellen Index dieses Cursors übereinstimmen. Ein kompletter Suchschlüssel wird in einer Reihe von **jetmakekey** -aufrufen erstellt, wobei jeder Aufruf verwendet wird, um den Spaltenwert für die nächste Schlüssel Spalte des aktuellen Index eines Cursors zu laden. Es ist auch möglich, einen zuvor erstellten Suchschlüssel zu laden, der mithilfe von [jetretrievekey](./jetretrievekey-function.md)aus dem Cursor abgerufen wurde.

```cpp
    JET_ERR JET_API JetMakeKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*pvData*

Der Eingabepuffer, der die Spaltendaten für die aktuelle Schlüssel Spalte des aktuellen Index des Cursors enthält, für den der Suchschlüssel erstellt wird.

Der Datentyp der Spaltendaten im Eingabepuffer muss exakt mit dem Datentyp und anderen Eigenschaften der Spaltendefinition der aktuellen Schlüssel Spalte übereinstimmen. Für die Spaltendaten wird keinerlei Typumwandlung durchgeführt.

Wenn JET_bitNormalizedKey im *grbit* -Parameter angegeben wird, muss der Eingabepuffer einen zuvor erstellten Suchschlüssel enthalten. Diese Schlüssel werden mit einem [calltretrievekey](./jetretrievekey-function.md)-Befehl abgerufen.

*cbData*

Die Größe der Spaltendaten in Bytes, die im Eingabepuffer bereitgestellt werden.

Wenn JET_bitNormalizedKey im *grbit* -Parameter angegeben wird, ist dies die Größe des Suchschlüssels, der im Eingabepuffer angegeben wird.

Wenn die Größe der Spaltendaten 0 (null) ist, wird der Inhalt des Eingabe Puffers ignoriert. Wenn JET_bitKeyDataZeroLength im *grbit* -Parameter angegeben wird und die aktuelle Schlüssel Spalte des aktuellen Index des Cursors eine Spalte variabler Länge ist, wird davon ausgegangen, dass die Daten der Eingabe Spalte einen Wert von 0 (null) aufweisen. Andernfalls wird davon ausgegangen, dass die Eingabe Spaltendaten ein NULL-Wert sind.

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
<td><p>JET_bitFullColumnEndLimit</p></td>
<td><p>Der Suchschlüssel sollte so erstellt werden, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden. Dies bedeutet, dass der erstellte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die über Folgendes verfügen:</p>
<ul>
<li><p>Die genauen Spaltenwerte, die für diese Schlüssel Spalte und alle vorherigen Schlüssel Spalten bereitgestellt werden.</p></li>
<li><p>Alle Spaltenwerte, die für nachfolgende Schlüssel Spalten erforderlich sind.</p></li>
</ul>
<p>Diese Option sollte zum Entwickeln von Platzhalter-Suchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden, die dem Ende eines Indexes am nächsten sind. Das Ende des Indexes ist der Index Eintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wurde. Das Ende des Indexes ist nicht mit dem hohen Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Diese Option ist nur unter Windows XP und höheren Versionen verfügbar.</p></td>
</tr>
<tr class="even">
<td><p>Jetbitfullcolumnstartlimit</p></td>
<td><p>Der Suchschlüssel sollte so erstellt werden, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden. Dies bedeutet, dass der erstellte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die über Folgendes verfügen:</p>
<ul>
<li><p>Die genauen Spaltenwerte, die für diese Schlüssel Spalte und alle vorherigen Schlüssel Spalten bereitgestellt werden.</p></li>
<li><p>Alle Spaltenwerte, die für nachfolgende Schlüssel Spalten erforderlich sind.</p></li>
</ul>
<p>Diese Option sollte zum Entwickeln von Platzhalter-Suchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden, die dem Anfang eines Indexes am nächsten sind. Der Index Anfang ist der Index Eintrag, der beim Verschieben in den ersten Datensatz in diesem Index gefunden wird. Der Index Anfang ist nicht mit dem unteren Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Diese Option ist nur unter Windows XP und höheren Versionen verfügbar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitKeyDataZeroLength</p></td>
<td><p>Wenn die Größe des Eingabe Puffers NULL und die aktuelle Schlüssel Spalte eine Spalte variabler Länge ist, gibt diese Option an, dass der Eingabepuffer den Wert 0 (null) enthält. Andernfalls würde eine Eingabepuffergröße von NULL einen NULL-Wert angeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNewKey</p></td>
<td><p>Es muss ein neuer Suchschlüssel erstellt werden. Alle bereits vorhandenen Suchschlüssel werden verworfen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitNormalizedKey</p></td>
<td><p>Wenn diese Option angegeben wird, werden alle anderen Optionen ignoriert, alle bereits vorhandenen Suchschlüssel werden verworfen, und der Inhalt des Eingabe Puffers wird als neuer Suchschlüssel geladen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitPartialColumnEndLimit</p></td>
<td><p>Der Suchschlüssel sollte so erstellt werden, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen. Dies bedeutet, dass der erstellte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die über Folgendes verfügen:</p>
<ul>
<li><p>Die genauen Spaltenwerte, die für diese Schlüssel Spalte und alle vorherigen Schlüssel Spalten bereitgestellt werden.</p></li>
<li><p>Alle Spaltenwerte, die für nachfolgende Schlüssel Spalten erforderlich sind.</p></li>
</ul>
<p>Diese Option sollte zum Entwickeln von Platzhalter-Suchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden, die dem Ende eines Indexes am nächsten sind. Das Ende des Indexes ist der Index Eintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wurde. Das Ende des Indexes ist nicht mit dem hohen Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Diese Option kann nicht verwendet werden, wenn die aktuelle Schlüssel Spalte weder eine Text Spalte noch eine binäre Variablen Spalte ist. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</p>
<p>Diese Option ist nur unter Windows XP und höheren Versionen verfügbar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitPartialColumnStartLimit</p></td>
<td><p>Diese Option gibt an, dass der Suchschlüssel so erstellt werden soll, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen. Dies bedeutet, dass der erstellte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die über Folgendes verfügen:</p>
<ul>
<li><p>Die genauen Spaltenwerte, die für diese Schlüssel Spalte und alle vorherigen Schlüssel Spalten bereitgestellt werden.</p></li>
<li><p>Alle Spaltenwerte, die für nachfolgende Schlüssel Spalten erforderlich sind.</p></li>
</ul>
<p>Diese Option sollte zum Entwickeln von Platzhalter-Suchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden, die dem Anfang eines Indexes am nächsten sind. Der Index Anfang ist der Index Eintrag, der beim Verschieben in den ersten Datensatz in diesem Index gefunden wird. Der Index Anfang ist nicht mit dem unteren Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Diese Option kann nicht verwendet werden, wenn die aktuelle Schlüssel Spalte weder eine Text Spalte noch eine binäre Variablen Spalte ist. Der Vorgang schlägt mit JET_errInvalidgrbit fehl, wenn ein Versuch unternommen wird.</p>
<p>Diese Option ist nur unter Windows XP und höheren Versionen verfügbar.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStrLimit</p></td>
<td><p>Diese Option gibt an, dass der Suchschlüssel so erstellt werden soll, dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen. Dies bedeutet, dass der erstellte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die über Folgendes verfügen:</p>
<ul>
<li><p>Die genauen Spaltenwerte, die für diese Schlüssel Spalte und alle vorherigen Schlüssel Spalten bereitgestellt werden.</p></li>
<li><p>Alle Spaltenwerte, die für nachfolgende Schlüssel Spalten erforderlich sind.</p></li>
</ul>
<p>Diese Option sollte zum Entwickeln von Platzhalter-Suchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden, die dem Ende eines Indexes am nächsten sind. Das Ende des Indexes ist der Index Eintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wurde. Das Ende des Indexes ist nicht mit dem hohen Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Wenn diese Option in Kombination mit JET_bitSubStrLimit angegeben wird und die aktuelle Schlüssel Spalte eine Text Spalte ist, wird diese Option ignoriert. Dieses Verhalten soll ermöglichen, dass der Typ der aktuellen Schlüssel Spalte bei der Erstellung des Suchschlüssels abgeleitet wird.</p>
<p>Wenn Sie einen ähnlichen Suchschlüssel für den Anfang eines Indexes erstellen möchten, sollten Sie einen ähnlichen Befehl von <strong>jetmakekey</strong> für die letzte Schlüssel Spalte, die kein Platzhalter ist, aber ohne festgelegte Platzhalter Optionen erstellen. Der Suchschlüssel befindet sich dann in einem geeigneten Zustand, der für eine solche Suche verwendet werden kann. Dies entspricht der Verwendung von JET_bitFullColumnStartLimit, mit dem Unterschied, dass der Suchschlüssel nicht ordnungsgemäß abgeschlossen ist, da er nach der Verwendung einer Platzhalter Option verwendet wird.</p>
<p>Diese Option wurde für Windows XP und spätere Versionen als veraltet markiert, um diese umständliche Semantik zu beheben. JET_bitFullColumnStartLimit und JET_bitFullColumnEndLimit sollten immer dann verwendet werden, wenn dies möglich ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSubStrLimit</p></td>
<td><p>Diese Option gibt an, dass der Suchschlüssel so erstellt werden soll, dass die aktuelle Schlüssel Spalte als Präfix-Platzhalter angesehen wird und dass alle Schlüssel Spalten, die nach der aktuellen Schlüssel Spalte liegen, als Platzhalter betrachtet werden sollen. Dies bedeutet, dass der erstellte Suchschlüssel verwendet werden kann, um Indexeinträge abzugleichen, die über Folgendes verfügen:</p>
<ul>
<li><p>Die genauen Spaltenwerte, die für alle vorherigen Schlüssel Spalten bereitgestellt werden.</p></li>
<li><p>Die angegebenen Spaltendaten als Präfix des Spaltenwerts für die aktuelle Schlüssel Spalte.</p></li>
<li><p>Alle Spaltenwerte für nachfolgende Schlüssel Spalten.</p></li>
</ul>
<p>Diese Option sollte zum Entwickeln von Platzhalter-Suchschlüsseln verwendet werden, die zum Suchen von Indexeinträgen verwendet werden, die dem Ende eines Indexes am nächsten sind. Das Ende des Indexes ist der Index Eintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wurde. Das Ende des Indexes ist nicht mit dem hohen Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</p>
<p>Wenn diese Option in Kombination mit JET_bitStrLimit angegeben wird und die aktuelle Schlüssel Spalte eine Text Spalte ist, hat diese Option Vorrang. Diese Option wird ignoriert, wenn es sich bei der aktuellen Schlüssel Spalte nicht um eine Text Spalte handelt. Dieses Verhalten soll ermöglichen, dass der Typ der aktuellen Schlüssel Spalte bei der Erstellung des Suchschlüssels abgeleitet wird.</p>
<p>Wenn Sie einen ähnlichen Suchschlüssel für den Anfang eines Indexes erstellen möchten, sollten Sie einen ähnlichen <strong>jetmakekey</strong> -Befehl für die Schlüssel Spalte erstellen, die als Präfix-Platzhalter festgelegt wird, wobei jedoch keine Platzhalter Optionen angegeben werden. Der Suchschlüssel befindet sich dann in einem geeigneten Zustand, der für eine solche Suche verwendet werden kann. Dies entspricht der Verwendung von JET_bitPartialColumnStartLimit, mit dem Unterschied, dass der Suchschlüssel nicht ordnungsgemäß abgeschlossen ist, da er nach der Verwendung einer Platzhalter Option verwendet wird.</p>
<p>Diese Option wurde für Windows XP und spätere Versionen als veraltet markiert, um diese umständliche Semantik zu beheben. JET_bitPartialColumnStartLimit und JET_bitPartialColumnEndLimit sollten stattdessen verwendet werden, wenn möglich.</p></td>
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
<td><p>JET_errIndexTuplesKeyTooSmall</p></td>
<td><p>Die angegebenen Spaltendaten waren zu klein, um einen gültigen Schlüssel für den aktuellen Index zu erstellen, da es sich bei diesem Index um einen Tupelindex handelt und die minimale Tupelgröße größer als die angegebenen Spaltendaten war. Weitere Informationen zu tupelindizes finden Sie unter <a href="gg294099(v=exchg.10).md">jetkreateindex</a> . Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen. Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Die angegebenen Spaltendaten entsprechen nicht der Größe, die für die Spaltendefinition erforderlich ist. Dies kann vorkommen, wenn der Datentyp der Spalte intrinsisch eine bestimmte Größe hat. Dies kann auch vorkommen, wenn der Datentyp der Spalte nicht intrinsisch eine bestimmte Größe hat, aber die Definition der Spalte eine festgelegte Länge deklariert. Eine Ausnahme besteht darin, dass dieser Fehler nicht auftritt, wenn für eine Text Spalte mit fester Länge zu wenig Daten bereitgestellt werden, da fehlende Daten automatisch mit Leerzeichen aufgefüllt werden. Eine zweite Ausnahme besteht darin, dass dieser Fehler nicht auftritt, wenn zu wenig Daten für eine binäre Spalte mit fester Länge bereitgestellt werden, da fehlende Daten automatisch mit Nullen aufgefüllt werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig, wird in unzulässiger Weise verwendet oder nicht implementiert. Dies kann bei <strong>jetmakekey</strong> vorkommen, wenn Folgendes geschieht:</p>
<ul>
<li><p>JET_bitPartialColumnStartLimit oder JET_bitPartialColumnEndLimit werden angegeben, und die entsprechende Schlüssel Spalte ist keine Text Spalte und keine binäre Spalte variabler Länge. Dieser Fall tritt nur unter Windows XP und höheren Versionen auf.</p></li>
<li><p>Es wird versucht, mehr als eine der folgenden Optionen zu verwenden: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit und JET_bitFullColumnEndLimit. Dieser Fall tritt nur unter Windows XP und höheren Versionen auf.</p></li>
<li><p>Es wurde versucht, JET_bitStrLimit oder JET_bitSubStrLimit zu verwenden, wenn eine der folgenden Optionen verwendet wird: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit und JET_bitFullColumnEndLimit. Dieser Fall tritt nur unter Windows XP und höheren Versionen auf.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</p>
<p>Dies kann bei <strong>jetmakekey</strong> vorkommen, wenn JET_bitNormalizedKey angegeben wurde und der im Eingabepuffer angegebene Wert zu groß ist, um ein gültiger Suchschlüssel zu sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade</p></td>
<td><p>Die für <strong>jetmakekey</strong> bereitgestellten Spaltendaten wurden zurückgewiesen, weil Spaltendaten bereits für alle Schlüssel Spalten im aktuellen Index bereitgestellt wurden. Dies kann auf drei Arten erfolgen. Die erste Möglichkeit ist, wenn Spaltendaten für jede Schlüssel Spalte im aktuellen Index bereitgestellt werden. Die zweite Möglichkeit ist, wenn Spaltendaten für mindestens eine Schlüssel Spalte bereitgestellt wurden und für den letzten-Befehl eine Platzhalter Option ausgewählt wurde. Die dritte Möglichkeit ist, dass ein zuvor erstellter Suchschlüssel mit JET_bitNormalizedKey bereitgestellt wurde, der alle Schlüssel Spalten abdeckt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Es ist kein aktueller Suchschlüssel für den Cursor vorhanden. Dies geschieht für <strong>jetmakekey</strong> , wenn JET_bitNewKey nicht angegeben ist und ein Suchschlüssel für diesen Cursor nicht mithilfe eines vorherigen Aufrufes von <strong>jetmakekey</strong>erstellt wurde. Der Suchschlüssel wird durch einen vorherigen-Aufrufvorgang für eine beliebige Navigations-API auf dem Cursor außer <a href="gg294117(v=exchg.10).md">jetmove</a>gelöscht.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Es ist kein aktueller Index für den Cursor vorhanden. Dies geschieht für <strong>jetmakekey</strong> , wenn sich der Cursor auf dem gruppierten Index einer Tabelle befindet, kein primärer Index definiert wurde und JET_bitNormalizedKey nicht angegeben wurde. Es ist nicht möglich, einen Suchschlüssel zu erstellen, wenn sich der Cursor in einem Index befindet, der keine Schlüssel Spalten besitzt, es sei denn, es wurde ein zuvor erstellter Suchschlüssel bereitgestellt.</p></td>
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
</tbody>
</table>


Bei Erfolg, wenn JET_bitNormalizedKey und JET_bitNewKey nicht angegeben wurden, wird der Suchschlüssel anhand der Suchkriterien für eine weitere Schlüssel Spalte im aktuellen Index erstellt. Wenn JET_bitNormalizedKey nicht angegeben wurde und JET_bitNewKey angegeben wurde, wurde ein zuvor vorhandener Suchschlüssel verworfen und ein neuer, der durch die Suchkriterien für die erste Schlüssel Spalte im aktuellen Index erstellt wurde. Wenn JET_bitNormalizedKey angegeben wurde, wurde ein zuvor vorhandener Suchschlüssel verworfen und ein neuer, der aus dem Eingabepuffer geladen wurde. In jedem Fall erfolgt keine Änderung des Daten Bank Status.

Bei einem Fehler, wenn JET_bitNormalizedKey oder JET_bitNewKey angegeben wurde, ist der Status des Suchschlüssels nicht definiert. Wenn weder JET_bitNormalizedKey noch JET_bitNewKey angegeben wurden, erfolgt keine Änderung des Zustands des Suchschlüssels. In jedem Fall erfolgt keine Änderung des Daten Bank Status.

#### <a name="remarks"></a>Bemerkungen

Schlüssel sollten als nicht transparente Datenblöcke behandelt werden. Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen. Allerdings sind die folgenden Informationen zu allen ESENT-Schlüsseln bekannt:

  - Schlüssel können mit [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) miteinander verglichen werden, um ihre relative Reihenfolge im Ursprungs Index für die Tabelle der Quell Indexeinträge festzulegen.

  - Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.

  - Ein Schlüssel ist immer kleiner oder gleich JET_cbKeyMost (255) Bytes in der Länge vor Windows Vista. Unter Windows Vista und späteren Versionen können Schlüssel größer sein. Die maximale Größe eines Schlüssels ist gleich dem aktuellen Wert JET_paramKeyMost.

Suchschlüssel können ein Byte länger sein, wenn eine Platzhalter Option verwendet wurde. In diesem Fall ist der Suchschlüssel bis zu JET_cbLimitKeyMost (256) Bytes für Releases vor Windows Vista und JET_paramKeyMost + 1 Bytes für Windows Vista und spätere Versionen.

Diese maximale Schlüsselgröße ist äußerst wichtig. Jedes Mal, wenn ein Index Eintrag mit Spaltenwerten vorhanden ist, die groß genug sind, um zu bewirken, dass für diesen Index ein Schlüssel generiert wird, der andernfalls größer als diese maximale Größe ist, wird der Schlüssel automatisch mit dieser maximalen Größe abgeschnitten. Dies hat zwei Auswirkungen:

  - Bei Einträgen in einem eindeutigen Index führt dies dazu, dass Einträge, die andernfalls eindeutig sind, als Duplikate deklariert werden.

  - Bei Einträgen in allen Indizes bewirkt das Abschneiden von Schlüsseln, dass Indexeinträge, die andernfalls nicht mit den Suchkriterien eines bestimmten Suchschlüssels übereinstimmen, als Übereinstimmungen deklariert werden.

Anwendungen müssen diese Abkürzung vorhersehen und entweder vermeiden oder ihre Auswirkungen kompensieren. In Windows Vista wurde ein neues indexflag ("JET_bitIndexDisallowTruncation") hinzugefügt, um es Anwendungen zu vereinfachen, schlüsseltruncations zu verhindern. Weitere Informationen zu dieser Indizierungs Option finden Sie in der [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Struktur.

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
[Jetkreateingedex](./jetcreateindex-function.md)  
[Jetretrievekey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[Jetsetindexrange](./jetsetindexrange-function.md)
