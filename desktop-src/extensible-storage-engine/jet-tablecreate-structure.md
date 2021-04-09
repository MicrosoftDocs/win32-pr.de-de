---
description: 'Weitere Informationen finden Sie hier: JET_TABLECREATE Struktur'
title: JET_TABLECREATE-Struktur
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128184"
---
# <a name="jet_tablecreate-structure"></a>JET_TABLECREATE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_tablecreate-structure"></a>JET_TABLECREATE-Struktur

Die **JET_TABLECREATE** Struktur enthält die Informationen, die erforderlich sind, um eine Tabelle zu erstellen, die mit Spalten und Indizes in einer ESE-Datenbank aufgefüllt ist. Die **JET_TABLECREATE** Struktur wird von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) verwendet.

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe dieser-Struktur in Bytes (für zukünftige Erweiterungen). Er muss auf sizeof (JET_TABLECREATE) in Bytes festgelegt werden.

**sztablename**

Der Name der zu erstellenden Tabelle.

Der Name muss die folgenden Bedingungen erfüllen:

  - Ein Wert, der kleiner als JET_cbNameMost ist, ohne den abschließenden NULL-Wert.

<!-- end list -->

  - Besteht aus folgendem Zeichensatz: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Punkte außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer ( \] ), d. h. ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.

<!-- end list -->

  - Beginnen Sie nicht mit einem Leerzeichen.

<!-- end list -->

  - Besteht aus mindestens einem Zeichen, das kein Leerzeichen ist.

**sztemplatetablename**

Der Name einer bereits vorhandenen Tabelle, aus der die Basis-DDL (Data Definition Language) geerbt werden soll. Die Verwendung einer Vorlagen Tabelle ermöglicht die einfache Erstellung von vielen Tabellen mit identischen Spalten und Indizes.

**ulpages**

Die anfängliche Anzahl von Datenbankseiten, die für die Tabelle zuzuordnen sind. Wenn eine Zahl größer als 1 angegeben wird, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.

**uldensity**

Die Tabellen Dichte in Prozent. Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 sein. Das übergeben von 0 bedeutet, dass der Standardwert verwendet werden soll. Der Standardwert ist 80.

**rgcolumncreate**

Ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die jeweils einer Spalte entsprechen, die in der neuen Tabelle erstellt werden soll.

**cColumns**

Die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) Elemente in **rgcolumncreate**.

**rgindexcreate**

Ein Array von [JET_INDEXCREATE](./jet-indexcreate-structure.md) Strukturen, von denen jede einem Index entspricht, der in der neuen Tabelle erstellt werden soll.

**cindexes**

Die Anzahl der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Elemente in **rgindexcreate**.

**grbit**

Eine Gruppe von Bits, die die Optionen für diesen-Befehl enthalten, die 0 (null) oder mehrere der folgenden Werte enthalten.

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
<td><p>Das Festlegen von JET_bitTableCreateFixedDDL verhindert DDL-Vorgänge für die Tabelle (z. b. das Hinzufügen oder Entfernen von Spalten)</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Das Festlegen von JET_bitTableCreateTemplateTable bewirkt, dass die Tabelle eine Vorlagen Tabelle ist. In neuen Tabellen kann dann der Name dieser Tabelle als Vorlagen Tabelle angegeben werden. Das Festlegen JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Veraltet. Nicht verwenden.</p></td>
</tr>
</tbody>
</table>


**TableID**

Ein Ausgabefeld, das den [JET_TABLEID](./jet-tableid.md) der neuen Tabelle enthält, wenn der API-Befehl erfolgreich ausgeführt wird. Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.

**erstellt**

Ein Ausgabefeld, das die Anzahl der-Objekte enthält, die beim erfolgreichen API-Rückruf erstellt werden. Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.

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
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_TABLECREATE_W</strong> (Unicode) und <strong>JET_TABLECREATE_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[Jetkreatetable](./jetcreatetable-function.md)  
[Jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
