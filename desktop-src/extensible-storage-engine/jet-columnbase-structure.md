---
description: 'Weitere Informationen finden Sie unter: JET_COLUMNBASE Struktur'
title: JET_COLUMNBASE-Struktur
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: eb9ac3377e97079794a8d4c81d4f8be59587870c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468647"
---
# <a name="jet_columnbase-structure"></a>JET_COLUMNBASE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columnbase-structure"></a>JET_COLUMNBASE-Struktur

Die **JET_COLUMNBASE-Struktur** beschreibt die Parameter einer Basisspalte. Die [JetGetColumnInfo- und](./jetgetcolumninfo-function.md) [JetGetTableColumnInfo-Funktionen](./jetgettablecolumninfo-function.md) verwenden die **JET_COLUMNBASE** Struktur.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe dieser Struktur in Bytes. Legen **Sie cbStruct** auf sizeof( JET_COLUMNBASE ) fest.

**Columnid**

Reserviert. Legen **Sie columnid** auf 0 (null) fest.

**coltyp**

Der Typ der Spalte (z. B. Text, binär oder numerisch). Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reserviert. Legen Sie auf 0 (null) fest.

**langid**

Reserviert. Legen Sie auf 0 (null) fest.

**cp**

Die Codepage für die Spalte. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252). Wenn die Spalte keine Textspalte ist, wird die Codepage automatisch auf 0 (null) festgelegt.

**wFiller**

Reserviert. Legen Sie auf 0 (null) fest.

**cbMax**

Die maximale Länge einer Spalte variabler Länge in Bytes oder die tatsächliche Länge einer Spalte fester Länge in Bytes.

**grbit**

Optionen für die Spalte, einschließlich null oder mehr der folgenden Werte.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>Die Spalte ist fest und belegt den gleichen Speicherplatz in einer Zeile, unabhängig davon, wie viele Daten sie enthält. JET_bitColumnFixed kann nicht mit JET_bitColumnTagged kombiniert und nicht verwendet werden, wenn der <strong>Coltyp-Member</strong> auf JET_coltypLongText <strong>oder</strong> <strong>JET_coltypLongBinary.</strong></p> | 
| <p>JET_bitColumnTagged</p> | <p>Die Spalte wird nur dann markiert und belegt Speicherplatz in der Datenbank, wenn sie Daten enthält. JET_bitColumnTagged kann nicht mit JET_bitColumnFixed, JET_bitColumnVersion oder JET_bitColumnEscrowUpdate.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>Die Spalte darf nicht auf einen <strong>NULL-Wert festgelegt</strong> werden.</p><p>JET_bitColumnNotNULL kann nicht mit einem JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnVersion</p> | <p>Die Spalte ist eine Versionsspalte, die die Version der Zeile angibt. Der Wert dieser Spalte beginnt bei 0 (null) und wird für jede Aktualisierung der Zeile automatisch erhöht.</p><p>JET_bitColumnVersion kann nur verwendet werden, wenn der <strong>Coltyp-Member</strong> auf <strong>JET_coltypLong</strong> festgelegt ist und nicht mit JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged oder JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>Die Spalte wird automatisch erhöht. Die Zahl ist eine steigende Zahl, und es ist garantiert, dass sie innerhalb einer Tabelle eindeutig ist. Die Zahlen sind jedoch möglicherweise nicht sequenziell. Wenn beispielsweise fünf Zeilen in eine Tabelle eingefügt werden, kann die automatisch inkrementierte Spalte die Werte { 1, 2, 6, 7, 8 } enthalten.</p><p>JET_bitColumnAutoincrement kann nur verwendet werden, wenn der <strong>Coltyp-Member</strong> auf <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong> festgelegt ist und nicht mit JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault oder JET_bitColumnVersion.</p><p><strong>Windows 2000:</strong> JET_bitColumnVersion kann nur verwendet werden, wenn der <strong>Coltyp-Member</strong> auf <strong>JET_coltypLong.</strong></p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Nur für Aufrufe von <a href="gg269215(v=exchg.10).md">JetGetColumnInfo gültig.</a> JET_bitColumnUpdatable kann nicht mit einem JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Nur für Aufrufe von <a href="gg294118(v=exchg.10).md">JetOpenTable gültig.</a></p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Nur für Aufrufe von <a href="gg269211(v=exchg.10).md">JetOpenTempTable gültig.</a></p> | 
| <p>JET_bitColumnMultiValued</p> | <p>Die Spalte kann mehrere Werte haben. Einer mehrwertigen Spalte können null, ein oder mehrere Werte zugeordnet sein. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl im <strong>itagSequence-Member</strong> verschiedener Strukturen identifiziert, z. B. <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Mehrwertige Spalten müssen mit Tags versehen sein. Dies bedeutet, dass es sich möglicherweise nicht um Spalten fester länge oder variabler Länge handelt.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Gibt an, dass es sich bei einer Spalte um eine Escrow-Updatespalte handelt, die gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> aktualisiert werden kann und transaktionskonsistent ist.</p><ul><li><p>Eine Spalte zum Aktualisieren der Stirnrunzeln kann nur erstellt werden, wenn die Tabelle leer ist.</p></li></ul><ul><li><p>Für eine Spalte zum Aktualisieren der Stirnrunzeln muss <strong>das Coltyp-Member</strong> auf <strong>JET_coltypLong.</strong></p></li></ul><ul><li><p>Eine Spalte zum Aktualisieren der Stirnrunzel muss über einen Standardwert verfügen (d. h. <strong>cbDefault</strong> muss positiv sein).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate kann nicht mit JET_bitColumnTagged, JET_bitColumnVersion oder JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>Die Spalte wird ohne Versionsnummer erstellt. Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit dem gleichen Namen hinzuzufügen, fehlschlagen. JET_bitColumnUnversioned wird nur mit <a href="gg294122(v=exchg.10).md">JetAddColumn verwendet.</a> Sie kann nicht innerhalb einer Transaktion verwendet werden.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Für die zukünftige Verwendung reserviert.</p><p>JET_bitColumnMaybeNull kann nicht mit -JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Darf nicht verwendet werden. Verwenden JET_bitColumnDeleteOnZero stattdessen .</p><p>Die Spalte kann finalisiert werden. Eine Spalte, die finalisiert werden kann, ist eine Hinterlegungsaktualisierungsspalte, die bewirkt, dass die Zeile gelöscht wird, wenn die Spalte 0 (null) erreicht. Zukünftige Versionen können stattdessen eine Rückruffunktion aufrufen (siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Eine Spalte, die finalisiert werden kann, muss eine Spalte für die Aktualisierung nach der Stirnrunzel sein. JET_bitColumnFinalize kann nicht mit -JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt. Siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Eine Spalte mit einem benutzerdefinierten Standardwert muss eine markierte Spalte sein. Wenn JET_bitColumnUserDefinedDefault angegeben wird, muss <strong>der pvDefault</strong> auf eine JET_USERDEFINEDDEFAULT-Struktur verweisen, und <a href="gg269200(v=exchg.10).md"></a> <strong>cbDefault</strong> muss auf sizeof( JET_USERDEFINEDDEFAULT ) festgelegt werden.</p><p>JET_bitColumnUserDefinedDefault kann nicht mit JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero oder JET_bitColumnMaybeNull.</p> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>Bei der Spalte handelt es sich um eine Spalte zum Aktualisieren der Stirnrunzeln, und wenn sie 0 (null) erreicht, wird der Datensatz gelöscht. Eine häufige Verwendung für Löschspalten ohne Null ist die Verwendung von Verweiszählerfeldern. Wenn die Anzahl der Verweise auf 0 (null) fällt, wird der Datensatz gelöscht. Eine Delete-on-Zero-Spalte muss eine Spalte mit der Spalte "escrow update" sein.</p><p>JET_bitColumnDeleteOnZero ersetzt JET_bitColumnFinalize.</p><p>JET_bitColumnDeleteOnZero können nicht mit JET_bitColumnFinalize oder JET_bitColumnUserDefinedDefault kombiniert und nicht mit benutzerdefinierten Standardspalten verwendet werden.</p> | 



**szBaseTableName**

Die Tabelle, von der die aktuelle Tabelle ihre DDL erbt.

**szBaseColumnName**

Der Name der Spalte in der Vorlagentabelle.

### <a name="remarks"></a>Hinweise

**JET_COLUMNBASE** enthält einen Großteil der gleichen Informationen wie [JET_COLUMNDEF](./jet-columndef-structure.md), fügt jedoch Zeichenfolgenfelder hinzu, um die Basistabelle zu beschreiben (wenn eine hierarchische DDL verwendet wurde).

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JET_COLUMNBASE_W</strong> (Unicode) und <strong>JET_COLUMNBASE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
