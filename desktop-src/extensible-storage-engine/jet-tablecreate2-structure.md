---
description: 'Weitere Informationen finden Sie unter: JET_TABLECREATE2 Struktur'
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
ms.openlocfilehash: b4d84a21fc9115823eaff0716b90ee37f1ae6655
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988103"
---
# <a name="jet_tablecreate2-structure"></a>JET_TABLECREATE2-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_tablecreate2-structure"></a>JET_TABLECREATE2-Struktur

Die **JET_TABLECREATE2-Struktur** enthält die Informationen, die zum Erstellen einer Tabelle erforderlich sind, die mit Spalten und Indizes in einer ESE-Datenbank aufgefüllt wird und die eine Rückruffunktion bestimmt. Die **JET_TABLECREATE2** wird von [JetCreateTableColumnIndex2 verwendet.](./jetcreatetablecolumnindex2-function.md)

**Windows XP:** Die **JET_TABLECREATE2-Struktur** wird in xp Windows eingeführt.

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

**szCallback**

Die Funktion, die während bestimmter Ereignisse aufgerufen wird. **cbtyp** bestimmt, wann die Rückruffunktion aufgerufen wird.

Das Format von **szCallback** muss "Modulfunktion" lauten. "alpha beta" bezieht sich beispielsweise auf die Betafunktion im Modul \! mit dem Namen \! "alpha". Der Prototyp der Funktion muss [mit](./jet-callback-callback-function.md)JET_CALLBACK. Weitere Informationen finden Sie unter [JET_CALLBACK](./jet-callback-callback-function.md).

**cbtyp**

Beschreibt den Typ der Rückruffunktion, die von **szCallback festgelegt wird.** Weitere Informationen finden Sie unter [JET_CBTYP](./jet-cbtyp.md). Dieses Bitfeld besteht aus mindestens einem der folgenden Bits.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_cbtypFinalize</p> | <p>Die Rückruffunktion wird aufgerufen, wenn eine Spalte, die finalisiert werden kann, auf 0 (null) gesetzt wurde.</p> | 
| <p>JET_cbtypBeforeInsert</p> | <p>Die Rückruffunktion wird vor dem Einfügen des Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterInsert</p> | <p>Die Rückruffunktion wird aufgerufen, sobald die Datenbank-Engine das Einfügen eines Datensatzes abgeschlossen hat.</p> | 
| <p>JET_cbtypBeforeReplace</p> | <p>Die Rückruffunktion wird vor der Änderung eines Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterReplace</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem die Änderung eines Datensatzes beendet wurde.</p> | 
| <p>JET_cbtypBeforeDelete</p> | <p>Die Rückruffunktion wird vor dem Löschen eines Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterDelete</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem ein Datensatz gelöscht wurde.</p> | 
| <p>JET_cbtypUserDefinedDefaultValue</p> | <p>Die Rückruffunktion wird aufgerufen, um einen benutzerdefinierten Standardwert zu berechnen.</p> | 
| <p>JET_cbtypOnlineDefragCompleted</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem ein Aufruf von <a href="gg294095(v=exchg.10).md">JetDefragment2</a> abgeschlossen wurde.</p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einem Cursor zugeordnet ist, frei werden muss.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einer Tabelle zugeordnet ist, frei werden muss.</p> | 



**grbit**

Eine Gruppe von Bits, die die Optionen für diesen Aufruf enthalten, die null oder mehr der folgenden Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Das JET_bitTableCreateFixedDDL verhindert DDL-Vorgänge für die Tabelle (z. B. das Hinzufügen oder Entfernen von Spalten).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Das JET_bitTableCreateTemplateTable bewirkt, dass die Tabelle eine Vorlagentabelle ist. Neue Tabellen können dann den Namen dieser Tabelle als Vorlagentabelle angeben. Das JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Muss in Verbindung mit der -JET_bitTableCreateTemplateTable. Veraltet. Nicht verwenden.</p> | 



**tableid**

Ein Ausgabefeld, das [die](./jet-tableid.md) JET_TABLEID der neuen Tabelle enthält, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert.

**cCreated**

Ein Ausgabefeld, das die Anzahl der Objekte enthält, die erstellt werden, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert.

Die Anzahl der erstellten Objekte entspricht der Summe der Erfolgreich erstellten Spalten, Tabellen und Indizes.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_TABLECREATE2_W</strong> (Unicode) und JET_TABLECREATE2_A (ANSI) implementiert. <strong></strong></p> | 



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
