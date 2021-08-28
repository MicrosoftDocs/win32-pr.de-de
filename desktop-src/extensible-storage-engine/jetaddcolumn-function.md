---
description: Weitere Informationen finden Sie unter JetAddColumn-Funktion.
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
ms.openlocfilehash: a1f59d4bb49145dd897994bebb776249a55e14d8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466377"
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

Der Name der hinzuzufügenden Spalte. Der Name muss die folgenden Kriterien erfüllen:

  - Es muss weniger als JET_cbNameMost Zeichen lang sein, ohne den beendenden **NULL-Wert.**

  - Sie darf nur Zeichen aus den folgenden Sätzen enthalten: 0 bis 9, A bis Z, a bis z und alle anderen Interpunktionen mit Ausnahme von Ausrufezeichen ( ), Komma (,), öffnenden Klammern () und schließenden Klammern ( ) – d. h. ASCII-Zeichen 0x20, 0x22 bis \! \[ \] 0x2d, 0x2f bis 0x5a, 0x5c und 0x5d bis 0x7f.

  - Er kann nicht mit einem Leerzeichen beginnen.

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

*pcolumndef*

Ein Zeiger auf [eine](./jet-columndef-structure.md) JET_COLUMNDEF Struktur, die die Daten definiert, die in einer Spalte gespeichert werden können.

*pvDefault*

Ein Zeiger auf einen Puffer, der den Standardwert für die Spalte enthält. Die Länge des Puffers ist **cbDefault.** Wenn es keinen Standardwert gibt, legen Sie **pvDefault** auf **NULL** und **cbDefault auf** 0 (null) fest. Standardwerte dürfen nicht größer als JET_cbColumnMost für feste Spalten oder JET_cbLVDefaultValueMost für long-Werte sein. Wenn ein Standardwert größer als dieser ist, wird er automatisch abgeschnitten.

Wenn *grbit* JET_bitColumnUserDefinedDefault festgelegt ist, **wird pvDefault** als Zeiger auf eine [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) interpretiert.

*cbDefault*

Die Größe des Puffers in Bytes, der in **pvDefault angegeben ist.**

*pcolumnid*

Ein Zeiger auf [eine](./jet-columnid.md) JET_COLUMNID struktur, die bei Erfolg den Bezeichner der neu erstellten Spalte erhält. Bei einem Fehler ist der Wert nicht definiert.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde durchgeführt.</p> | 
| <p>JET_errFixedDDL</p> | <p>Es wurde versucht, die Datendefinition einer festen DDL-Tabelle zu ändern. Ein Beispiel für eine Tabelle mit fester DDL ist eine Vorlagentabelle.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde an die API übergeben. Beispiele für ungültige Parameter sind:</p><ul><li><p>Übergeben der falschen Größe der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> struktur in ihrem <em>cbStruct-Member.</em></p></li><li><p>Übergeben von JET_bitColumnUserDefinedDefault, aber nicht festlegen <strong>von cbDefault</strong> auf sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li></ul> | 
| <p>JET_errInTransaction</p> | <p>Es wurde versucht, eine Spalte mit dem festgelegten JET_bitColumnUnversioned hinzuzufügen, aber die Sitzung befindet sich derzeit in einer Transaktion.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Eine Spalte ist bereits vorhanden. Es wurde versucht, eine Spalte ohne Versionsinformationen hinzuzufügen, und diese Spalte ist bereits vorhanden.</p> | 
| <p>JET_errTableNotEmpty</p> | <p>Die Tabelle enthält Daten. Eine Escrow Update-Spalte kann nur einer leeren Tabelle hinzugefügt werden.</p> | 
| <p>JET_errRecordTooBig</p> | <p>Der Datensatz ist zu groß. Die Summe des <strong>cbMax-Parameters</strong> für die festen Spalten darf einen bestimmten Wert nicht überschreiten.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen. Eine Tabelle kann nicht mehr als JET_ccolFixedMost Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost spalten enthalten.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Es wurde versucht, eine redundante Spalte hinzuzufügen. Es sollte nicht mehr als eine Spalte für die automatische Inkrementierung und nicht mehr als eine Versionsspalte pro Tabelle geben.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Die Rückruffunktion konnte nicht aufgelöst werden. Die DLL wurde möglicherweise nicht gefunden, oder die Funktion in der DLL wurde möglicherweise nicht gefunden. Das Ereignisprotokoll enthält weitere Details, wenn eine ausreichende Protokollierung aktiviert ist.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Eine Warnung, die angibt, dass die maximale Länge (<strong>cbMax</strong>) einer festen oder variablen Spalte größer als JET_cbColumnMost. Dieser Grenzwert gilt nicht für lange Werte <a href="gg269213(v=exchg.10).md">(d.</a> h. JET_coltypLongBinary und <a href="gg269213(v=exchg.10).md">JET_coltypLongText).</a></p> | 
| <p>JET_errInvalidName</p> | <p>Ein ungültiger Name wurde als <strong>szColumnName übergeben.</strong> Weitere Informationen zu den Einschränkungen finden Sie in den Kriterien <strong>für szColumnName</strong>.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Das <strong>Coltyp-Feld</strong> wurde nicht auf einen gültigen Spaltentyp festgelegt.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Der <strong>cp-Parameter</strong> der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf eine gültige Codepage festgelegt. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</p> | 
| <p>JET_errTaggedNotNULL</p> | <p>JET_bitColumnNotNULL kann nicht mit markierten Spalten, Long Value- oder SLV-Spalten verwendet werden.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Es wurde eine ungültige <em>Kombination von Grbits</em> angegeben. Einige der Gründe für diesen Fehler sind:</p><ul><li><p>JET_bitColumnFixed wurde für eine markierte Spalte, einen long-Wert oder eine SLV-Spalte verwendet.</p></li><li><p>JET_bitColumnEscrowUpdate wurde für eine Spalte verwendet, die nicht vom <a href="gg269213(v=exchg.10).md">Typ</a>JET_coltypLong.</p></li><li><p>JET_bitColumnEscrowUpdate wurde für eine Version-Spalte (JET_bitColumnVersion).</p></li><li><p>JET_bitColumnEscrowUpdate wurde für eine AutoIncrememnt-Spalte (JET_bitColumnAutoincrement).</p></li><li><p>JET_bitColumnEscrowUpdate wurde für eine Spalte ohne Standardwert verwendet (<strong>cbDefault</strong> war gleich null).</p></li><li><p>JET_bitColumnFinalize wurde für eine Spalte verwendet, die keine Escrow Update-Spalte war (JET_bitColumnEscrowUpdate wurde nicht festgelegt).</p></li><li><p>JET_bitColumnDeleteOnZero wurde für eine Spalte verwendet, die keine Escrow Update-Spalte war (JET_bitColumnEscrowUpdate wurde nicht festgelegt).</p></li><li><p>JET_bitColumnAutoincrement wurde für eine Spalte verwendet, die <a href="gg269213(v=exchg.10).md">nicht</a>JET_coltypLong.</p><p><strong>Windows 2000:</strong> Dieser Grund für den Fehlercode wird nur in Windows 2000 verwendet.</p><p>JET_bitColumnAutoincrement wurde für eine Spalte verwendet, die <a href="gg269213(v=exchg.10).md">weder</a> JET_coltypLong <a href="gg269213(v=exchg.10).md">noch</a>JET_coltypCurrency.</p><p><strong>Windows XP:</strong> Dieser Grund für den Fehlercode wird in betriebssystemen Windows XP und höher verwendet.</p></li><li><p>JET_bitColumnVersion wurde für eine Spalte verwendet, die <a href="gg269213(v=exchg.10).md">nicht</a>JET_coltypLong.</p></li><li><p>JET_bitColumnVersion wurde für eine Spalte mit automatischer Inkrementierung verwendet.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnFixed.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnNotNULL.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnVersion.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnAutoincrement.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnUpdatable.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnEscrowUpdate.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnFinalize.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnDeleteOnZero.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde in Verbindung mit JET_bitColumnMaybeNull.</p></li><li><p>JET_bitColumnUserDefinedDefault wurde für eine nicht markierte Spalte (die fest oder variable ist) verwendet.</p></li></ul> | 
| <p>JET_errMultiValuedColumnMustBeTagged</p> | <p>Eine mehrwertige Spalte (JET_bitColumnMultiValued) kann nur für eine markierte Spalte oder eine Long Value-Spalte (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> <a href="gg269213(v=exchg.10).md">oder JET_coltypLongText</a>) verwendet werden.</p> | 
| <p>JET_errCannotBeTagged</p> | <p>Es wurde versucht, eine markierte Spalte zu verwenden, wenn die Spalte möglicherweise nicht markiert wurde. Zu den Einschränkungen für das Nichtergieren von markierten Spalten gehören:</p><ul><li><p>Eine Escrow Update-Spalte (JET_bitColumnEscrowUpdate) kann nicht für eine markierte Spalte oder eine Long Value-Spalte (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> <a href="gg269213(v=exchg.10).md">oder JET_coltypLongText</a>) verwendet werden.</p></li><li><p>Eine Spalte für die automatische Inkrementierung wurde möglicherweise nicht markiert.</p></li><li><p>Eine Version -Spalte wurde möglicherweise nicht markiert.</p></li></ul> | 
| <p>JET_errExclusiveTableLockRequired</p> | <p>Für diesen Vorgang war eine exklusive Sperre für die Tabelle erforderlich.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Eine Warnung, die angibt, dass die maximale Länge (<em>cbMax</em>) einer festen oder variablen Spalte größer als JET_cbColumnMost. Dieser Grenzwert gilt nicht für lange Werte (d. h. <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> <a href="gg269213(v=exchg.10).md">und JET_coltypLongText).</a></p> | 



#### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JetAddColumnW</strong> (Unicode) und <strong>JetAddColumnA</strong> (ANSI) implementiert.</p> | 



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
