---
description: 'Weitere Informationen zu: JET_TABLECREATE3-Struktur'
title: JET_TABLECREATE3-Struktur
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64f820b9e9a42099cdb99d8ab8f0756e8fdbb23256917821d05573afd9068017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979240"
---
# <a name="jet_tablecreate3-structure"></a>JET_TABLECREATE3-Struktur


_**Gilt für:** Windows | Windows Server_

Die **JET_TABLECREATE3-Struktur** enthält die Informationen, die zum Erstellen einer Tabelle erforderlich sind, die mit Spalten und Indizes in einer ESE-Datenbank (Extensible Storage Engine) aufgefüllt ist und eine Rückruffunktion bestimmt. Die **JET_TABLECREATE3-Struktur** wird von der [JetCreateTableColumnIndex3-Funktion](./jetcreatetablecolumnindex3-function.md) verwendet.

Die **JET_TABLECREATE3-Struktur** wurde im Betriebssystem Windows 7 eingeführt.

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a>Member

**cbStruct**

Die Größe dieser Struktur in Bytes (für zukünftige Erweiterungen). Sie muss auf sizeof( JET_TABLECREATE3 ) in Bytes festgelegt werden.

**szTableName**

Der Name der zu erstellenden Tabelle.

Der Name muss die folgenden Bedingungen erfüllen:

  - Er muss einen Wert aufweisen, der kleiner als JET_cbNameMost ist, ohne den abschließenden NULL-Wert zu enthalten.

  - Sie muss aus den folgenden Zeichen bestehen: 0 bis 9, A bis Z, a bis z und allen anderen Interpunktionszeichen mit Ausnahme von Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer ( ), d. h. \] ASCII-Zeichen 0x20, 0x22 durch 0x2d, 0x2f durch 0x5a, 0x5c und 0x5d durch 0x7f.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss aus mindestens einem Zeichen ohne Leerzeichen bestehen.

**szTemplateTableName**

Der Name einer vorhandenen Tabelle, von der die Basisdatendefinitionssprache (DDL) geerbt werden soll. Die Verwendung einer Vorlagentabelle ermöglicht die einfache Erstellung vieler Tabellen mit identischen Spalten und Indizes.

**ulPages**

Die anfängliche Anzahl der Datenbankseiten, die für die Tabelle zugeordnet werden sollen. Wenn Sie eine Zahl angeben, die größer als 1 ist, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.

**ulDensity**

Die Tabellendichte in Prozent. Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 liegen. Die Übergabe von 0 bedeutet, dass der Standardwert verwendet werden soll. Der Standardwert ist 80.

**rgcolumncreate**

Ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, von denen jede einer Spalte entspricht, die in der neuen Tabelle erstellt werden soll.

**cColumns**

Die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) Elemente im *rgcolumncreate-Parameter.*

**rgindexcreate**

Ein Array von [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Strukturen, von denen jede einem Index entspricht, der in der neuen Tabelle erstellt werden soll.

**cIndexes**

Die Anzahl der [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Elemente im *rgindexcreate-Parameter.*

**szCallback**

Die Funktion, die während bestimmter Ereignisse aufgerufen wird. **cbtyp** bestimmt, wann die Rückruffunktion aufgerufen wird.

Das Format von **szCallback** muss \! "Modulfunktion" sein, z.B. bezieht sich "alpha \! beta" auf die Betafunktion im Modul mit dem Namen "alpha".

Der Prototyp der Funktion muss mit der [JET_CALLBACK](./jet-callback-callback-function.md) Rückruffunktion übereinstimmen.

**cbtyp**

Beschreibt den Typ der rückruffunktion, die von **szCallback** festgelegt wird. Weitere Informationen finden Sie unter [JET_CBTYP](./jet-cbtyp.md).

Dieses Bitfeld besteht aus mindestens einem der in der folgenden Tabelle aufgeführten Bitwerte.

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
<td><p>JET_cbtypFinalize</p></td>
<td><p>Die Rückruffunktion wird aufgerufen, wenn eine Spalte, die finalisiert werden kann, 0 (null) erreicht hat.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeInsert</p></td>
<td><p>Die Rückruffunktion wird vor dem Einfügen des Datensatzes aufgerufen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterInsert</p></td>
<td><p>Die Rückruffunktion wird aufgerufen, nachdem die Datenbank-Engine das Einfügen eines Datensatzes abgeschlossen hat.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeReplace</p></td>
<td><p>Die Rückruffunktion wird vor der Änderung eines Datensatzes aufgerufen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterReplace</p></td>
<td><p>Die Rückruffunktion wird aufgerufen, nachdem die Änderung eines Datensatzes abgeschlossen wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeDelete</p></td>
<td><p>Die Rückruffunktion wird vor dem Löschen eines Datensatzes aufgerufen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterDelete</p></td>
<td><p>Die Rückruffunktion wird aufgerufen, nachdem ein Datensatz gelöscht wurde.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypUserDefinedDefaultValue</p></td>
<td><p>Die Rückruffunktion wird aufgerufen, um einen benutzerdefinierten Standardwert zu berechnen.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS</p></td>
<td><p>Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einem Cursor zugeordnet ist, freigegeben werden muss.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS</p></td>
<td><p>Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einer Tabelle zugeordnet ist, freigegeben werden muss.</p></td>
</tr>
</tbody>
</table>


**grbit**

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Aufrufoptionswerte enthält.

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
<td><p>JET_bitTableCreateFixedDDL</p></td>
<td><p>Verhindert DDL-Vorgänge für die Tabelle (z. B. das Hinzufügen oder Entfernen von Spalten).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Bewirkt, dass die Tabelle eine Vorlagentabelle ist. Neue Tabellen können dann den Namen dieser Tabelle als Vorlagentabelle angeben. Das Festlegen JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Muss in Verbindung mit JET_bitTableCreateTemplateTable verwendet werden. Veraltet. Nicht verwenden.</p></td>
</tr>
</tbody>
</table>


**pSeqSpacehints**

Ein Zeiger auf eine [JET_SPACEHINTS-Struktur](./jet-spacehints-structure.md) für den sequenziellen Standardindex.

**pSeqSpacehints** wurde in Windows 7 eingeführt.

**pLVSpacehints**

Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) Struktur für eine Struktur mit getrennten langen Werten.

**pLVSpacehints** wurde in Windows 7 eingeführt.

**cbSeparateLV**

Die Größe, die ein systeminternes LV vom primären Datensatz trennen soll. Eine beliebige c-Struktur mit einem langen Wert für eine separate LV-Struktur. Weitere Informationen finden Sie unter ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md). Spalten mit langen Werten, die kleiner als dieser Wert sind, können getrennt werden, wenn der Datensatz zu groß wird.

**cbSeparateLV** wurde in Windows 7 eingeführt.

**tableid**

Ein Ausgabefeld, das die [JET_TABLEID](./jet-tableid.md) der neuen Tabelle enthält, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert. Diese Tabelle wird ausschließlich geöffnet.

**cCreated**

Ein Ausgabefeld, das die Anzahl der Objekte enthält, die erstellt werden, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert.

Die Anzahl der erstellten Objekte entspricht der Summe der Erfolgreich erstellten Spalten, Tabellen und Indizes.

### <a name="requirements"></a>Anforderungen

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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_TABLECREATE3_W</strong> (Unicode) und JET_TABLECREATE3_A (ANSI) implementiert. <strong></strong></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
