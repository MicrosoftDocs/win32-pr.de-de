---
description: 'Weitere Informationen finden Sie unter: JET_TABLECREATE3 Struktur'
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
ms.openlocfilehash: 1b3e1f3a21b5e5f901ef039b9cff0cdd52d415d5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983023"
---
# <a name="jet_tablecreate3-structure"></a>JET_TABLECREATE3-Struktur


_**Gilt für:** Windows | Windows Server_

Die **JET_TABLECREATE3-Struktur** enthält die Informationen, die erforderlich sind, um eine Tabelle zu erstellen, die mit Spalten und Indizes in einer ESE-Datenbank (Extensible Storage Engine) aufgefüllt wird, und die eine Rückruffunktion bezeichnet. Die **JET_TABLECREATE3** struktur wird von der [JetCreateTableColumnIndex3-Funktion](./jetcreatetablecolumnindex3-function.md) verwendet.

Die **JET_TABLECREATE3-Struktur** wurde im Windows 7-Betriebssystem eingeführt.

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

  - Sie muss einen Wert haben, der kleiner als JET_cbNameMost ist, ohne den beendenden NULL-Wert.

  - Sie muss aus den folgenden Zeichen bestehen: 0 bis 9, A bis Z, a bis z und allen anderen Satzzeichen außer Ausrufezeichen ( ), Komma (,), öffnenden eckigen Klammern ( ) und schließenden Klammern ( ), d. h. ASCII-Zeichen 0x20, 0x22 bis \! \[ \] 0x2d, 0x2f bis 0x5a, 0x5c und 0x5d bis 0x7f.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss aus mindestens einem Zeichen ohne Leerzeichen bestehen.

**szTemplateTableName**

Der Name einer vorhandenen Tabelle, von der die Basisdatendefinitionssprache (Base Data Definition Language, DDL) geerbt werden soll. Die Verwendung einer Vorlagentabelle ermöglicht die einfache Erstellung vieler Tabellen mit identischen Spalten und Indizes.

**ulPages**

Die anfängliche Anzahl von Datenbankseiten, die der Tabelle zuteilen sind. Wenn Sie eine Zahl angeben, die größer als 1 ist, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.

**ulDensity**

Die Tabellendichte in Prozent. Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 liegen. Das Übergeben von 0 bedeutet, dass der Standardwert verwendet werden soll. Der Standardwert ist 80.

**rgcolumncreate**

Ein Array [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die jeweils einer Spalte entsprechen, die in der neuen Tabelle erstellt werden soll.

**cColumns**

Die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) im *rgcolumncreate-Parameter.*

**rgindexcreate**

Ein Array [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Strukturen, die jeweils einem Index entsprechen, der in der neuen Tabelle erstellt werden soll.

**cIndexes**

Die Anzahl der [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) im *rgindexcreate-Parameter.*

**szCallback**

Die Funktion, die während bestimmter Ereignisse aufgerufen wird. **cbtyp** bestimmt, wann die Rückruffunktion aufgerufen wird.

Das Format von **szCallback** muss "Modulfunktion" sein. "alpha beta" bezieht sich beispielsweise auf die Betafunktion im Modul \! mit dem Namen \! "alpha".

Der Prototyp der Funktion muss mit der [Rückruffunktion JET_CALLBACK](./jet-callback-callback-function.md) übereinstimmen.

**cbtyp**

Beschreibt den Typ der Rückruffunktion, die von **szCallback festgelegt wird.** Weitere Informationen finden Sie unter [JET_CBTYP](./jet-cbtyp.md).

Dieses Bitfeld besteht aus mindestens einem der in der folgenden Tabelle aufgeführten Bitwerte.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_cbtypFinalize</p> | <p>Die Rückruffunktion wird aufgerufen, wenn eine Spalte, die finalisiert werden kann, auf 0 (null) gesetzt wurde.</p> | 
| <p>JET_cbtypBeforeInsert</p> | <p>Die Rückruffunktion wird vor dem Einfügen des Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterInsert</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem die Datenbank-Engine das Einfügen eines Datensatzes abgeschlossen hat.</p> | 
| <p>JET_cbtypBeforeReplace</p> | <p>Die Rückruffunktion wird vor der Änderung eines Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterReplace</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem die Änderung eines Datensatzes beendet wurde.</p> | 
| <p>JET_cbtypBeforeDelete</p> | <p>Die Rückruffunktion wird vor dem Löschen eines Datensatzes aufgerufen.</p> | 
| <p>JET_cbtypAfterDelete</p> | <p>Die Rückruffunktion wird aufgerufen, nachdem ein Datensatz gelöscht wurde.</p> | 
| <p>JET_cbtypUserDefinedDefaultValue</p> | <p>Die Rückruffunktion wird aufgerufen, um einen benutzerdefinierten Standardwert zu berechnen.</p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einem Cursor zugeordnet ist, frei werden muss.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einer Tabelle zugeordnet ist, frei werden muss.</p> | 



**grbit**

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Aufrufoptionswerte enthält.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>Verhindert DDL-Vorgänge für die Tabelle (z. B. Hinzufügen oder Entfernen von Spalten).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>Bewirkt, dass die Tabelle eine Vorlagentabelle ist. Neue Tabellen können dann den Namen dieser Tabelle als Vorlagentabelle angeben. Das JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Muss in Verbindung mit der -JET_bitTableCreateTemplateTable. Veraltet. Nicht verwenden.</p> | 



**pSeqSpacehints**

Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) für einen sequenziellen Standardindex.

**pSeqSpacehints** wurde in Windows 7 eingeführt.

**pLVSpacehints**

Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) struktur für eine Struktur mit getrennten langen Wert.

**pLVSpacehints** wurde in Windows 7 eingeführt.

**cbSeparateLV**

Die Größe, um eine systeminterne LV vom primären Datensatz zu trennen. Jede long-value c-Struktur für eine separate LV-Struktur. Weitere Informationen finden Sie unter ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md). Spalten mit langen Werte, die kleiner als dieser Wert sind, können getrennt werden, wenn der Datensatz zu groß wird.

**cbSeparateLV** wurde in Windows 7 eingeführt.

**tableid**

Ein Ausgabefeld, das [die](./jet-tableid.md) JET_TABLEID der neuen Tabelle enthält, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert. Diese Tabelle wird exklusiv geöffnet.

**cCreated**

Ein Ausgabefeld, das die Anzahl der Objekte enthält, die erstellt werden, wenn der API-Aufruf erfolgreich ist. Wenn der API-Aufruf fehlschlägt, ist der Wert nicht definiert.

Die Anzahl der erstellten Objekte entspricht der Summe der Spalten, Tabellen und Indizes, die erfolgreich erstellt wurden.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JET_TABLECREATE3_W</strong> (Unicode) und <strong>JET_TABLECREATE3_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Siehe auch

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
