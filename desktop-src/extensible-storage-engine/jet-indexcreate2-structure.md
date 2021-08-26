---
description: 'Weitere Informationen zu: JET_INDEXCREATE2-Struktur'
title: JET_INDEXCREATE2-Struktur
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
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
ms.openlocfilehash: fe474bad552ca816ec9f0f5419cac21923b1f10f9d711812ee5aab749a027aba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016920"
---
# <a name="jet_indexcreate2-structure"></a>JET_INDEXCREATE2-Struktur


_**Gilt für:** Windows | Windows Server_

Die **JET_INDEXCREATE2-Struktur** enthält die Informationen, die erforderlich sind, um einen Index für Daten in einer ESE-Datenbank (Extensible Storage Engine) zu erstellen. Die -Struktur wird von Funktionen wie [JetCreateIndex2](./jetcreateindex2-function.md)und in Strukturen wie [JET_TABLECREATE](./jet-tablecreate-structure.md) und [JET_TABLECREATE2](./jet-tablecreate2-structure.md)verwendet.

Die **JET_INDEXCREATE2-Struktur** wurde im Betriebssystem Windows 7 eingeführt.

```cpp
typedef struct tagJET_INDEXCREATE2 {
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
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe (in Bytes) dieser Struktur. Legen Sie diesen Member auf sizeof( JET_INDEXCREATE2 ) fest.

**szIndexName**

Der Name des zu erstellende Indexes.

Der Name sollte die folgenden Bedingungen erfüllen:

  - Er sollte kleiner als JET_cbNameMost sein, ohne den abschließenden NULL-Wert zu enthalten.

  - Sie muss aus den folgenden Zeichen bestehen: 0 (null) bis 9, A bis Z, a bis z und alle anderen Interpunktion außer " \! " " (Ausrufezeichen), "," (Komma), \[ " " (öffnende eckige Klammer) und \] " (schließende Klammer) – das heißt, ASCII-Zeichen 0x20, 0x22 durch 0x2d, 0x2f durch 0x5a, 0x5c und 0x5d durch 0x7f.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

**szKey**

Ein Zeiger auf eine doppelt auf NULL endende Zeichenfolge von durch NULL getrennten Token.

Jedes Token hat das Format \<direction-specifier\> \<column-name\> "", wobei direction-specification entweder "+" oder "-" ist. Beispielsweise indiziert ein **szKey** von "+abc \\ 0-def \\ 0+ whi \\ 0" die drei Spalten "abc" (in aufsteigender Reihenfolge), "def" (in absteigender Reihenfolge) und " whi" (in aufsteigender Reihenfolge). In der Programmiersprache C verfügen Zeichenfolgenliterale über ein implizites NULL-Abschlusszeichen, sodass die obige Zeichenfolge durch einen doppelten NULL-Wert beendet wird. 

Die Anzahl der in **szKey** angegebenen Spalten darf JET_ccolKeyMost (eine versionsabhängige Konstante) nicht überschreiten.

Mindestens eine Spalte muss in **szKey** benannt werden.

Veraltetes Verhalten: Nach dem Double-NULL-Abschlusszeichen kann eine Sprach-ID (ein WORD, das an MAKELCID( langid, SORT_DEFAULT ) übergeben wird) als Möglichkeit zum Angeben der LCID für den Index angegeben werden. Es ist unzulässig, sowohl eine Sprach-ID in **szKey** als auch eine LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) anzugeben (indem JET_bitIndexUnicode in *grbit* festgelegt wird).

Veraltet: Nach der Sprach-ID ist es möglich, **cbVarSegMac** als **USHORT-Datentyp** zu übergeben. Das Verhalten ist nicht definiert, wenn USHORT sowohl in **szKey** als auch **cbVarSegMac** in der -Struktur festgelegt ist.

**cbKey**

Die Länge von **szKey** in Bytes, einschließlich der beiden abschließenden NULL-Werte.

**grbit**

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Wertoptionen enthalten.

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
<td><p>JET_bitIndexUnique</p></td>
<td><p>Doppelte Indexeinträge (Schlüssel) sind nicht zulässig. Dies wird erzwungen, wenn <a href="gg269288(v=exchg.10).md">JetUpdate</a> aufgerufen wird, nicht, wenn <a href="gg294137(v=exchg.10).md">JetSetColumn</a> aufgerufen wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexPrimary</p></td>
<td><p>Der Index ist ein primärer (gruppierter) Index. Jede Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index explizit für eine Tabelle definiert ist, erstellt die Datenbank-Engine einen eigenen primären Index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexDisallowNull</p></td>
<td><p>Keine der Spalten, über die der Index erstellt wird, darf einen <strong>NULL-Wert</strong> enthalten.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreNull</p></td>
<td><p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn alle indizierten Spalten <strong>NULL</strong>sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexIgnoreAnyNull</p></td>
<td><p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn eine der indizierten Spalten <strong>NULL</strong>ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreFirstNull</p></td>
<td><p>Fügen Sie keinen Indexeintrag für eine Zeile hinzu, wenn die erste indizierte Spalte <strong>NULL</strong>ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexLazyFlush</p></td>
<td><p>Gibt an, dass die Indexvorgänge verzögert protokolliert werden.</p>
<p>JET_bitIndexLazyFlush wirkt sich nicht auf die Verzögertheit von Datenupdates aus. Wenn der Indizierungsvorgang durch Die Prozessbeendigung unterbrochen wird, kann die Soft Recovery die Datenbank weiterhin in einen konsistenten Zustand bringen, aber der Index ist möglicherweise nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexEmpty</p></td>
<td><p>Versuchen Sie nicht, den Index zu erstellen, da alle Einträge als <strong>NULL</strong>ausgewertet würden. <strong>grbit</strong> MUSS auch JET_bitIgnoreAnyNull angeben, wenn JET_bitIndexEmpty übergeben wird. Dies ist eine Leistungsverbesserung. Wenn z. B. einer Tabelle eine neue Spalte hinzugefügt wird und dann ein Index für diese neu hinzugefügte Spalte erstellt wird, werden alle Datensätze in der Tabelle überprüft, obwohl sie dem Index nicht hinzugefügt werden. Wenn Sie JET_bitIndexEmpty angeben, wird die Überprüfung der Tabelle übersprungen, was möglicherweise viel Zeit in Anspruch nehmen kann.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnversioned</p></td>
<td><p>JET_bitIndexUnversioned bewirkt, dass die Indexerstellung für andere Transaktionen sichtbar ist. Normalerweise kann eine Sitzung in einer Transaktion keinen Indexerstellungsvorgang in einer anderen Sitzung sehen. Dieses Flag kann nützlich sein, wenn eine andere Transaktion wahrscheinlich denselben Index erstellt. Die zweite Indexerstellung schlägt einfach fehl, anstatt potenziell viele unnötige Datenbankvorgänge zu verursachen. Die zweite Transaktion kann den Index möglicherweise nicht sofort verwenden. Der Indexerstellungsvorgang muss abgeschlossen werden, bevor er verwendet werden kann. Die Sitzung darf sich derzeit nicht in einer Transaktion befinden, um einen Index ohne Versionsinformationen zu erstellen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexSortNullsHigh</p></td>
<td><p>Wenn Sie dieses Flag angeben, werden <strong>NULL-Werte</strong> nach Daten für alle Spalten im Index sortiert.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnicode</p></td>
<td><p>Die Angabe dieses Flags wirkt sich auf die Interpretation des lcid/pidxunicde union-Felds in der Struktur aus. Das Festlegen des Bits bedeutet, dass das Pidxunicode-Feld tatsächlich auf eine <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur zeigt. JET_bitIndexUnicode ist zum Indizierung von Unicode-Daten nicht erforderlich. Es ist nur erforderlich, um die Normalisierung von Unicode-Daten anzupassen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexTuples</p></td>
<td><p>Gibt an, dass der Index ein Tupelindex ist. Eine Beschreibung eines Tupelindex finden Sie unter <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS.</a></p>
<p>Der JET_bitIndexTuples Wert wurde im betriebssystem Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexTupleLimits</p></td>
<td><p>Die Angabe dieses Flags wirkt sich auf die Interpretation des union-Felds <strong>cbVarSegMac/ptuplelimits</strong> in der -Struktur aus. Das Festlegen dieses Bits bedeutet, dass das <strong>Feld ptuplelimits</strong> tatsächlich auf eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> -Struktur zeigt, um benutzerdefinierte Tupelindexgrenzwerte zuzulassen (impliziert JET_bitIndexTuples).</p>
<p>Der <strong>JET_bitIndexTupleLimits</strong> Wert wurde im Betriebssystem Windows Server 2003 eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexCrossProduct<br />
0x00004000</p></td>
<td><p>Wenn Sie dieses Flag für einen Index angeben, der über mehrere Schlüsselspalten verfügt, bei denen es sich um eine mehrwertige Spalte handelt, wird für jedes Ergebnis eines Kreuzprodukts aller Werte in diesen Schlüsselspalten ein Indexeintrag erstellt. Andernfalls hätte der Index nur einen Eintrag für jede mehrwertige Spalte in der wichtigsten Schlüsselspalte, bei der es sich um eine mehrwertige Spalte handelt, und jeder dieser Indexeinträge würde den ersten mehrwertigen Wert aus allen anderen Schlüsselspalten verwenden, bei denen es sich um mehrwertige Spalten handelt.</p>
<p>Wenn Sie z. B. dieses Flag für einen Index über Spalte A mit den Werten rot und blau und für Spalte B mit &quot; &quot; den Werten &quot; &quot; 1 und 2 angegeben &quot; &quot; &quot; &quot; haben, werden die folgenden Indexeinträge erstellt: &quot; rot , &quot; &quot; 1 &quot; ; &quot; rot &quot; , &quot; 2 &quot; ; &quot; blue &quot; , &quot; 1 &quot; ; &quot; blau, &quot; &quot; 2 &quot; . Andernfalls werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; blau, &quot; &quot; 1 &quot; .</p>
<p>Der <strong>JET_bitIndexCrossProduct</strong> Wert wurde in Windows Vista eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexKeyMost<br />
0x00008000</p></td>
<td><p>Wenn Sie dieses Flag angeben, verwendet der Index die maximale Schlüsselgröße, die im feld <strong>cbKeyMost</strong> in der -Struktur angegeben ist. Andernfalls verwendet der Index JET_cbKeyMost (255) als maximale Schlüsselgröße.</p>
<p>Der <strong>JET_bitIndexKeyMost</strong> Wert wurde in Windows Vista eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexDisallowTruncation<br />
0x00010000</p></td>
<td><p>Die Angabe dieses Flags führt dazu, dass jede Aktualisierung des Indexes, die dazu führen würde, dass ein abgeschnittener Schlüssel mit dem JET_errKeyTruncated Antwortcode fehlschlägt. Andernfalls werden Schlüssel automatisch abgeschnitten. Weitere Informationen zum Abschneiden von Schlüsseln finden Sie unter <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p>
<p>Der <strong>JET_bitIndexDisallowTruncation</strong> Wert wurde in Windows Vista eingeführt.</p></td>
</tr>
</tbody>
</table>


**ulDensity**

Die prozentuale Dichte der anfänglichen Indexstruktur B+. Wenn Sie eine Zahl kleiner als 100 angeben, wird mehr Speicherplatz benötigt, um den Index anfänglich zu erstellen. Dies ermöglicht jedoch das zukünftige Wachstum des Indexes, wodurch eine interne Fragmentierung vermieden wird.

**lcid**

Der Gebietsschemabezeichner (LCID), der beim Normalisieren der Daten verwendet werden soll, wenn der JET_bitIndexUnicode Wert nicht im *grbit-Parameter* angegeben ist. Die LCID wirkt sich auf die Normalisierung aus, wenn sich der Index über Unicode-Spalten befindet.

**pidxunicode**

Ein Zeiger [](./jet-unicodeindex-structure.md) auf eine JET_UNICODEINDEX-Struktur, wenn der JET_bitIndexUnicode Wert im *grbit-Parameter* angegeben ist. Dadurch kann der Benutzer benutzerdefinierte Flags angeben, die während der Unicode-Normalisierung an die [LCMapString-Funktion](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) übergeben werden.

**cbVarSegMac**

Die maximale Länge (in Bytes) jeder Spalte, die im Index gespeichert werden soll, wenn der JET_bitIndexTupleLimits Wert nicht im *grbit-Parameter* angegeben ist.

Das Angeben des Werts 0 (null) für dieses Feld entspricht folgendem Wert:

  - Angeben JET_cbPrimaryKeyMost für einen primären Index.

  - Angeben JET_cbSecondaryKeyMost für einen sekundären Index.

**ptuplelimits**

Ein Zeiger [](./jet-tuplelimits-structure.md) auf eine JET_TUPLELIMITS-Struktur, wenn der JET_bitIndexTupleLimits Wert im *grbit-Parameter* angegeben ist.

**ptuplelimits** wurde in Windows Server 2003 eingeführt.

**rgconditionalcolumn**

Ein optionaler Parameter für ein Array von [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) Strukturen, die zum Angeben der bedingten Spalten im Index verwendet werden.

**cConditionalColumn**

Die Anzahl der Strukturen im **Array rgconditionalcolumn.**

**Err**

Enthält den Rückgabecode zum Erstellen dieses Indexes.

**cbKeyMost**

Gibt die maximal zulässige Größe für Schlüssel im Index in Bytes an. Dieser Parameter wird ignoriert, wenn JET_bitIndexKeyMost nicht im *grbit-Parameter* angegeben ist. Wenn dieser Parameter auf 0 (null) festgelegt ist und JET_bitIndexKeyMost im *grbit-Member* angegeben ist, schlägt die aufrufende Funktion mit JET_err_InvalidDef fehl.

Die maximal unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255), was der maximalen Legacyschlüsselgröße entspricht.

Die maximale Schlüsselgröße hängt wie folgt von der Größe der Datenbankseite (JET_paramDatabasePageSize) ab:

  - Wenn JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Wenn JET_paramDatabasePageSize = 4096 ist, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Wenn JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

Die maximal unterstützte maximale Schlüsselgröße für die Instanz kann auch aus dem JET_paramKeyMost Systemparameter gelesen werden.

**cbKeyMost** wurde in Windows Vista eingeführt.

**pSpacehints**

Ein Zeiger [](./jet-spacehints-structure.md) auf eine JET_SPACEHINTS-Struktur.

**pSpacehints** wurde in Windows 7 eingeführt.

### <a name="remarks"></a>Hinweise

ESE unterstützt die Indizierung über Schlüsselspalten, die mehrere Werte enthalten. Um dieses Feature verwenden zu können, muss die Spalte ein markierter Spaltentyp (JET_bitColumnTagged) sein, und sie muss gekennzeichnet werden, damit ihre mehreren Werte mit JET_bitColumnMultiValued indiziert werden. In Versionen von Windows vor Windows Vista werden nur in der ersten mehrwertigen Schlüsselspalte im Index die Werte im Index erweitert. Für alle anderen mehrwertigen und markierten Spalten werden nur die ersten Werte im Index erweitert.

Angenommen, die folgenden Zeilen sind in einer Tabelle vorhanden (Spalte Alpha ist nicht mehrwertig, während die Spalten Beta, Gamma und Delta mehrwertig sind), und ein Index wird als "+Alpha \\ 0+Beta \\ 0+Gamma \\ 0+Delta \\ 0 \\ 0" erstellt:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Alpha</p></th>
<th><p>Beta</p></th>
<th><p>Gamma</p></th>
<th><p>Delta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>ABC<br />
GHI<br />
JKL</p></td>
<td><p>MNO<br />
Az<br />
Stu</p></td>
<td><p>VWX<br />
Yz</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>das</p></td>
<td><p>REGEN<br />
Spanien</p></td>
<td><p>IN<br />
Fällt</p></td>
</tr>
</tbody>
</table>


Die folgenden Indextupel werden gespeichert:

{1,ABC,MNO,VWX}  
{1, WHI,MNO,VWX}  
{1,JKL,MNO,VWX}  
{2,THE,RAIN,IN}

Beachten Sie, dass {2,THE,SPANIEN,IN} nicht gespeichert ist, obwohl die Alphaspalte in der zweiten Zeile einen einzelnen mehrwertigen Wert aufzuweisen hat.

In Versionen von Windows, die mit Windows Vista beginnen, können alle mehrwertigen Spalten im Index durch Angabe von JET_bitIndexCrossProduct erweitert werden.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementiert als <strong>JET_ INDEXCREATE2_W</strong> (Unicode) und <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
