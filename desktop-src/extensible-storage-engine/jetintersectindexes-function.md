---
description: Weitere Informationen finden Sie unter JetIntersectIndexes-Funktion.
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
ms.openlocfilehash: 23d9d7bcd7d41251883313517db34f0cbca0ec8e6d2aaa5946348057cc29d844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978870"
---
# <a name="jetintersectindexes-function"></a>JetIntersectIndexes-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetintersectindexes-function"></a>JetIntersectIndexes-Funktion

Die **JetIntersectIndexes-Funktion** berechnet die Schnittmenge zwischen mehreren Sätzen von Indexeinträgen aus verschiedenen sekundären Indizes über dieselbe Tabelle. Dieser Vorgang ist nützlich, um den Satz von Datensätzen in einer Tabelle zu finden, die zwei oder mehr Kriterien erfüllen, die mithilfe von Indexbereichen ausgedrückt werden können.

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

*sesid*

Die Sitzung, die für diesen Aufruf verwendet werden soll.

*rgindexrange*

Ein Zeiger auf ein Array von [JET_IndexRange](./jet-indexrange-structure.md) Strukturen. Jede -Struktur enthält [JET_TABLEID,](./jet-tableid.md) die so eingerichtet wurde, dass sie einen der zu überschneidenden Indexbereiche enthält. Weitere Informationen finden Sie unter [JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

Die Anzahl der [JET_IndexRange](./jet-indexrange-structure.md) strukturen im Array, das im *rgindexrange-Parameter enthalten* ist.

*precordlist*

Zeiger auf eine [JET_RECORDLIST](./jet-recordlist-structure.md) Struktur. Diese Struktur wird mit genügend Informationen aufgefüllt, um die temporäre Tabelle mit den Ergebnissen von **JetIntersectIndexes zu durchlaufen.**

Der Ausgabepuffer, der eine [JET_RECORDLIST](./jet-recordlist-structure.md) empfängt. Die -Struktur enthält eine Beschreibung des Ergebnissets der Schnittmenge.

*grbit*

Für die zukünftige Verwendung reserviert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Es ist nicht möglich, den Vorgang abschließen, da alle Aktivitäten auf der -Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufs von <a href="gg269240(v=exchg.10).md">JetStopService beendet wurden.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da für die der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität dieser Daten zu schützen.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Eine der angeforderten Optionen war ungültig, wurde falsch verwendet oder nicht implementiert.</p>
<p>Dieser Fehler wird von <strong>JetIntersectIndexes zurückgegeben, wenn:</strong></p>
<p>Das <em>in der</em> -Struktur enthaltene <a href="gg269335(v=exchg.10).md">grbit JET_IndexRange,</a> auf das von einem Element im <em>rgindexrange-Array</em> verwiesen wird, ist nicht gleich JET_bitRecordInIndex.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthält einen unerwarteten Wert oder einen Wert, der inkonsistent ist, wenn er mit dem Wert eines anderen Parameters kombiniert wird.</p>
<p>Dieser Fehler wird aus den folgenden Gründen von <strong>JetIntersectIndexes</strong> zurückgegeben:</p>
<ul>
<li><p>Der <em>precordlist-Parameter</em> ist NULL.</p></li>
<li><p>Der <strong>cbStruct-Member</strong> der <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> im <em>precordlist-Parameter</em> angegebenen Struktur ist nicht gleich der Größe der JET_RECORDLIST <a href="gg269287(v=exchg.10).md">Struktur.</a></p></li>
<li><p>Der <em>cindexrange-Parameter</em> ist 0 (null).</p></li>
<li><p>Der <em>cindexrange-Parameter</em> ist größer als 64.</p></li>
<li><p>Der <strong>cbStruct-Member</strong> für jedes Element im Array, das durch den <em>rgindexrange-Parameter</em> angegeben wird, ist nicht gleich der Größe der JET_IndexRange <a href="gg269335(v=exchg.10).md">Struktur.</a></p></li>
<li><p>Die Elemente im <em>Array rgindexrange</em> <a href="gg269182(v=exchg.10).md">enthalten</a>JET_TABLEID aus verschiedenen Tabellen.</p></li>
<li><p>Ein Element im <em>Array rgindexrange</em> enthält <a href="gg269182(v=exchg.10).md">eine</a> JET_TABLEID, die nicht auf einem sekundären Index positioniert ist.</p></li>
<li><p>Mindestens eines der Elemente im <em>Array rgindexrange</em> enthält <a href="gg269182(v=exchg.10).md">JET_TABLEID,</a>die am gleichen sekundären Index positioniert sind.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Das Sitzungshandy ist ungültig oder verweist auf eine geschlossene Sitzung.</p>
<p>Dieser Fehler wird nicht unter allen Umständen zurückgegeben. Handles werden nur nach bestem Aufwand überprüft.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz nicht initialisiert wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, da die Engine nicht die Ressourcen zuordnen konnte, die zum Öffnen eines neuen Cursors erforderlich sind. Cursorressourcen werden durch Aufrufen von <a href="gg294044(v=exchg.10).md">JetSetSystemParameter konfiguriert,</a> <em>JET_paramMaxCursors</em> parameter <em>angegeben</em> sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Fehler beim Vorgang, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um ihn abschließen zu können.</p>
<p><strong>JetIntersectIndexes</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Hostprozesses zu fragmentiert wird. Der temporäre Tabellen-Manager ordnet für jede temporäre Tabelle, die erstellt wird, immer einen Adressraum von 1 MB zu, unabhängig von der zu speichernden Datenmenge. <strong>JetIntersectIndexes</strong> erstellt eine temporäre Tabelle für jede <a href="gg269335(v=exchg.10).md">JET_IndexRange,</a> die im <em>rgindexrange-Parameter</em> angegeben ist, und eine temporäre Tabelle für die Ausgabe in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da ein Wiederherstellungsvorgang für die -Instanz durchgeführt wird, die der Sitzung zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Es ist unzulässig, dieselbe Sitzung von mehr als einem Thread gleichzeitig zu verwenden.</p>
<p><strong>Windows XP:</strong>  Dieser Rückgabewert wird in xp Windows eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Der Vorgang kann nicht abgeschlossen werden, da die der Sitzung zugeordnete Instanz heruntergefahren wird.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil die Engine nicht die Ressourcen zuordnen konnte, die zum Zwischenspeichern der Indizes der Tabelle erforderlich sind. Die Anzahl der Indizes, deren Schema zwischengespeichert werden <em></em> kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter konfiguriert,</a> JET_paramMaxOpenTables parameter <em>angegeben</em> ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil die Engine nicht die Ressourcen zuordnen konnte, die zum Zwischenspeichern des Schemas der Tabelle erforderlich sind. Die Anzahl der Tabellen, deren Schema zwischengespeichert werden <em></em> kann, wird mit <a href="gg294044(v=exchg.10).md">JetSetSystemParameter konfiguriert,</a> JET_paramMaxOpenTables parameter <em>angegeben</em> ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts</p></td>
<td><p>Der Vorgang ist fehlgeschlagen, weil die Engine nicht die Ressourcen zuordnen konnte, die zum Erstellen einer temporären Tabelle erforderlich sind. Temporäre Tabellenressourcen werden <a href="gg294044(v=exchg.10).md">mitHilfe von JetSetSystemParameter konfiguriert,</a> JET_paramMaxTemporaryTables parameter <em>angegeben</em> werden.</p></td>
</tr>
</tbody>
</table>


Bei Erfolg wird eine neue temporäre Tabelle zurückgegeben, die die Lesezeichen der Datensätze enthält, die den Kriterien entsprechen, die von den einzelnen Beschreibungen des Eingabeindexbereichs dargestellt werden.

Bei einem Fehler wird die temporäre Tabelle, die die Ergebnisse enthält, nicht erstellt. Der Status der temporären Datenbank kann geändert werden. Der Status normaler Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert. Die aktuelle Position der [-JET_TABLEID,](./jet-tableid.md)die für diese Funktion bereitgestellt werden, kann geändert werden.

#### <a name="remarks"></a>Hinweise

**JetIntersectIndexes** kann verwendet werden, um die Datensätze in einer Tabelle effizient nach mehreren Kriterien zu filtern, wenn diese Kriterien als sekundäre Indizes für diese Tabelle ausgedrückt werden können. Stellen Sie sich beispielsweise vor, Dass Sie über eine sehr große Tabelle mit Personen verfügen. Die Tabelle kann Spalten für die Benutzer-ID, den Vornamen, den Nachnamen und so weiter enthalten. Angenommen, jede dieser Spalten wird separat indiziert, und der primäre Index der Tabelle befindet sich über der Benutzer-ID. Wenn Sie alle Personen suchen möchten, deren Vorname mit einem A beginnt und dessen Nachname mit G beginnt, führen Sie die folgenden Schritte aus:

1.  Öffnen Sie einen neuen Cursor für die Tabelle, und legen Sie fest, dass dieser Cursor den Index über die Spalte "Vorname" verwendet. Richten Sie [dann](./jet-indexrange-structure.md) einen Indexbereich für alle Personen ein, deren "Vorname" mit "A" begonnen hat, und erstellen Sie eine JET_IndexRange-Struktur, die diesen Cursor enthält.

2.  Wiederholen Sie Schritt 1 mit einem neuen Cursor auf dem Index "Nachname" für alle Personen, deren "Nachname" mit "G" begonnen hat.

3.  Übergeben Sie diese Kriterien **an JetIntersectIndexes,** um das Ergebnis in einer temporären Tabelle zu berechnen.

4.  Durchlaufen Sie die temporäre Tabelle, und rufen Sie alle Datensätze ab, die die Kriterien per Lesezeichen übergeben.

Die temporäre Tabelle, die das ResultSet enthält, ist eine einfache Tabelle mit einer Spalte, die das Lesezeichen jedes Datensatzes enthält, der alle Kriterien zum Berechnen der Schnittmenge erfüllt hat. Das ResultSet wird in der gleichen Reihenfolge wie der primäre Index sortiert und enthält keine doppelten Einträge. Die Anwendung kann die Ergebnisse der Schnittmenge aufzählen, indem sie die Zeilen in der temporären Tabelle aufzählt, das Lesezeichen für jedes Ergebnis mithilfe von [JetRetrivorColumn](./jetretrievecolumn-function.md)abruft und dann den Datensatz in der Datenbank durch Aufrufen [von JetGotoBookmark](./jetgotobookmark-function.md) mit diesem Lesezeichen auf einem Cursor aufruft, der auf dem primären Index positioniert ist.

Die von **JetIntersectIndexes zurückgegebene** temporäre Tabelle kann nur vorwärts gescannt werden. Sie sollte auch über [JetCloseTable geschlossen werden,](./jetclosetable-function.md) wenn die Überprüfung abgeschlossen wurde. Weitere Informationen zu temporären Tabellen und ihrer Funktionsweise finden Sie unter [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

**JetIntersectIndexes** ist im Allgemeinen eine effiziente und praktische Möglichkeit, Datensätze basierend auf mehreren indizierten Kriterien zu filtern. Es gibt jedoch einige wichtige Tipps, die befolgt werden sollten, um die Nützlichkeit dieses Features zu maximieren. Wenn Sie wissen, dass eines der Kriterien so restriktiv ist, dass der resultierende Indexbereich nur sehr wenige Datensätze enthält, ist es wahrscheinlich besser, einfach diesen Indexbereich zu durchgehen und die Datensätze auf Anwendungsebene zu filtern. Wenn Sie darüber hinaus wissen, dass Sie über Kriterien verfügen, die viel weniger restriktiv sind als andere Kriterien in Ihrer Schnittmenge, können Sie erwägen, diese wesentlich weniger restriktiven Kriterien aus der Schnittmenge zu löschen. Wenn Sie wissen, dass eines der Kriterien überhaupt nicht restriktiv ist, sodass der resultierende Indexbereich fast so groß wie der primäre Index ist, ist es unwahrscheinlich, dass die Schnittmenge mit diesem Indexbereich das Resultset profitiert (verkleinern). In allen Fällen sollten Sie Kriterien auf eine Weise auswählen, die möglichst wenige Indexeinträge bei der Eingabe aufnimmt und den spezifischsten Satz von Lesezeichen für die Ausgabe generiert, um maximale Leistung zu erzielen.

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
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
