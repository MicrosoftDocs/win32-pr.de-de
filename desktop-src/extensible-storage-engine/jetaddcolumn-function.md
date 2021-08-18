---
description: 'Weitere Informationen zu: JetAddColumn-Funktion'
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
ms.openlocfilehash: 2c1c70ab6510d2e63cc1b59e94ae058565937e854968b7ba05e2710ba22aa6af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979050"
---
# <a name="jetaddcolumn-function"></a>JetAddColumn-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetaddcolumn-function"></a>JetAddColumn-Funktion

Die **JetAddColumn-Funktion** fügt einer vorhandenen Tabelle in einer ESE-Datenbank eine neue Spalte hinzu.

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

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, der die Spalte hinzugefügt werden soll.

*szColumnName*

Der Name der hinzuzufügende Spalte. Der Name muss die folgenden Kriterien erfüllen:

  - Er muss weniger als JET_cbNameMost Zeichen lang sein, ohne dass der abschließende **NULL-Wert** enthalten ist.

  - Sie darf nur Zeichen aus den folgenden Sätzen enthalten: 0 bis 9, A bis Z, a bis z und alle anderen Interpunktionszeichen mit Ausnahme von Ausrufezeichen ( \! ), Komma (,), öffnende Klammer ( \[ ) und schließende Klammer ( ), d. h. \] ASCII-Zeichen 0x20, 0x22 durch 0x2d, 0x2f durch 0x5a, 0x5c und 0x5d über 0x7f.

  - Sie kann nicht mit einem Leerzeichen beginnen.

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

*pcolumndef*

Ein Zeiger auf eine [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur, die die Daten definiert, die in einer Spalte gespeichert werden können.

*pvDefault*

Ein Zeiger auf einen Puffer, der den Standardwert für die Spalte enthält. Die Länge des Puffers ist **cbDefault.** Wenn kein Standardwert vorhanden ist, legen Sie **pvDefault** auf **NULL** und **cbDefault** auf 0 (null) fest. Standardwerte dürfen nicht größer als JET_cbColumnMost Bytes für feste Spalten oder JET_cbLVDefaultValueMost Bytes für lange Werte sein. Wenn ein Standardwert größer ist, wird er automatisch abgeschnitten.

Wenn *grbit* JET_bitColumnUserDefinedDefault festgelegt ist, wird **pvDefault** als Zeiger auf eine [JET_USERDEFINEDDEFAULT-Struktur](./jet-userdefineddefault-structure.md) interpretiert.

*cbDefault*

Die Größe des Puffers in Bytes, der in **pvDefault** angegeben ist.

*pcolumnid*

Ein Zeiger auf eine [JET_COLUMNID](./jet-columnid.md) Struktur, die bei Erfolg den Bezeichner der neu erstellten Spalte empfängt. Bei einem Fehler ist der Wert nicht definiert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Es wurde versucht, die Datendefinition einer festen DDL-Tabelle zu ändern. Ein Beispiel für eine Tabelle mit fester DDL ist eine Vorlagentabelle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde an die API übergeben. Beispiele für ungültige Parameter sind:</p>
<ul>
<li><p>Übergeben der falschen Größe der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF-Struktur</a> in ihrem <em>cbStruct-Member.</em></p></li>
<li><p>Übergeben sie JET_bitColumnUserDefinedDefault, legen Sie <strong>cbDefault</strong> jedoch nicht auf sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>) fest.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Es wurde versucht, eine Spalte mit dem JET_bitColumnUnversioned Bit hinzuzufügen, aber die Sitzung befindet sich derzeit in einer Transaktion.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Eine Spalte ist bereits vorhanden. Es wurde versucht, eine Spalte ohne Versionsinformationen hinzuzufügen, und diese Spalte ist bereits vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableNotEmpty</p></td>
<td><p>Die Tabelle enthält Daten. Eine Spalte "Escrow Update" kann nur einer leeren Tabelle hinzugefügt werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Der Datensatz ist zu groß. Die Summe des <strong>cbMax-Parameters</strong> für die festen Spalten darf einen bestimmten Wert nicht überschreiten.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle darf nicht mehr als JET_ccolFixedMost festen Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierten Spalten enthalten.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Es wurde versucht, eine redundante Spalte hinzuzufügen. Es sollte nicht mehr als eine Spalte für die automatische Inkrementierung und nicht mehr als eine Versionsspalte pro Tabelle vorhanden sein.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>Die Rückruffunktion konnte nicht aufgelöst werden. Die DLL wurde möglicherweise nicht gefunden, oder die Funktion in der DLL wurde möglicherweise nicht gefunden. Das Ereignisprotokoll enthält weitere Details, wenn eine ausreichende Protokollierung aktiviert ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Eine Warnung, die angibt, dass die maximale Länge<strong>(cbMax)</strong>einer festen oder variablen Spalte größer als JET_cbColumnMost war. Dieser Grenzwert gilt nicht für Long-Werte (d. <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> und <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Ein ungültiger Name wurde als <strong>szColumnName</strong>übergeben. Weitere Informationen zu den Einschränkungen finden Sie in den Kriterien für <strong>szColumnName</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Das <strong>Coltypfeld</strong> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Der <strong>cp-Parameter</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF-Struktur</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaggedNotNULL</p></td>
<td><p>JET_bitColumnNotNULL können nicht mit markierten Spalten, langen Werten oder SLV-Spalten verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Es wurde eine ungültige Kombination von <em>Grbits</em> angegeben. Einige der Gründe für diesen Fehler sind:</p>
<ul>
<li><p>JET_bitColumnFixed wurde für eine markierte Spalte, einen langen Wert oder eine SLV-Spalte verwendet.</p></li>
<li><p>JET_bitColumnEscrowUpdate wurde für eine Spalte verwendet, die nicht vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>war.</p></li>
<li><p>JET_bitColumnEscrowUpdate wurde in einer Spalte Version (JET_bitColumnVersion) verwendet.</p></li>
<li><p>JET_bitColumnEscrowUpdate wurde für eine AutoIncrememnt-Spalte (JET_bitColumnAutoincrement) verwendet.</p></li>
<li><p>JET_bitColumnEscrowUpdate wurde für eine Spalte ohne Standardwert verwendet (<strong>cbDefault</strong> war gleich null).</p></li>
<li><p>JET_bitColumnFinalize wurde für eine Spalte verwendet, bei der es sich nicht um eine Spalte für die Escrow Update-Spalte handelte (JET_bitColumnEscrowUpdate wurde nicht festgelegt).</p></li>
<li><p>JET_bitColumnDeleteOnZero wurde für eine Spalte verwendet, bei der es sich nicht um eine Escrow Update-Spalte handelte (JET_bitColumnEscrowUpdate wurde nicht festgelegt).</p></li>
<li><p>JET_bitColumnAutoincrement wurde für eine Spalte verwendet, die nicht <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>war.</p>
<p><strong>Windows 2000:</strong> Dieser Fehlercode wird nur in Windows 2000 verwendet.</p>
<p>JET_bitColumnAutoincrement wurde für eine Spalte verwendet, die weder <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> noch <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>war.</p>
<p><strong>Windows XP:</strong> Dieser Grund für den Fehlercode wird in Windows XP- und späteren Betriebssystemen verwendet.</p></li>
<li><p>JET_bitColumnVersion wurde für eine Spalte verwendet, die nicht <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>wurde.</p></li>
<li><p>JET_bitColumnVersion wurde für eine Spalte für die automatische Inkrementierung verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnFixed verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnNotNULL verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnVersion verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnAutoincrement verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnUpdatable verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnEscrowUpdate verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnFinalize verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnDeleteOnZero verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnMaybeNull verwendet.</p></li>
<li><p>JET_bitColumnUserDefinedDefault wurde für eine nicht markierte Spalte verwendet (die fest oder variabel ist).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged</p></td>
<td><p>Eine mehrwertige Spalte (JET_bitColumnMultiValued) kann nur für eine markierte oder lange Wertspalte<a href="gg269213(v=exchg.10).md">(JET_coltypLongBinary</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongText)</a>verwendet werden.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged</p></td>
<td><p>Es wurde versucht, eine markierte Spalte zu verwenden, wenn die Spalte möglicherweise nicht markiert ist. Folgende Einschränkungen gelten für das Nichtermöglichen von markierten Spalten:</p>
<ul>
<li><p>Eine Escrow Update-Spalte (JET_bitColumnEscrowUpdate) kann nicht für eine markierte spalte oder long value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) verwendet werden.</p></li>
<li><p>Eine Spalte für die automatische Inkrementierung wird möglicherweise nicht markiert.</p></li>
<li><p>Eine Spalte Version ist möglicherweise nicht gekennzeichnet.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired</p></td>
<td><p>Für diesen Vorgang war eine exklusive Sperre für die Tabelle erforderlich.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Eine Warnung, die angibt, dass die maximale Länge<em>(cbMax)</em>einer festen oder variablen Spalte größer als JET_cbColumnMost war. Dieser Grenzwert gilt nicht für Long-Werte (d. <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> und <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
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
<td><p>Implementiert als <strong>JetAddColumnW</strong> (Unicode) und <strong>JetAddColumnA</strong> (ANSI).</p></td>
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
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
