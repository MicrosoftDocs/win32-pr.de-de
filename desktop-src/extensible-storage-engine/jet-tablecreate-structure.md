---
description: 'Weitere Informationen finden Sie unter: JET_TABLECREATE Struktur'
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
ms.openlocfilehash: fcc6c63b06614eb16379fbb18d59a5459a8e5085
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983033"
---
# <a name="jet_tablecreate-structure"></a>JET_TABLECREATE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_tablecreate-structure"></a>JET_TABLECREATE-Struktur

Die **JET_TABLECREATE-Struktur** enthält die Informationen, die zum Erstellen einer Tabelle erforderlich sind, die mit Spalten und Indizes in einer ESE-Datenbank aufgefüllt wird. Die **JET_TABLECREATE** wird von [JetCreateTableColumnIndex verwendet.](./jetcreatetablecolumnindex-function.md)

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

Die Größe dieser Struktur in Bytes (für zukünftige Erweiterungen). Sie muss auf sizeof( JET_TABLECREATE ) in Bytes festgelegt werden.

**szTableName**

Der Name der zu erstellenden Tabelle.

Der Name muss folgende Bedingungen erfüllen:

  - Der Wert ist kleiner als JET_cbNameMost, ohne den beendenden NULL-Wert.

<!-- end list -->

  - Sie bestehen aus den folgenden Zeichen: 0 bis 9, A bis Z, a bis z und alle anderen Interpunktionen mit Ausnahme von Ausrufezeichen ( ), Komma (,), öffnenden eckigen Klammern () und schließenden Klammern (), d. h. ASCII-Zeichen 0x20, 0x22 bis \! \[ \] 0x2d, 0x2f bis 0x5a, 0x5c und 0x5d bis 0x7f.

<!-- end list -->

  - Beginnen Sie nicht mit einem Leerzeichen.

<!-- end list -->

  - Besteht aus mindestens einem Zeichen, das kein Leerzeichen ist.

**szTemplateTableName**

Der Name einer bereits vorhandenen Tabelle, von der die Basis-DDL (Data Definition Language) geerbt werden soll. Die Verwendung einer Vorlagentabelle ermöglicht die einfache Erstellung vieler Tabellen mit identischen Spalten und Indizes.

**ulPages**

Die anfängliche Anzahl von Datenbankseiten, die der Tabelle zuteilen sind. Wenn Sie eine Zahl angeben, die größer als 1 ist, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.

**ulDensity**

Die Tabellendichte in Prozent. Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 liegen. Das Übergeben von 0 bedeutet, dass der Standardwert verwendet werden soll. Der Standardwert beträgt 80.

**rgcolumncreate**

Ein Array [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die jeweils einer Spalte entsprechen, die in der neuen Tabelle erstellt werden soll.

**cColumns**

Die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) in **rgcolumncreate**.

**rgindexcreate**

Ein Array [JET_INDEXCREATE](./jet-indexcreate-structure.md) Strukturen, die jeweils einem Index entsprechen, der in der neuen Tabelle erstellt werden soll.

**cIndexes**

Die Anzahl der [JET_INDEXCREATE](./jet-indexcreate-structure.md) in **rgindexerzeugen**.

**grbit**

Eine Gruppe von Bits, die die Optionen für diesen Aufruf enthalten, die null oder mehr der folgenden Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Das JET_bitTableCreateFixedDDL verhindert DDL-Vorgänge für die Tabelle (z. B. das Hinzufügen oder Entfernen von Spalten).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Das JET_bitTableCreateTemplateTable bewirkt, dass die Tabelle eine Vorlagentabelle ist. Neue Tabellen können dann den Namen dieser Tabelle als Vorlagentabelle angeben. Das JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Veraltet. Nicht verwenden.</p> | 



**tableid**

Ein Ausgabefeld, das [die](./jet-tableid.md) JET_TABLEID der neuen Tabelle enthält, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert.

**cCreated**

Ein Ausgabefeld, das die Anzahl der erstellten Objekte enthält, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert.

Die Anzahl der erstellten Objekte entspricht der Summe der Erfolgreich erstellten Spalten, Tabellen und Indizes.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_TABLECREATE_W</strong> (Unicode) <strong>und</strong> JET_TABLECREATE_A (ANSI) implementiert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
