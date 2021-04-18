---
description: 'Weitere Informationen über: jetintersectindexes-Funktion'
title: JetIntersectIndexes-Funktion
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344651"
---
# <a name="jetintersectindexes-function"></a>JetIntersectIndexes-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetintersectindexes-function"></a>JetIntersectIndexes-Funktion

Die **jetintersectindexes** -Funktion berechnet die Schnittmenge zwischen mehreren Sätzen von Indexeinträgen aus unterschiedlichen sekundären Indizes für dieselbe Tabelle. Dieser Vorgang ist nützlich, um die Gruppe von Datensätzen in einer Tabelle zu suchen, die mit zwei oder mehr Kriterien übereinstimmen, die mithilfe von Index Bereichen ausgedrückt werden können.

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Die Sitzung, die für diesen-Befehl verwendet werden soll.

*rgindexrange*

Ein Zeiger auf ein Array von [JET_IndexRange](./jet-indexrange-structure.md) Strukturen. Jede Struktur enthält eine [JET_TABLEID](./jet-tableid.md) , die zum Speichern eines der zu überschneidenden Index Bereiche eingerichtet wurde. Weitere Informationen finden Sie unter [JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

Die Anzahl der [JET_IndexRange](./jet-indexrange-structure.md) Strukturen im-Array, die im *rgindexrange* -Parameter enthalten sind.

*precordlist*

Zeiger auf eine [JET_RECORDLIST](./jet-recordlist-structure.md) -Struktur. Diese Struktur wird mit ausreichenden Informationen aufgefüllt, um die temporäre Tabelle mit den Ergebnissen von **jetintersectindexes** zu durchlaufen.

Der Ausgabepuffer, der eine [JET_RECORDLIST](./jet-recordlist-structure.md) Struktur empfängt. Die Struktur enthält eine Beschreibung des Resultsets der Schnittmenge.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig, wurde falsch verwendet oder nicht implementiert.</p>
<p>Dieser Fehler wird von <strong>jetintersectindexes</strong> zurückgegeben, wenn Folgendes gilt:</p>
<p>Das in der <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> Struktur enthaltene <em>grbit</em> , auf das von einem Element im <em>rgindexrange</em> -Array verwiesen wird, ist nicht gleich JET_bitRecordInIndex.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der angegebenen Parameter enthält einen unerwarteten Wert oder einen Wert, der inkonsistent ist, wenn er mit dem Wert eines anderen Parameters kombiniert wird.</p>
<p>Dieser Fehler wird von <strong>jetintersectindexes</strong> aus den folgenden Gründen zurückgegeben:</p>
<ul>
<li><p>Der <em>precordlist</em> -Parameter ist NULL.</p></li>
<li><p>Der <strong>cbStruct</strong> -Member der im <em>precordlist</em> -Parameter angegebenen <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> Struktur entspricht nicht der Größe der <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> Struktur.</p></li>
<li><p>Der <em>cindexrange</em> -Parameter ist 0 (null).</p></li>
<li><p>Der <em>cindexrange</em> -Parameter ist größer als 64.</p></li>
<li><p>Das <strong>cbStruct</strong> -Element für jedes Element im Array, das durch den <em>rgindexrange</em> -Parameter angegeben wird, entspricht nicht der Größe der <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> Struktur.</p></li>
<li><p>Die Elemente im <em>rgindexrange</em> -Array enthalten <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s aus unterschiedlichen Tabellen.</p></li>
<li><p>Ein Element im <em>rgindexrange</em> -Array enthält eine <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> , die nicht auf einem sekundären Index positioniert ist.</p></li>
<li><p>Mindestens eines der Elemente im <em>rgindexrange</em> -Array enthält <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>en, die sich auf demselben sekundären Index befinden.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</p>
<p>Dieser Fehler wird unter allen Umständen nicht zurückgegeben. Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen konnte. Cursor Ressourcen werden durch Aufrufen von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <em>JET_paramMaxCursors</em> im <em>paramID</em> -Parameter festgelegt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</p>
<p><strong>Jetintersectindexes</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Host Prozesses zu fragmentiert wird. Der temporäre Tabellen-Manager weist immer einen 1-MB-Adressraum für jede temporäre Tabelle zu, die unabhängig von der zu speichernden Datenmenge erstellt wird. <strong>Jetintersectindexes</strong> erstellt eine temporäre Tabelle für jede <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> , die im <em>rgindexrange</em> -Parameter angegeben ist, und eine temporäre Tabelle für die Ausgabe in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Es ist nicht zulässig, dieselbe Sitzung von mehr als einem Thread gleichzeitig zu verwenden.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern der Indizes der Tabelle erforderlichen Ressourcen nicht zuordnen konnte. Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <em>JET_paramMaxOpenTables</em> im <em>paramID</em> -Parameter festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern des Schemas der Tabelle erforderlichen Ressourcen nicht zuordnen konnte. Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <em>JET_paramMaxOpenTables</em> im <em>paramID</em> -Parameter festgelegt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine die zum Erstellen einer temporären Tabelle erforderlichen Ressourcen nicht zuordnen konnte. Temporäre Tabellen Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit JET_paramMaxTemporaryTables konfiguriert, die im <em>paramID</em> -Parameter angegeben sind.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird eine neue temporäre Tabelle zurückgegeben, die die Lesezeichen der Datensätze enthält, die mit den Kriterien übereinstimmen, die durch die einzelnen Beschreibungen der Eingabe Index Bereiche dargestellt werden.

Bei einem Fehler wird die temporäre Tabelle, die die Ergebnisse enthält, nicht erstellt. Der Status der temporären Datenbank kann geändert werden. Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert. Die aktuelle Position der [JET_TABLEID](./jet-tableid.md)s, die für diese Funktion bereitgestellt wird, kann geändert werden.

#### <a name="remarks"></a>Bemerkungen

**Jetintersectindexes** kann verwendet werden, um die Datensätze in einer Tabelle anhand mehrerer Kriterien effizient zu filtern, wenn diese Kriterien in Bezug auf die sekundären Indizes für diese Tabelle ausgedrückt werden können. Nehmen Sie beispielsweise an, dass Sie über eine sehr große Tabelle mit Personen verfügen. Die Tabelle kann Spalten für Ihre Benutzer-ID, den Vornamen, den Nachnamen usw. aufweisen. Angenommen, jede dieser Spalten wird separat indiziert, und der primäre Index der Tabelle ist über die Benutzer-ID. Wenn Sie alle Benutzer suchen möchten, deren Vorname mit einem beginnt und dessen Nachname mit G beginnt, führen Sie die folgenden Schritte aus:

1.  Öffnen Sie einen neuen Cursor in der Tabelle, und legen Sie für diesen Cursor fest, dass der Index für die Spalte "Vorname" verwendet wird. Richten Sie dann einen Index Bereich für alle Personen ein, deren "Vorname" mit "A" beginnt, und erstellen Sie eine [JET_IndexRange](./jet-indexrange-structure.md) Struktur, die diesen Cursor enthält.

2.  Wiederholen Sie Schritt 1 mit einem neuen Cursor für den Index "Last Name" für alle Personen, deren "Nachname" mit "G" begonnen hat.

3.  Übergeben Sie diese Kriterien an **jetintersectindexes** , um das Ergebnis in einer temporären Tabelle zu berechnen.

4.  Durchlaufen Sie die temporäre Tabelle, und rufen Sie jeden Datensatz ab, der die Kriterien nach Lesezeichen übergibt.

Die temporäre Tabelle, die das Resultset enthält, ist eine einfache Tabelle mit einer Spalte, die das Lesezeichen der einzelnen Datensätze enthält, die alle zum Berechnen der Schnittmenge verwendeten Kriterien überschritten haben. Das Resultset wird in derselben Reihenfolge wie der primäre Index sortiert und enthält keine doppelten Einträge. Die Anwendung kann die Ergebnisse der Schnittmenge auflisten, indem Sie die Zeilen in der temporären Tabelle aufzählt, das Lesezeichen für jedes Ergebnis mithilfe von [jetretrievecolumn](./jetretrievecolumn-function.md)abrufen und dann den Datensatz in der Datenbank aufrufen, indem Sie [jetgotobookmark](./jetgotobookmark-function.md) mit diesem Lesezeichen auf einem Cursor aufrufen, der auf dem primären Index positioniert ist.

Die von **jetintersectindexes** zurückgegebene temporäre Tabelle kann nur in Vorwärtsrichtung gescannt werden. Er sollte auch über [jetclosetable](./jetclosetable-function.md) geschlossen werden, wenn die Überprüfung abgeschlossen ist. Weitere Informationen zu temporären Tabellen und ihrer Funktionsweise finden Sie unter [jetopertemporarytable](./jetopentemporarytable-function.md).

**Jetintersectindexes** ist im Allgemeinen eine effiziente und bequeme Möglichkeit zum Filtern von Datensätzen basierend auf mehreren indizierten Kriterien. Es gibt jedoch einige wichtige Tipps, die befolgt werden sollten, um die Nützlichkeit dieses Features zu maximieren. Wenn Sie wissen, dass eines der Kriterien so restriktiv ist, dass der resultierende Index Bereich nur sehr wenige Datensätze enthält, ist es wahrscheinlich besser, diesen Index Bereich zu durchlaufen und die Datensätze auf Anwendungsebene zu filtern. Wenn Sie darüber hinaus wissen, dass Sie Kriterien haben, die weitaus weniger restriktiv sind als andere Kriterien in ihrer Schnittmenge, sollten Sie in Erwägung ziehen, diese weitaus weniger restriktiven Kriterien aus der Schnittmenge zu verwerfen. Wenn Sie wissen, dass eines der Kriterien überhaupt nicht restriktiv ist, sodass der resultierende Index Bereich fast so groß wie der primäre Index ist, ist es unwahrscheinlich, dass die überschneidende Verwendung dieses Index Bereichs den Wert für das Resultset (reduzieren der Größe) beeinträchtigt. In allen Fällen sollten Sie Kriterien auf eine Weise auswählen, die möglichst wenige Indexeinträge für die Eingabe verwendet und den spezifischsten Satz an Lesezeichen bei der Ausgabe generiert, um die maximale Leistung zu erzielen.

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
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[Jetgojebookmark](./jetgotobookmark-function.md)  
[Jetretrievecolumschlag](./jetretrievecolumn-function.md)  
[Jetsetindexrange](./jetsetindexrange-function.md)
