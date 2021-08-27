---
description: 'Weitere Informationen zu: JET_INDEXCREATE-Struktur'
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
ms.openlocfilehash: 31b6b72cba336e3f7251bacfb1836673086ba9c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467627"
---
# <a name="jet_indexcreate-structure"></a>JET_INDEXCREATE-Struktur


_**Gilt für:** Windows | Windows Server_

Die **JET_INDEXCREATE-Struktur** enthält die Informationen, die zum Erstellen eines Indexes für Daten in einer ESE-Datenbank (Extensible Storage Engine) erforderlich sind. Die -Struktur wird von Funktionen wie [JetCreateIndex2](./jetcreateindex2-function.md)und in Strukturen wie [JET_TABLECREATE](./jet-tablecreate-structure.md) und [JET_TABLECREATE2](./jet-tablecreate2-structure.md)verwendet.

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

Der Name des zu erstellende Indexes.

Der Name des Indexes muss die folgenden Bedingungen erfüllen:

  - Er muss kleiner als JET_cbNameMost sein, ohne den abschließenden NULL-Wert zu enthalten.

  - Sie muss aus den folgenden Zeichen bestehen: 0 (null) bis 9, A bis Z, a bis z und alle anderen Interpunktion außer " \! " (Ausrufezeichen), "," (Komma), \[ " " (öffnende eckige Klammer) und \] " (schließende Klammer) – das heißt, ASCII-Zeichen 0x20, 0x22 durch 0x2d, 0x2f durch 0x5a, 0x5c, 0x5d durch 0x7f.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss aus mindestens einem Nichtbereichszeichen bestehen.

**szKey**

Ein Zeiger auf eine doppelt auf NULL endende Zeichenfolge von Token mit NULL-Trennzeichen.

Jedes Token hat das Format \<direction-specifier\> \<column-name\> "", wobei direction-specification entweder "+" oder "-" ist. Beispielsweise indiziert ein **szKey** von "+abc \\ 0-def \\ 0+ whi \\ 0" die drei Spalten "abc" (in aufsteigender Reihenfolge), "def" (in absteigender Reihenfolge) und " whi" (in aufsteigender Reihenfolge). In der Programmiersprache C verfügen Zeichenfolgenliterale über ein implizites **NULL-Abschlusszeichen.** daher wird die obige Zeichenfolge mit einem Double-NULL-Wert beendet.

Die Anzahl der in **szKey** angegebenen Spalten darf den Wert von **JET_ccolKeyMost** (eine versionsabhängige Konstante) nicht überschreiten.

Mindestens eine Spalte muss in **szKey** benannt werden.

Veraltetes Verhalten: Nach dem Double-NULL-Abschlusszeichen kann eine Sprach-ID (ein WORD, das an MAKELCID( langid, SORT_DEFAULT ) übergeben wird) als Möglichkeit zum Angeben der LCID für den Index angegeben werden. Es ist unzulässig, sowohl eine Sprach-ID in **szKey** als auch eine LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) anzugeben (indem JET_bitIndexUnicode in *grbit* festgelegt wird).

Veraltet: Nach der Sprach-ID ist es möglich, **cbVarSegMac** als USHORT zu übergeben. Das Verhalten ist nicht definiert, wenn USHORT sowohl in **szKey** als auch **cbVarSegMac** in der -Struktur festgelegt ist.

**cbKey**

Die Länge von **szKey** in Bytes, einschließlich der beiden abschließenden NULL-Werte.

**grbit**

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Werte enthält.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>Doppelte Indexeinträge (Schlüssel) sind nicht zulässig. Dies wird erzwungen, wenn <a href="gg269288(v=exchg.10).md">JetUpdate</a> aufgerufen wird, nicht, wenn <a href="gg294137(v=exchg.10).md">JetSetColumn</a> aufgerufen wird.</p> | 
| <p>JET_bitIndexPrimary</p> | <p>Der Index ist ein primärer (gruppierter) Index. Jede Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index explizit für eine Tabelle definiert ist, erstellt die Datenbank-Engine einen eigenen primären Index.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Keine der Spalten, über die der Index erstellt wird, kann einen <strong>NULL-Wert</strong> enthalten.</p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn alle indizierten Spalten <strong>NULL</strong>sind.</p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn eine der indizierten Spalten <strong>NULL</strong>ist.</p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn die erste indizierte Spalte <strong>NULL</strong>ist.</p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>Indexvorgänge werden verzögert protokolliert.</p><p>JET_bitIndexLazyFlush wirkt sich nicht auf die Verzögertheit von Datenupdates aus. Wenn der Indizierungsvorgang durch die Prozessbeendigung unterbrochen wird, kann die Soft Recovery die Datenbank weiterhin in einen konsistenten Zustand bringen, aber der Index ist möglicherweise nicht vorhanden.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>Versuchen Sie nicht, den Index zu erstellen, da alle Einträge als <strong>NULL</strong>ausgewertet würden. <strong>grbit</strong> muss auch JET_bitIgnoreAnyNull angeben, wenn JET_bitIndexEmpty übergeben wird. Dies ist eine Leistungsverbesserung. Wenn einer Tabelle beispielsweise eine neue Spalte hinzugefügt wird, wird ein Index für diese neu hinzugefügte Spalte erstellt, und alle Datensätze in der Tabelle werden überprüft, obwohl sie dem Index nicht hinzugefügt werden. Wenn Sie JET_bitIndexEmpty angeben, wird die Überprüfung der Tabelle übersprungen, was möglicherweise viel Zeit in Anspruch nehmen kann.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>Bewirkt, dass die Indexerstellung für andere Transaktionen sichtbar ist. In der Regel kann eine Sitzung in einer Transaktion keinen Indexerstellungsvorgang in einer anderen Sitzung sehen. Dieses Flag kann nützlich sein, wenn eine andere Transaktion wahrscheinlich denselben Index erstellt. Die zweite Indexerstellung schlägt fehl, anstatt potenziell viele unnötige Datenbankvorgänge zu verursachen. Die zweite Transaktion kann den Index möglicherweise nicht sofort verwenden. Der Indexerstellungsvorgang muss abgeschlossen werden, bevor er verwendet werden kann. Die Sitzung darf sich derzeit nicht in einer Transaktion befinden, um einen Index ohne Versionsinformationen zu erstellen.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>Wenn Sie dieses Flag angeben, werden <strong>NULL-Werte</strong> nach Daten für alle Spalten im Index sortiert.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>Die Angabe dieses Flags wirkt sich auf die Interpretation des lcid/pidxunicde union-Felds in der Struktur aus. Das Festlegen des Bits bedeutet, dass das <strong>Pidxunicode-Feld</strong> tatsächlich auf eine <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX-Struktur</a> zeigt. JET_bitIndexUnicode ist zum Indizierung von Unicode-Daten nicht erforderlich. Es wird nur verwendet, um die Normalisierung von Unicode-Daten anzupassen.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Gibt an, dass der Index ein Tupelindex ist. Eine Beschreibung eines Tupelindex finden Sie unter <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS.</a></p><p>JET_bitIndexTuples wurde im betriebssystem Windows XP eingeführt.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>Die Angabe dieses Flags wirkt sich auf die Interpretation des union-Felds <strong>cbVarSegMac/ptuplelimits</strong> in der -Struktur aus. Das Festlegen dieses Bits bedeutet, dass das <strong>Feld ptuplelimits</strong> tatsächlich auf eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> -Struktur zeigt, um benutzerdefinierte Tupelindexgrenzwerte zuzulassen (impliziert JET_bitIndexTuples).</p><p>JET_bitIndexTupleLimits wurde im Betriebssystem Windows Server 2003 eingeführt.</p> | 
| <p>JET_bitIndexCrossProduct 0x00004000</p> | <p>Wenn Sie dieses Flag für einen Index angeben, der mehr als eine Schlüsselspalte enthält, bei der es sich um eine mehrwertige Spalte handelt, wird für jedes Ergebnis eines Kreuzprodukts aller Werte in diesen Schlüsselspalten ein Indexeintrag erstellt. Andernfalls hätte der Index nur einen Eintrag für jede mehrwertige Spalte in der wichtigsten Schlüsselspalte, bei der es sich um eine mehrwertige Spalte handelt, und jeder dieser Indexeinträge würde den ersten Mehrwert aus allen anderen Schlüsselspalten verwenden, bei denen es sich um mehrwertige Spalten handelt.</p><p>Wenn Sie dieses Flag beispielsweise für einen Index über Spalte A mit den Werten "red" und "blue" und für Spalte B mit den Werten "1" und "2" angegeben haben, werden die folgenden Indexeinträge erstellt: "red", "1"; "red", "2"; "blue", "1"; "blue", "2". Andernfalls werden die folgenden Indexeinträge erstellt: "red", "1"; "blue", "1".</p><p>JET_bitIndexCrossProduct wurde im Betriebssystem Windows Vista eingeführt.</p> | 
| <p>JET_bitIndexKeyMost 0x00008000</p> | <p>Wenn Sie dieses Flag angeben, verwendet der Index die maximale Schlüsselgröße, die im feld <strong>cbKeyMost</strong> in der -Struktur angegeben ist. Andernfalls verwendet der Index JET_cbKeyMost (255) als maximale Schlüsselgröße.</p><p>JET_bitIndexKeyMost wurde in Windows Vista eingeführt.</p> | 
| <p>JET_bitIndexDisallowTruncation 0x00010000</p> | <p>Die Angabe dieses Flags führt dazu, dass bei jeder Aktualisierung des Indexes, die dazu führen würde, dass ein abgeschnittener Schlüssel mit JET_errKeyTruncated fehlschlägt. Andernfalls werden Schlüssel automatisch abgeschnitten. Weitere Informationen zum Abschneiden von Schlüsseln finden Sie in der <a href="gg269329(v=exchg.10).md">JetMakeKey-Funktion.</a></p><p><strong>Windows Vista: JET_bitIndexDisallowTruncation</strong> wird in Windows Vista eingeführt.</p> | 
| <p>JET_bitIndexNestedTable 0x00020000</p> | <p>Die Angabe dieses Flags führt dazu, dass der Index über mehrere mehrwertige Spalten aktualisiert wird, jedoch nur mit Werten desselben <strong>ItagSequence-Werts.</strong></p><p>JET_bitIndexNestedTable wurde in Windows Vista eingeführt.</p> | 



**ulDensity**

Die Prozentuale Dichte der anfänglichen B+-Indexstruktur. Die Angabe einer Zahl unter 100 verbraucht zunächst mehr Speicherplatz zum Erstellen des Indexes, ermöglicht jedoch eine zukünftige Verdrtung des Indexes, wodurch eine interne Fragmentierung vermieden wird.

**lcid**

Der Locale Identifier (LCID), der beim Normalisieren der Daten verwendet werden soll, wenn der JET_bitIndexUnicode im *grbit-Parameter nicht angegeben* ist. Die LCID wirkt sich auf die Normalisierung aus, wenn sich der Index über Unicode-Spalten befindet.

**pidxunicode**

Ein Zeiger auf [](./jet-unicodeindex-structure.md) eine JET_UNICODEINDEX-Struktur, wenn der JET_bitIndexUnicode wert im *grbit-Parameter angegeben* ist. Dadurch kann der Benutzer benutzerdefinierte Flags angeben, die während der Unicode-Normalisierung an die [LCMapString-Funktion](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) übergeben werden.

**cbVarSegMac**

Die maximale Länge jeder Spalte in Byte, die im Index gespeichert werden soll, wenn der JET_bitIndexTupleLimits im *grbit-Parameter nicht angegeben* ist.

Die Angabe eines Werts von 0 (null) für dieses Feld entspricht Folgendem:

  - Angeben JET_cbPrimaryKeyMost für einen primären Index.

  - Angeben JET_cbSecondaryKeyMost für einen sekundären Index.

**ptuplelimits**

Ein Zeiger auf [eine](./jet-tuplelimits-structure.md) JET_TUPLELIMITS-Struktur, JET_bitIndexTupleLimits wert im *grbit-Parameter angegeben* ist.

ptuplelimits wurde in Windows Server 2003 eingeführt.

**rgconditionalcolumn**

Ein optionaler Parameter [](./jet-conditionalcolumn-structure.md) für ein Array JET_CONDITIONALCOLUMN Strukturen, die verwendet werden, um die bedingten Spalten im Index anzugeben.

**cConditionalColumn**

Die Anzahl der Strukturen im **Array rgconditionalcolumn.**

**Err**

Enthält den Rückgabecode zum Erstellen dieses Indexes.

**cbKeyMost**

Gibt die maximal zulässige Größe für Schlüssel im Index in Bytes an. Dieser Parameter wird ignoriert, wenn JET_bitIndexKeyMost wert nicht im *grbit-Parameter angegeben* ist. Wenn dieser Parameter auf 0 (null) festgelegt ist und JET_bitIndexKeyMost im *grbit-Parameter* angegeben ist, kann die aufrufende Funktion nicht JET_err_InvalidDef.

Die unterstützte maximale Mindestschlüsselgröße beträgt JET_cbKeyMostMin (255). Dies ist die maximale Legacyschlüsselgröße.

Die maximale Schlüsselgröße hängt wie folgt von der Datenbankseitengröße (JET_paramDatabasePageSize ab:

  - Wenn JET_paramDatabasePageSize = 2048 ist, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Wenn JET_paramDatabasePageSize = 4096 ist, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Wenn JET_paramDatabasePageSize = 8192 ist, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

Die maximal unterstützte Schlüsselgröße für die Instanz kann auch aus dem JET_paramKeyMost gelesen werden.

**cbKeyMost** wurde in Windows Vista eingeführt.

### <a name="remarks"></a>Hinweise

ESE unterstützt die Indizierung über Schlüsselspalten, die mehrere Werte enthalten. Um dieses Feature verwenden zu können, muss die Spalte ein mit Tags versehener Spaltentyp (JET_bitColumnTagged) sein, und sie muss gekennzeichnet sein, damit ihre mehreren Werte mit der JET_bitColumnMultiValued. In Versionen von Windows vor Windows Vista werden die Werte nur für die erste mehrwertige Schlüsselspalte im Index erweitert. Für alle anderen mehrwertigen und markierten Spalten werden nur die ersten Werte im Index erweitert.

Angenommen, die folgenden Zeilen sind in einer Tabelle vorhanden (die Spalte Alpha ist nicht mehrwertigen, während die Spalten Beta, Gamma und Delta mehrwertigen sind), und ein Index wird als "+Alpha \\ 0+Beta \\ 0+Gamma \\ 0+Delta \\ 0 \\ 0" erstellt:


| <p>Alpha</p> | <p>Beta</p> | <p>Gamma</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />AZ<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>DAS</p> | <p>REGEN<br />SPANIEN</p> | <p>IN<br />FÄLLT</p> | 



Die fallenden Index-Tupel werden gespeichert:

{1,ABC,MNO,VWX}  
{1,OMETR,MNO,VWX}  
{1,JKL,MNO,VWX}  
{2,THE,RAIN,IN}

Beachten Sie, dass {2,THE,SPANIEN,IN} nicht gespeichert wird, obwohl die Alpha -Spalte in der zweiten Zeile einen einzelnen Mehrwert auf hat.

In Versionen von Windows ab Windows Vista können alle mehrwertigen Spalten im Index erweitert werden, indem sie JET_bitIndexCrossProduct.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_ INDEXCREATE_W</strong> (Unicode) und JET_ INDEXCREATE_A (ANSI) implementiert. <strong></strong></p> | 



### <a name="see-also"></a>Weitere Informationen

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
