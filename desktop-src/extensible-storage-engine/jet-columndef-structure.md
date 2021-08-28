---
description: 'Weitere Informationen zu: JET_COLUMNDEF-Struktur'
title: JET_COLUMNDEF-Struktur
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: fccf3b076b71e8923366a95810d1f3009d4fe1c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471136"
---
# <a name="jet_columndef-structure"></a>JET_COLUMNDEF-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_columndef-structure"></a>JET_COLUMNDEF-Struktur

Die **JET_COLUMNDEF-Struktur** definiert die Daten, die in einer Spalte gespeichert werden können.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe der -Struktur in Bytes. Sie muss auf sizeof( JET_COLUMNDEF) festgelegt werden.

**Columnid**

Reserviert. **columnid** muss auf 0 (null) festgelegt werden.

**coltyp**

Der Typ der Spalte (z. B. Text, binär oder numerisch). Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reserviert. **wCountry** muss auf 0 (null) festgelegt werden.

**langid**

Veraltet. **langid** sollte auf 0 (null) festgelegt werden.

**cp**

Die Codepage für die Spalte. Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200). Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252). Wenn die Spalte keine Textspalte ist, wird die Codepage automatisch auf 0 (null) festgelegt.

**wCollate**

Reserviert. **wCollate** muss auf 0 (null) festgelegt werden.

**cbMax**

Die maximale Länge einer Spalte variabler Länge in Bytes oder die Länge einer Spalte mit fester Länge.

**grbit**

Eine Gruppe von Bits, die die für diesen Aufruf zu verwendenden Optionen enthalten, die null oder mehr der folgenden Werte enthalten.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>Die Spalte wird korrigiert. Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden. JET_bitColumnFixed kann nicht mit JET_bitColumnTagged verwendet werden. Dieses Bit kann nicht mit langen Werten verwendet werden (d. <strong>JET_coltypLongText</strong> und <strong>JET_coltypLongBinary</strong>).</p> | 
| <p>JET_bitColumnTagged</p> | <p>Die Spalte wird markiert. Markierte Spalten nehmen keinen Speicherplatz in der Datenbank ein, wenn sie keine Daten enthalten. Dieses Bit kann nicht mit JET_bitColumnFixed verwendet werden.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>Die Spalte darf nie auf einen NULL-Wert festgelegt werden.</p> | 
| <p>JET_bitColumnVersion</p> | <p>Die Spalte ist eine Versionsspalte, die die Version der Zeile angibt. Der Wert dieser Spalte beginnt bei 0 (null) und wird für jedes Update in der Zeile automatisch erhöht.</p><p>Dieses Bit kann nur auf <strong>JET_coltypLong</strong> Spalten angewendet werden. Dieses Bit kann nicht mit JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate oder JET_bitColumnTagged verwendet werden.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>Die Spalte wird automatisch erhöht. Die Zahl ist eine steigende Zahl und innerhalb einer Tabelle garantiert eindeutig. Die Zahlen sind jedoch möglicherweise nicht kontinuierlich. Wenn beispielsweise fünf Zeilen in eine Tabelle eingefügt werden, kann die Spalte "autoincrement" die Werte { 1, 2, 6, 7, 8 } enthalten. Dieses Bit kann nur für Spalten vom Typ <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong>verwendet werden.</p><p><strong>Windows 2000:</strong> In Windows 2000 kann dieses Bit nur für Spalten vom Typ <strong>JET_coltypLong</strong>verwendet werden.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Dieses Bit ist nur für Aufrufe von <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>gültig.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Dieses Bit ist nur für Aufrufe von <a href="gg294118(v=exchg.10).md">JetOpenTable</a>gültig.</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Dieses Bit ist nur für Aufrufe von <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>gültig.</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>Die Spalte kann mehrwertige Werte aufweisen. Einer mehrwertigen Spalte können null, ein oder mehrere Werte zugeordnet sein. Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl identifiziert, die als <strong>itagSequence-Member</strong> bezeichnet wird und zu verschiedenen Strukturen gehört, <a href="gg294049(v=exchg.10).md">einschließlich: JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>und <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Mehrwertige Spalten müssen mit Tags versehen werden. Das heißt, dass es sich nicht um Spalten mit fester oder variabler Länge handelt.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Gibt an, dass es sich bei einer Spalte um eine Spalte für die Nachschubaktualisierung handelt. Eine Spalte für die Escrow-Aktualisierung kann gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> aktualisiert werden, und die Transaktionskonsistenz wird beibehalten. Eine Spalte zum Aktualisieren der Spalte "escrow" muss außerdem die folgenden Bedingungen erfüllen:</p><ul><li><p>Eine Spalte zum Aktualisieren der Spalte "escrow" kann nur erstellt werden, wenn die Tabelle leer ist.</p></li></ul><ul><li><p>Eine Spalte für die Escrow-Aktualisierung muss vom Typ <strong>JET_coltypLong</strong>sein.</p></li></ul><ul><li><p>Eine Spalte für die Escrow-Aktualisierung muss einen Standardwert aufweisen <strong>(cbDefault</strong> muss positiv sein).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate können nicht in Verbindung mit JET_bitColumnTagged, JET_bitColumnVersion oder JET_bitColumnAutoincrement verwendet werden.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>Die Spalte wird in einem ohne Versionsinformationen erstellt. Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit dem gleichen Namen hinzuzufügen, fehlschlagen. Dieses Bit ist nur bei <a href="gg294122(v=exchg.10).md">JetAddColumn</a>nützlich. Sie kann nicht innerhalb einer Transaktion verwendet werden.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Für die zukünftige Verwendung reserviert.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Verwenden Sie JET_bitColumnDeleteOnZero anstelle von JET_bitColumnFinalize. JET_bitColumnFinalize, dass eine Spalte abgeschlossen werden kann. Wenn eine Spalte, die finalisiert werden kann, über eine Spalte zum Hinterlegungsupdate verfügt, die 0 (null) erreicht, wird die Zeile gelöscht. Zukünftige Versionen können stattdessen eine Rückruffunktion aufrufen (weitere Informationen finden Sie unter <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Eine Spalte, die finalisiert werden kann, muss eine Spalte für die Escrow-Aktualisierung sein. JET_bitColumnFinalize kann nicht mit JET_bitColumnUserDefinedDefault verwendet werden.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt. Siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Eine Spalte mit einem benutzerdefinierten Standardwert muss eine markierte Spalte sein. Das Angeben von JET_bitColumnUserDefinedDefault bedeutet, dass <strong>pvDefault</strong> auf eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur zeigen muss, und <strong>cbDefault</strong> muss auf sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ) festgelegt werden.</p><ul><li><p>JET_bitColumnUserDefinedDefault können nicht in Verbindung mit JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero oder JET_bitColumnMaybeNull verwendet werden.</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>Bei der Spalte handelt es sich um eine Spalte für die Nachschubaktualisierung, und wenn sie 0 (null) erreicht, wird der Datensatz gelöscht. Eine gängige Verwendung für eine Spalte, die finalisiert werden kann, besteht darin, sie als Verweisanzahlfeld zu verwenden, und wenn das Feld 0 (null) erreicht, wird der Datensatz gelöscht. JET_bitColumnDeleteOnZero bezieht sich auf JET_bitColumnFinalize. Eine Delete-on-Zero-Spalte muss eine Spalte für die Escrow-Aktualisierung sein. JET_bitColumnDeleteOnZero kann nicht mit JET_bitColumnFinalize verwendet werden. JET_bitColumnDeleteOnZero kann nicht mit benutzerdefinierten Standardspalten verwendet werden.</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetOpenTempTable2](./jetopentemptable2-function.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
