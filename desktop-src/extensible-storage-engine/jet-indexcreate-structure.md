---
description: 'Weitere Informationen finden Sie unter: JET_INDEXCREATE Struktur'
title: JET_INDEXCREATE-Struktur
TOCTitle: JET_INDEXCREATE Structure
ms:assetid: 0c55f25c-d42a-49ba-a1fe-549850fdc9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269186(v=EXCHG.10)
ms:contentKeyID: 32765489
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
ms.openlocfilehash: 237e6351c7baf7f418c5160797f413d78ce034bd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984153"
---
# <a name="jet_indexcreate-structure"></a>JET_INDEXCREATE-Struktur


_**Gilt für:** Windows | Windows Server_

Die **JET_INDEXCREATE-Struktur** enthält die Informationen, die zum Erstellen eines Indexes für Daten in einer ESE-Datenbank (Extensible Storage Engine) erforderlich sind. Die -Struktur wird von Funktionen wie [JetCreateIndex2](./jetcreateindex2-function.md)und in Strukturen wie JET_TABLECREATE [und](./jet-tablecreate-structure.md) [JET_TABLECREATE2.](./jet-tablecreate2-structure.md)

``` c++
typedef struct tagJET_INDEXCREATE {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
  unsigned long cbKeyMost;
} JET_INDEXCREATE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe (in Bytes) dieser Struktur. Legen Sie diesen Member auf sizeof( JET_INDEXCREATE ) fest.

**szIndexName**

Der Name des zu erstellenden Indexes.

Der Name des Indexes muss die folgenden Bedingungen erfüllen:

  - Er muss kleiner als JET_cbNameMost sein, ohne den beendenden NULL-Wert.

  - Sie muss aus den folgenden Zeichen bestehen: 0 (null) bis 9, A bis Z, a bis z und alle anderen Interpunktionen außer " \! " (Ausrufezeichen), "," (Komma), " " (öffnende Klammer) und " " ( schließende Klammer) – d. h. ASCII-Zeichen 0x20, 0x22 bis 0x2d, 0x2f bis \[ \] 0x5a, 0x5c, 0x5d bis 0x7f.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss aus mindestens einem Nicht-Leerzeichen bestehen.

**szKey**

Ein Zeiger auf eine double-null-terminierte Zeichenfolge von Token mit NULL-Trennzeichen.

Jedes Token hat das Formular " \<direction-specifier\> \<column-name\> ", wobei direction-specification entweder "+" oder "-" ist. Beispielsweise indiziert ein **szKey** von "+abc \\ 0-def 0+ %. 0" über die drei Spalten "abc" (in aufsteigender Reihenfolge), "def" (in absteigender Reihenfolge) und \\ \\ "uff" (in aufsteigender Reihenfolge). In der Programmiersprache C verfügen Zeichenfolgenliterale über ein implizites **NULL-Abschlusszeichen.** daher wird die oben genannte Zeichenfolge durch einen double-NULL-Wert beendet.

Die Anzahl der in **szKey angegebenen** Spalten darf den Wert von JET_ccolKeyMost **(einer** versionsabhängigen Konstante) nicht überschreiten.

Mindestens eine Spalte muss in **szKey benannt werden.**

Veraltetes Verhalten: Nach dem Double-NULL-Abschlusszeichen ist es möglich, eine Sprach-ID (ein WORD, das an MAKELCID( langid, SORT_DEFAULT ) übergeben wird) anzugeben, um die LCID für den Index anzugeben. Es ist unzulässig, sowohl eine Sprach-ID in **szKey** als [auch](./jet-unicodeindex-structure.md) eine LCID in JET_UNICODEINDEX anzugeben (durch Festlegen JET_bitIndexUnicode in *grbit*).

Veraltet: Nach der Sprach-ID ist es möglich, **cbVarSegMac** als USHORT zu übergeben. Das Verhalten ist nicht definiert, wenn USHORT sowohl in **szKey** als auch in **der Struktur cbVarSegMac** festgelegt ist.

**cbKey**

Die Länge von **szKey** in Bytes, einschließlich der beiden endenden NULL-Werte.

**grbit**

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Werte enthält.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>Doppelte Indexeinträge (Schlüssel) sind nicht zulässig. Dies wird erzwungen, wenn <a href="gg269288(v=exchg.10).md">JetUpdate</a> aufgerufen wird, nicht, wenn <a href="gg294137(v=exchg.10).md">JetSetColumn</a> aufgerufen wird.</p> | 
| <p>JET_bitIndexPrimary</p> | <p>Der Index ist ein primärer (gruppierter) Index. Jede Tabelle muss genau einen primären Index haben. Wenn kein primärer Index explizit für eine Tabelle definiert ist, erstellt die Datenbank-Engine einen eigenen primären Index.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Keine der Spalten, für die der Index erstellt wird, kann einen <strong>NULL-Wert</strong> enthalten.</p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn alle indizierten Spalten <strong>NULL sind.</strong></p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn eine der indizierten Spalten <strong>NULL ist.</strong></p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn die erste spalte, die indiziert wird, <strong>NULL ist.</strong></p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>Indexvorgänge werden lazidiert protokolliert.</p><p>JET_bitIndexLazyFlush hat keine Auswirkungen auf die Trägheit von Datenupdates. Wenn der Indizierungsvorgang durch die Prozessbeendigung unterbrochen wird, kann die Soft Recovery die Datenbank weiterhin in einen konsistenten Zustand zurückbezustanden, aber der Index ist möglicherweise nicht vorhanden.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>Versuchen Sie nicht, den Index zu erstellen, da alle Einträge als <strong>NULL ausgewertet würden.</strong> <strong>Grbit muss</strong> auch angeben JET_bitIgnoreAnyNull wenn JET_bitIndexEmpty übergeben wird. Dies ist eine Leistungsverbesserung. Wenn einer Tabelle beispielsweise eine neue Spalte hinzugefügt wird, wird ein Index für diese neu hinzugefügte Spalte erstellt, und alle Datensätze in der Tabelle werden überprüft, obwohl sie nicht dem Index hinzugefügt wurden. Wenn sie JET_bitIndexEmpty, wird die Überprüfung der Tabelle übersprungen, was möglicherweise sehr lange dauern kann.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>Bewirkt, dass die Indexerstellung für andere Transaktionen sichtbar ist. In der Regel kann eine Sitzung in einer Transaktion keinen Indexerstellungsvorgang in einer anderen Sitzung sehen. Dieses Flag kann nützlich sein, wenn eine andere Transaktion wahrscheinlich denselben Index erstellt. Bei der zweiten Indexerstelle wird ein Fehler verursacht, anstatt potenziell viele unnötige Datenbankvorgänge zu verursachen. Die zweite Transaktion kann den Index möglicherweise nicht sofort verwenden. Der Indexerstellungsvorgang muss abgeschlossen werden, bevor er verwendet werden kann. Die Sitzung darf sich derzeit nicht in einer Transaktion befindet, um einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>Wenn Sie dieses Flag angeben, werden <strong>NULL-Werte</strong> nach Daten für alle Spalten im Index sortiert.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>Die Angabe dieses Flags wirkt sich auf die Interpretation des Felds lcid/pidxunicde union in der Struktur aus. Das Festlegen des Bits bedeutet, <strong>dass das Feld pidxunicode</strong> tatsächlich auf eine <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> verweist. JET_bitIndexUnicode ist nicht erforderlich, um Unicode-Daten zu indizieren. Es wird nur verwendet, um die Normalisierung von Unicode-Daten anzupassen.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Gibt an, dass der Index ein Tupelindex ist. Unter <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> finden Sie eine Beschreibung eines Tupelindexes.</p><p>JET_bitIndexTuples wurde im xp Windows Betriebssystem eingeführt.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>Die Angabe dieses Flags wirkt sich auf die Interpretation des <strong>union-Felds cbVarSegMac/ptuplelimits</strong> in der -Struktur aus. Das Festlegen dieses Bits bedeutet, dass das <a href="gg269207(v=exchg.10).md"></a> <strong>Ptuplelimits-Feld</strong> tatsächlich auf eine JET_TUPLELIMITS-Struktur verweist, um benutzerdefinierte Tupelindexgrenzwerte zu ermöglichen (impliziert JET_bitIndexTuples).</p><p>JET_bitIndexTupleLimits wurde im Betriebssystem Windows Server 2003 eingeführt.</p> | 
| <p>JET_bitIndexCrossProduct 0x00004000</p> | <p>Wenn Sie dieses Flag für einen Index angeben, der über mehrere Schlüsselspalten verfügt, bei denen es sich um eine mehrwertige Spalte handelt, wird für jedes Ergebnis eines Kreuzprodukts aller Werte in diesen Schlüsselspalten ein Indexeintrag erstellt. Andernfalls würde der Index nur einen Eintrag für jeden Mehrwert in der wichtigsten Schlüsselspalte enthalten, die eine mehrwertige Spalte ist, und jeder dieser Indexeinträge würde den ersten Mehrwert aus allen anderen Schlüsselspalten verwenden, bei denen es sich um mehrwertige Spalten handelt.</p><p>Wenn Sie z. B. dieses Flag für einen Index über Spalte A mit den Werten "red" und "blue" und über Spalte B mit den Werten "1" und "2" angegeben haben, werden die folgenden Indexeinträge erstellt: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". Andernfalls werden die folgenden Indexeinträge erstellt: "red", "1"; "blue", "1".</p><p>JET_bitIndexCrossProduct wurde im Betriebssystem Windows Vista eingeführt.</p> | 
| <p>JET_bitIndexKeyMost 0x00008000</p> | <p>Wenn Sie dieses Flag angeben, verwendet der Index die maximale Schlüsselgröße, die im <strong>feld cbKeyMost</strong> in der Struktur angegeben ist. Andernfalls verwendet der Index JET_cbKeyMost (255) als maximale Schlüsselgröße.</p><p>JET_bitIndexKeyMost wurde in Windows Vista eingeführt.</p> | 
| <p>JET_bitIndexDisallowTruncation 0x00010000</p> | <p>Die Angabe dieses Flags führt dazu, dass bei jeder Aktualisierung des Indexes, die zu einem abgeschnittenen Schlüssel führen würde, ein Fehler mit JET_errKeyTruncated. Andernfalls werden Schlüssel automatisch abgeschnitten. Weitere Informationen zum Abschneiden von Schlüsseln finden Sie unter der <a href="gg269329(v=exchg.10).md">JetMakeKey-Funktion.</a></p><p><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> wird in Windows Vista eingeführt.</p> | 
| <p>JET_bitIndexNestedTable 0x00020000</p> | <p>Wenn Sie dieses Flag angeben, wird der Index über mehrere mehrwertige Spalten aktualisiert, jedoch nur mit Werten desselben <strong>itagSequence.</strong></p><p>JET_bitIndexNestedTable wurde in Windows Vista eingeführt.</p> | 



**ulDensity**

Die prozentuale Dichte der anfänglichen Indexstruktur B+. Wenn Sie eine Zahl kleiner als 100 angeben, wird mehr Speicherplatz benötigt, um den Index anfänglich zu erstellen. Dies ermöglicht jedoch das zukünftige Wachstum des Indexes, wodurch eine interne Fragmentierung vermieden wird.

**lcid**

Der Gebietsschemabezeichner (LCID), der beim Normalisieren der Daten verwendet werden soll, wenn der JET_bitIndexUnicode Wert nicht im *grbit-Parameter* angegeben ist. Die LCID wirkt sich auf die Normalisierung aus, wenn sich der Index über Unicode-Spalten befindet.

**pidxunicode**

Ein Zeiger [](./jet-unicodeindex-structure.md) auf eine JET_UNICODEINDEX-Struktur, wenn der JET_bitIndexUnicode Wert im *grbit-Parameter* angegeben ist. Dadurch kann der Benutzer benutzerdefinierte Flags angeben, die während der Unicode-Normalisierung an die [LCMapString-Funktion](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) übergeben werden.

**cbVarSegMac**

Die maximale Länge (in Bytes) jeder Spalte, die im Index gespeichert werden soll, wenn der JET_bitIndexTupleLimits Wert nicht im *grbit-Parameter* angegeben ist.

Das Angeben des Werts 0 (null) für dieses Feld entspricht:

  - Angeben JET_cbPrimaryKeyMost für einen primären Index.

  - Angeben JET_cbSecondaryKeyMost für einen sekundären Index.

**ptuplelimits**

Ein Zeiger [](./jet-tuplelimits-structure.md) auf eine JET_TUPLELIMITS-Struktur, wenn der JET_bitIndexTupleLimits Wert im *grbit-Parameter* angegeben ist.

ptuplelimits wurde in Windows Server 2003 eingeführt.

**rgconditionalcolumn**

Ein optionaler Parameter für ein Array von [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) Strukturen, die zum Angeben der bedingten Spalten im Index verwendet werden.

**cConditionalColumn**

Die Anzahl der Strukturen im **Array rgconditionalcolumn.**

**Err**

Enthält den Rückgabecode zum Erstellen dieses Indexes.

**cbKeyMost**

Gibt die maximal zulässige Größe für Schlüssel im Index in Bytes an. Dieser Parameter wird ignoriert, wenn der JET_bitIndexKeyMost Wert nicht im *grbit-Parameter* angegeben ist. Wenn dieser Parameter auf 0 (null) festgelegt ist und JET_bitIndexKeyMost im *grbit-Parameter* angegeben ist, schlägt die aufrufende Funktion mit JET_err_InvalidDef fehl.

Die maximal unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255), was der maximalen Legacyschlüsselgröße entspricht.

Die maximale Schlüsselgröße hängt wie folgt von der Größe der Datenbankseite (JET_paramDatabasePageSize) ab:

  - Wenn JET_paramDatabasePageSize = 2048 ist, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Wenn JET_paramDatabasePageSize = 4096 ist, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Wenn JET_paramDatabasePageSize = 8192, dann JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

Die maximal unterstützte Schlüsselgröße für die Instanz kann auch aus dem JET_paramKeyMost Systemparameters gelesen werden.

**cbKeyMost** wurde in Windows Vista eingeführt.

### <a name="remarks"></a>Bemerkungen

ESE unterstützt die Indizierung über Schlüsselspalten, die mehrere Werte enthalten. Um dieses Feature verwenden zu können, muss die Spalte ein markierter Spaltentyp (JET_bitColumnTagged) sein, und sie muss gekennzeichnet werden, damit ihre mehreren Werte mit JET_bitColumnMultiValued indiziert werden. In Versionen von Windows vor Windows Vista werden nur für die erste mehrwertige Schlüsselspalte im Index die Werte im Index erweitert. Für alle anderen mehrwertigen und markierten Spalten werden nur die ersten Werte im Index erweitert.

Angenommen, die folgenden Zeilen sind in einer Tabelle vorhanden (Spalte Alpha ist nicht mehrwertig, während die Spalten Beta, Gamma und Delta mehrwertig sind), und ein Index wird als "+Alpha \\ 0+Beta \\ 0+Gamma \\ 0+Delta \\ 0 \\ 0" erstellt:


| <p>Alpha</p> | <p>Beta</p> | <p>Gamma</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />AZ<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>DAS</p> | <p>REGEN<br />SPANIEN</p> | <p>IN<br />FÄLLT</p> | 



Die fallenden Indextupel werden gespeichert:

{1,ABC,MNO,VWX}  
{1, WHI,MNO,VWX}  
{1,JKL,MNO,VWX}  
{2,THE,RAIN,IN}

Beachten Sie, dass {2,THE,SPANIEN,IN} nicht gespeichert ist, obwohl die Alphaspalte in der zweiten Zeile einen einzelnen mehrwertigen Wert aufzuweisen hat.

In Versionen von Windows, die mit Windows Vista beginnen, können alle mehrwertigen Spalten durch Angabe von JET_bitIndexCrossProduct im Index erweitert werden.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_ INDEXCREATE_W</strong> (Unicode) und <strong>JET_ INDEXCREATE_A</strong> (ANSI) implementiert.</p> | 



### <a name="see-also"></a>Siehe auch

[JET_COLTYP](./jet-coltyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
