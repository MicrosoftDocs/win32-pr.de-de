---
description: 'Weitere Informationen zu: JET_TABLECREATE2-Struktur'
title: JET_TABLECREATE2-Struktur
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: 95e4d60ba80317624004fa7c9335005aa16a9300
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476466"
---
# <a name="jet_tablecreate2-structure"></a>JET_TABLECREATE2-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_tablecreate2-structure"></a>JET_TABLECREATE2-Struktur

Die **JET_TABLECREATE2-Struktur** enthält die Informationen, die zum Erstellen einer Tabelle erforderlich sind, die mit Spalten und Indizes in einer ESE-Datenbank aufgefüllt ist und eine Rückruffunktion bestimmt. Die **JET_TABLECREATE2-Struktur** wird von [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)verwendet.

**Windows XP:** Die **JET_TABLECREATE2-Struktur** wird in Windows XP eingeführt.

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe dieser Struktur in Bytes (für zukünftige Erweiterungen). Sie muss auf sizeof( JET_TABLECREATE2 ) in Bytes festgelegt werden.

**szTableName**

Der Name der zu erstellende Tabelle.

Der Name muss folgende Bedingungen erfüllen:

  - Weisen Sie einen Wert kleiner als JET_cbNameMost auf, ohne dass der abschließende NULL-Wert enthalten ist.

<!-- end list -->

  - Besteht aus den folgenden Zeichen: 0 bis 9, A bis Z, a bis z und allen anderen Interpunktionszeichen mit Ausnahme von Ausrufezeichen ( \! ), Komma (,), öffnende Klammer ( \[ ) und schließende Klammer ( ), d. h. \] ASCII-Zeichen 0x20, 0x22 durch 0x2d, 0x2f durch 0x5a, 0x5c und 0x5d durch 0x7f.

<!-- end list -->

  - Beginnen Sie nicht mit einem Leerzeichen.

<!-- end list -->

  - Besteht aus mindestens einem Zeichen ohne Leerzeichen.

**szTemplateTableName**

Der Name einer bereits vorhandenen Tabelle, von der Basis-DDL (Data Definition Language) geerbt werden soll. Die Verwendung einer Vorlagentabelle ermöglicht die einfache Erstellung vieler Tabellen mit identischen Spalten und Indizes.

**ulPages**

Die anfängliche Anzahl der Datenbankseiten, die für die Tabelle zugeordnet werden sollen. Wenn Sie eine Zahl angeben, die größer als 1 ist, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.

**ulDensity**

Die Tabellendichte in Prozent. Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 liegen. Die Übergabe von 0 bedeutet, dass der Standardwert verwendet werden soll. Der Standardwert beträgt 80.

**rgcolumncreate**

Ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, von denen jede einer Spalte entspricht, die in der neuen Tabelle erstellt werden soll.

**cColumns**

die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) Elemente in **rgcolumncreate**.

**rgindexcreate**

Ein Array von [JET_INDEXCREATE](./jet-indexcreate-structure.md) Strukturen, von denen jede einem Index entspricht, der in der neuen Tabelle erstellt werden soll.

**cIndexes**

Die Anzahl der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Elemente in **rgindexcreate**.

**szCallback**

Die Funktion, die während bestimmter Ereignisse aufgerufen wird. **cbtyp** bestimmt, wann die Rückruffunktion aufgerufen wird.

Das Format von **szCallback** muss \! "Modulfunktion" sein, z.B. bezieht sich "alpha \! beta" auf die Betafunktion im Modul mit dem Namen "alpha". Der Prototyp der Funktion muss [mit JET_CALLBACK](./jet-callback-callback-function.md)übereinstimmen. Weitere Informationen finden Sie unter [JET_CALLBACK](./jet-callback-callback-function.md).

**cbtyp**

Beschreibt den Typ der rückruffunktion, die von **szCallback** festgelegt wird. Weitere Informationen finden Sie unter [JET_CBTYP](./jet-cbtyp.md). Dieses Bitfeld besteht aus einem oder mehreren der folgenden Bits.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_cbtypFinalize</p> | <p>Die Rückruffunktion wird aufgerufen, wenn eine Spalte, die finalisiert werden kann, 0 (null) erreicht hat.</p> | 
| <p>JET_cbtypBeforeInsert</p> | <p>Die Rückruffunktion wird vor dem Einfügen des Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterInsert</p> | <p>Die Rückruffunktion wird aufgerufen, sobald die Datenbank-Engine mit dem Einfügen eines Datensatzes fertig ist.</p> | 
| <p>JET_cbtypBeforeReplace</p> | <p>Die Rückruffunktion wird vor der Änderung eines Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterReplace</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem die Änderung eines Datensatzes abgeschlossen wurde.</p> | 
| <p>JET_cbtypBeforeDelete</p> | <p>Die Rückruffunktion wird vor dem Löschen eines Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterDelete</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem ein Datensatz gelöscht wurde.</p> | 
| <p>JET_cbtypUserDefinedDefaultValue</p> | <p>Die Rückruffunktion wird aufgerufen, um einen benutzerdefinierten Standardwert zu berechnen.</p> | 
| <p>JET_cbtypOnlineDefragCompleted</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem ein Aufruf von <a href="gg294095(v=exchg.10).md">JetDefragment2</a> abgeschlossen wurde.</p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einem Cursor zugeordnet ist, freigegeben werden muss.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einer Tabelle zugeordnet ist, freigegeben werden muss.</p> | 



**grbit**

Eine Gruppe von Bits, die die Optionen für diesen Aufruf enthalten, die null oder mehr der folgenden Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Das Festlegen JET_bitTableCreateFixedDDL verhindert DDL-Vorgänge für die Tabelle (z. B. das Hinzufügen oder Entfernen von Spalten).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Das Festlegen JET_bitTableCreateTemplateTable bewirkt, dass die Tabelle eine Vorlagentabelle ist. Neue Tabellen können dann den Namen dieser Tabelle als Vorlagentabelle angeben. Das Festlegen JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Muss in Verbindung mit JET_bitTableCreateTemplateTable verwendet werden. Veraltet. Nicht verwenden.</p> | 



**tableid**

Ein Ausgabefeld, das die [JET_TABLEID](./jet-tableid.md) der neuen Tabelle enthält, wenn der API-Aufruf erfolgreich war. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert.

**cCreated**

Ein Ausgabefeld, das die Anzahl der Objekte enthält, die erstellt werden, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert.

Die Anzahl der erstellten Objekte entspricht der Summe der Spalten, Tabellen und Indizes, die erfolgreich erstellt wurden.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_TABLECREATE2_W</strong> (Unicode) <strong>und</strong> JET_TABLECREATE2_A (ANSI) implementiert.</p> | 



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
