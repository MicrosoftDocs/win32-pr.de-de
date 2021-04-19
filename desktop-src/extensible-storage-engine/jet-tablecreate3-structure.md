---
description: 'Weitere Informationen finden Sie hier: JET_TABLECREATE3 Struktur'
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
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353013"
---
# <a name="jet_tablecreate3-structure"></a>JET_TABLECREATE3-Struktur


_**Gilt für:** Windows | Windows Server_

Die **JET_TABLECREATE3** Struktur enthält die Informationen, die erforderlich sind, um eine Tabelle zu erstellen, die mit Spalten und Indizes in einer ESE-Datenbank (Extensible Storage Engine) gefüllt ist und die eine Rückruffunktion festlegt. Die **JET_TABLECREATE3** -Struktur wird von der [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) -Funktion verwendet.

Die **JET_TABLECREATE3** Struktur wurde mit dem Betriebssystem Windows 7 eingeführt.

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

Die Größe dieser-Struktur in Bytes (für zukünftige Erweiterungen). Er muss auf sizeof (JET_TABLECREATE3) in Bytes festgelegt werden.

**sztablename**

Der Name der zu erstellenden Tabelle.

Der Name muss die folgenden Bedingungen erfüllen:

  - Er muss einen Wert aufweisen, der kleiner als JET_cbNameMost ist, ohne den abschließenden NULL-Wert.

  - Sie muss aus folgenden Zeichen bestehen: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Punkte außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer (), d. h \] . ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss aus mindestens einem Zeichen bestehen, das kein Leerzeichen ist.

**sztemplatetablename**

Der Name einer vorhandenen Tabelle, aus der die Basis-DDL (Data Definition Language) geerbt werden soll. Die Verwendung einer Vorlagen Tabelle ermöglicht die einfache Erstellung von vielen Tabellen mit identischen Spalten und Indizes.

**ulpages**

Die anfängliche Anzahl von Datenbankseiten, die für die Tabelle zuzuordnen sind. Wenn eine Zahl größer als 1 angegeben wird, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.

**uldensity**

Die Tabellen Dichte in Prozent. Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 sein. Das übergeben von 0 bedeutet, dass der Standardwert verwendet werden soll. Der Standardwert ist 80.

**rgcolumncreate**

Ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die jeweils einer Spalte entsprechen, die in der neuen Tabelle erstellt werden soll.

**cColumns**

Die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) Elemente im *rgcolumncreate* -Parameter.

**rgindexcreate**

Ein Array von [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Strukturen, von denen jede einem Index entspricht, der in der neuen Tabelle erstellt werden soll.

**cindexes**

Die Anzahl der [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Elemente im *rgindexcreate* -Parameter.

**szcallback**

Die Funktion, die während bestimmter Ereignisse aufgerufen wird. **cbyp** bestimmt, wann die Rückruffunktion aufgerufen wird.

Das Format von **szcallback** muss "Module \! Function" lauten, – z. b. "Alpha \! Beta" bezieht sich auf die Beta Funktion im Modul "Alpha".

Der Prototyp der Funktion muss mit der [JET_CALLBACK](./jet-callback-callback-function.md) Rückruffunktion identisch sein.

**cbyp**

Beschreibt den Typ der durch **szcallback** bezeichneten Rückruffunktion. Weitere Informationen finden Sie unter [JET_CBTYP](./jet-cbtyp.md).

Dieses Bitfeld besteht aus einem oder mehreren Bitwerten, die in der folgenden Tabelle aufgeführt sind.

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
<td><p>Die Rückruffunktion wird aufgerufen, wenn eine Spalte, die abgeschlossen werden kann, auf NULL gesetzt ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeInsert</p></td>
<td><p>Die Rückruffunktion wird vor dem Einfügen von Datensätzen aufgerufen.</p></td>
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

Eine Gruppe von Bits, die NULL oder mehr der in der folgenden Tabelle aufgeführten aufrufoptions Werte enthält.

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
<td><p>Verhindert DDL-Vorgänge für die Tabelle (z. b. das Hinzufügen oder Entfernen von Spalten).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Bewirkt, dass die Tabelle eine Vorlagen Tabelle ist. In neuen Tabellen kann dann der Name dieser Tabelle als Vorlagen Tabelle angegeben werden. Das Festlegen JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Muss in Verbindung mit JET_bitTableCreateTemplateTable verwendet werden. Veraltet. Nicht verwenden.</p></td>
</tr>
</tbody>
</table>


**pssqspacehints**

Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) -Struktur für den sequenziellen Standard Index.

**p* qspacehints** wurde in Windows 7 eingeführt.

**plvspacehints**

Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) Struktur für eine getrennte Struktur mit langen Werten.

**plvspacehints** wurde in Windows 7 eingeführt.

**cbseparatelv**

Die Größe, mit der ein System internes LV vom primären Datensatz getrennt wird. Eine beliebige lange Wert-c-Struktur für eine getrennte LV-Struktur. Weitere Informationen finden Sie unter ng-Value in [JET_SPACEHINTS](./jet-spacehints-structure.md). Lange Wert Spalten, die kleiner als dieser Wert sind, können getrennt werden, wenn der Datensatz zu groß wird.

**cbseparatelv** wurde in Windows 7 eingeführt.

**TableID**

Ein Ausgabefeld, das den [JET_TABLEID](./jet-tableid.md) der neuen Tabelle enthält, wenn der API-Befehl erfolgreich ausgeführt wird. Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert. Diese Tabelle wird exklusiv geöffnet.

**erstellt**

Ein Ausgabefeld, das die Anzahl der-Objekte enthält, die erstellt werden, wenn der API-Befehl erfolgreich ausgeführt wird. Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.

Die Anzahl der Objekte, die erstellt werden, entspricht der Summe der Spalten, Tabellen und Indizes, die erfolgreich erstellt wurden.

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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_TABLECREATE3_W</strong> (Unicode) und <strong>JET_TABLECREATE3_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Siehe auch

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetkreatetable](./jetcreatetable-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
