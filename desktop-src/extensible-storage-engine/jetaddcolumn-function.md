---
description: 'Weitere Informationen zu: jetaddcolumn-Funktion'
title: JetAddColumn-Funktion
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368962"
---
# <a name="jetaddcolumn-function"></a>JetAddColumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetaddcolumn-function"></a>JetAddColumn-Funktion

Die **jetaddcolumn** -Funktion fügt einer vorhandenen Tabelle in einer ESE-Datenbank eine neue Spalte hinzu.

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>Parameter

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Die Tabelle, der die Spalte hinzugefügt werden soll.

*szcolumnname*

Der Name der hinzu zufügenden Spalte. Der Name muss die folgenden Kriterien erfüllen:

  - Es muss weniger als JET_cbNameMost Zeichen lang sein, ohne das abschließende **null**-Zeichen.

  - Sie darf nur Zeichen aus den folgenden Sätzen enthalten: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Zeichen außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer ( \] ) – das heißt, die ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

*pcolumndef*

Ein Zeiger auf eine [JET_COLUMNDEF](./jet-columndef-structure.md) -Struktur, die die Daten definiert, die in einer Spalte gespeichert werden können.

*pvdefault*

Ein Zeiger auf einen Puffer, der den Standardwert für die Spalte enthält. Die Länge des Puffers ist **cbdefault**. Wenn kein Standardwert vorhanden ist, legen Sie **pvdefault** auf **null** und **cbdefault** auf NULL fest. Standardwerte dürfen nicht größer als JET_cbColumnMost Bytes für Fixed-Spalten oder JET_cbLVDefaultValueMost Bytes für Long-Werte sein. Wenn ein Standardwert größer als dieser Wert ist, wird er automatisch abgeschnitten.

Wenn *grbit* JET_bitColumnUserDefinedDefault festgelegt ist, wird **pvdefault** als Zeiger auf eine [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) Struktur interpretiert.

*cbdefault*

Die Größe (in Bytes) des Puffers, der in **pvdefault** angegeben wird.

*pColumnID*

Ein Zeiger auf eine [JET_COLUMNID](./jet-columnid.md) -Struktur, die bei Erfolg den Bezeichner der neu erstellten Spalte empfängt. Bei einem Fehler ist der Wert nicht definiert.

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
<td><p>Der Vorgang wurde durchgeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL</p></td>
<td><p>Es wurde versucht, die Datendefinition einer fixierten DDL-Tabelle zu ändern. Ein Beispiel für eine Tabelle mit fester DDL ist eine Vorlagen Tabelle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde an die API übergeben. Einige Beispiele für ungültige Parameter sind:</p>
<ul>
<li><p>Übergeben der falschen Größe der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> -Struktur in Ihrem <em>cbStruct</em> -Member.</p></li>
<li><p>Das übergeben von JET_bitColumnUserDefinedDefault, aber nicht das Festlegen von <strong>cbdefault</strong> auf sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Es wurde versucht, eine Spalte mit dem JET_bitColumnUnversioned-Bit hinzuzufügen, aber die Sitzung befindet sich derzeit in einer Transaktion.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Eine Spalte ist bereits vorhanden. Es wurde versucht, eine Spalte ohne Versionsinformationen hinzuzufügen, und diese Spalte ist bereits vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableNotEmpty</p></td>
<td><p>Die Tabelle enthält Daten. Eine Spalte für das Hinterlegungs Update kann nur einer leeren Tabelle hinzugefügt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Der Datensatz ist zu groß. Die Summe des <strong>cbmax</strong> -Parameters für die Fixed-Spalten darf einen bestimmten Wert nicht überschreiten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Es wurde versucht, eine redundante Spalte hinzuzufügen. Es darf nicht mehr als eine AUTOINCREMENT-Spalte und höchstens eine Versions Spalte pro Tabelle vorhanden sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>Die Rückruffunktion konnte nicht aufgelöst werden. Die dll wurde möglicherweise nicht gefunden, oder die Funktion in der dll wurde nicht gefunden. Wenn eine ausreichende Protokollierung aktiviert ist, werden im Ereignisprotokoll weitere Details angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Eine Warnung, die angibt, dass die maximale Länge (<strong>cbmax</strong>) einer Fixed-oder Variable-Spalte größer als JET_cbColumnMost ist. Dieser Grenzwert gilt nicht für lange Werte ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> und <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Ein ungültiger Name wurde als <strong>szcolumnname</strong>-Element übermittelt. Weitere Informationen zu den Einschränkungen finden Sie unter den Kriterien für <strong>szcolumnname</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Das Feld <strong>colyp</strong> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Der <strong>CP</strong> -Parameter der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaggedNotNULL</p></td>
<td><p>JET_bitColumnNotNULL können nicht mit markierten, langen Wert-oder SLV-Spalten verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Es wurde eine ungültige Kombination von <em>grbits</em> angegeben. Mögliche Ursachen für diesen Fehler sind:</p>
<ul>
<li><p>JET_bitColumnFixed wurde für eine markierte, lange Wert-oder SLV-Spalte verwendet.</p></li>
<li><p>JET_bitColumnEscrowUpdate wurde für eine Spalte verwendet, die nicht vom Typ " <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>" war.</p></li>
<li><p>JET_bitColumnEscrowUpdate wurde für eine Versions Spalte (JET_bitColumnVersion) verwendet.</p></li>
<li><p>JET_bitColumnEscrowUpdate wurde in einer autoincrememnt-Spalte (JET_bitColumnAutoincrement) verwendet.</p></li>
<li><p>JET_bitColumnEscrowUpdate wurde für eine Spalte verwendet, die keinen Standardwert enthielt (<strong>cbdefault</strong> war gleich null).</p></li>
<li><p>JET_bitColumnFinalize wurde für eine Spalte verwendet, bei der es sich nicht um eine Spalte für eine hinterlegte Aktualisierung handelt (JET_bitColumnEscrowUpdate nicht festgelegt wurde).</p></li>
<li><p>JET_bitColumnDeleteOnZero wurde für eine Spalte verwendet, bei der es sich nicht um eine Spalte für eine hinterlegte Aktualisierung handelt (JET_bitColumnEscrowUpdate nicht festgelegt wurde).</p></li>
<li><p>JET_bitColumnAutoincrement wurde für eine Spalte verwendet, die nicht <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>wurde.</p>
<p><strong>Windows 2000:  </strong> Dieser Fehlercode wird nur in Windows 2000 verwendet.</p>
<p>JET_bitColumnAutoincrement wurde für eine Spalte verwendet, die weder <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> noch <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>war.</p>
<p><strong>Windows XP:  </strong> Dieser Fehlercode wird in Windows XP und neueren Betriebssystemen verwendet.</p></li>
<li><p>JET_bitColumnVersion wurde für eine Spalte verwendet, die nicht <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>wurde.</p></li>
<li><p>In einer autoincrement-Spalte wurde JET_bitColumnVersion verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnFixed verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnNotNULL verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnVersion verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnAutoincrement verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnUpdatable verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnEscrowUpdate verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnFinalize verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnDeleteOnZero verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnMaybeNull verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde für eine nicht markierte Spalte (fest oder Variable) verwendet.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged</p></td>
<td><p>Eine mehrwertige Spalte (JET_bitColumnMultiValued) kann nur für eine markierte oder lange Wert Spalte (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged</p></td>
<td><p>Es wurde versucht, eine markierte Spalte zu verwenden, wenn die Spalte möglicherweise nicht markiert ist. Folgende Einschränkungen gelten für das Zulassen von markierten Spalten:</p>
<ul>
<li><p>Eine Spalte für das Hinterlegungs Update (JET_bitColumnEscrowUpdate) kann nicht für eine markierte oder lange Wert Spalte (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) verwendet werden.</p></li>
<li><p>Eine AUTOINCREMENT-Spalte kann nicht markiert werden.</p></li>
<li><p>Eine Versions Spalte kann nicht markiert werden.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired</p></td>
<td><p>Für diesen Vorgang war eine exklusive Sperre für die Tabelle erforderlich.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Eine Warnung, die angibt, dass die maximale Länge (<em>cbmax</em>) einer Fixed-oder Variable-Spalte größer als JET_cbColumnMost ist. Dieser Grenzwert gilt nicht für lange Werte ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> und <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
</tbody>
</table>


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
<td><p>Implementiert als <strong>jetaddcolumnw</strong> (Unicode) und <strong>jetaddcolumna</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
