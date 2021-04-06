---
description: 'Weitere Informationen finden Sie hier: JET_INDEXCREATE2 Struktur'
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
ms.openlocfilehash: ac0d9a40e159a8aa5054228d18e431cee8d0319f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960967"
---
# <a name="jet_indexcreate2-structure"></a>JET_INDEXCREATE2-Struktur


_**Gilt für:** Windows | Windows Server_

Die **JET_INDEXCREATE2** Struktur enthält die Informationen, die erforderlich sind, um einen Index über Daten in einer ESE-Datenbank (Extensible Storage Engine) zu erstellen. Die-Struktur wird von Funktionen wie z. b. [JetCreateIndex2](./jetcreateindex2-function.md)und in Strukturen wie [JET_TABLECREATE](./jet-tablecreate-structure.md) und [JET_TABLECREATE2](./jet-tablecreate2-structure.md)verwendet.

Die **JET_INDEXCREATE2** Struktur wurde mit dem Betriebssystem Windows 7 eingeführt.

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

Die Größe (in Bytes) dieser Struktur. Legen Sie diesen Member auf sizeof (JET_INDEXCREATE2) fest.

**szindexname**

Der Name des zu erstellenden Indexes.

Der Name muss die folgenden Bedingungen erfüllen:

  - Er sollte kleiner als JET_cbNameMost sein, ohne dass der abschließende NULL-Wert eingeschlossen wird.

  - Sie muss aus folgenden Zeichen bestehen: 0 (null) bis 9, a bis z, a bis z und alle anderen Interpunktions Zeichen mit Ausnahme von " \! ". (Ausrufezeichen), "," (Komma), " \[ " (öffnende eckige Klammer) und " \] " (schließende Klammer) – das heißt, die ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.

  - Er darf nicht mit einem Leerzeichen beginnen.

  - Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.

**szkey**

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die NULL-Werte getrennt ist.

Jedes Token hat das Format " \<direction-specifier\> \<column-name\> ", wobei "Direction-Specification" entweder "+" oder "-" ist. Beispielsweise indiziert ein **szkey** -Wert von "+ ABC \\ 0-DEF \\ 0 + ghi \\ 0" die drei Spalten "ABC" (in aufsteigender Reihenfolge), "Def" (in absteigender Reihenfolge) und "ghi" (in aufsteigender Reihenfolge). In der Programmiersprache C haben Zeichen folgen Literale einen impliziten **null** -Terminator, sodass die obige Zeichenfolge durch einen Double-NULL-Wert beendet wird.

Die Anzahl der in **szkey** angegebenen Spalten darf JET_ccolKeyMost (eine Versions abhängige Konstante) nicht überschreiten.

Mindestens eine Spalte muss in **szkey** benannt werden.

Veraltetes Verhalten: nach dem Double-NULL-Abschluss Zeichen ist es möglich, eine Sprach-ID (ein Wort, das an MAKELCID (langid, SORT_DEFAULT) übergeben wird) als Möglichkeit anzugeben, die LCID für den Index anzugeben. Es ist unzulässig, sowohl eine Sprachen-ID in **szkey** als auch eine LCID in [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) anzugeben (durch Festlegen von JET_bitIndexUnicode in *grbit*).

Veraltet: nach der Sprach-ID ist es möglich, **cbvarsegmac** als **UShort** -Datentyp zu übergeben. Das Verhalten ist nicht definiert, wenn der ushort-Wert sowohl in **szkey** als auch in der-Struktur fest **gelegt ist.**

**cbKey**

Die Länge (in Byte) von **szkey**, einschließlich der beiden abschließenden Nullen.

**grbit**

Eine Gruppe von Bits, die NULL oder mehr der Wert Optionen enthalten, die in der folgenden Tabelle aufgeführt sind.

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
<td><p>Doppelte Indexeinträge (Schlüssel) sind nicht zulässig. Dies wird erzwungen, wenn <a href="gg269288(v=exchg.10).md">jetupdate</a> aufgerufen wird, nicht wenn <a href="gg294137(v=exchg.10).md">jetsetcolumn</a> aufgerufen wird.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexPrimary</p></td>
<td><p>Der Index ist ein primärer Index (gruppierter Index). Jede Tabelle muss genau einen primären Index aufweisen. Wenn kein primärer Index explizit für eine Tabelle definiert wird, erstellt die Datenbank-Engine ihren eigenen primären Index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexDisallowNull</p></td>
<td><p>Keine der Spalten, für die der Index erstellt wird, kann einen <strong>null</strong> -Wert enthalten.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreNull</p></td>
<td><p>Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn alle indizierten Spalten <strong>null</strong>sind.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexIgnoreAnyNull</p></td>
<td><p>Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn eine der indizierten Spalten <strong>null</strong>ist.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreFirstNull</p></td>
<td><p>Fügen Sie keinen Index Eintrag für eine Zeile hinzu, wenn die erste indizierte Spalte <strong>null</strong>ist.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexLazyFlush</p></td>
<td><p>Gibt an, dass die Index Vorgänge verzögert protokolliert werden.</p>
<p>JET_bitIndexLazyFlush wirkt sich nicht auf die Faulheit von Datenaktualisierungen aus. Wenn der Indizierungs Vorgang durch die Beendigung des Prozesses unterbrochen wird, kann die Wiederherstellung der Datenbank dennoch in einen konsistenten Zustand versetzt werden, aber der Index ist möglicherweise nicht vorhanden.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexEmpty</p></td>
<td><p>Versuchen Sie nicht, den Index zu erstellen, da alle Einträge zu <strong>null</strong>ausgewertet werden. <strong>grbit</strong> Muss auch JET_bitIgnoreAnyNull angeben, wenn JET_bitIndexEmpty übermittelt wird. Dies ist eine Leistungsverbesserung. Wenn z. b. eine neue Spalte zu einer Tabelle hinzugefügt wird und dann ein Index für diese neu hinzugefügte Spalte erstellt wird, werden alle Datensätze in der Tabelle gescannt, auch wenn Sie nicht zum Index hinzugefügt werden. Durch angeben JET_bitIndexEmpty wird die Überprüfung der Tabelle ausgelassen, was möglicherweise sehr lange dauern kann.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnversioned</p></td>
<td><p>JET_bitIndexUnversioned bewirkt, dass die Indexerstellung für andere Transaktionen sichtbar ist. Normalerweise kann eine Sitzung in einer Transaktion einen Index Erstellungs Vorgang nicht in einer anderen Sitzung sehen. Dieses Flag kann nützlich sein, wenn eine andere Transaktion wahrscheinlich denselben Index erstellt. Die zweite Indexerstellung schlägt einfach fehl, anstatt potenziell viele unnötige Daten Bank Vorgänge zu verursachen. Die zweite Transaktion ist möglicherweise nicht in der Lage, den Index sofort zu verwenden. Der Index Erstellungs Vorgang muss beendet werden, bevor er verwendet werden kann. Die Sitzung darf sich zurzeit nicht in einer Transaktion befinden, um einen Index ohne Versionsinformationen zu erstellen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexSortNullsHigh</p></td>
<td><p>Die Angabe dieses Flags bewirkt, dass <strong>null</strong> -Werte nach den Daten für alle Spalten im Index sortiert werden.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnicode</p></td>
<td><p>Die Angabe dieses Flags wirkt sich auf die Interpretation des LCID/pidxunicde-Union-Felds in der Struktur aus. Das Festlegen des Bits bedeutet, dass das Feld pidxunicode tatsächlich auf eine <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> Struktur verweist. JET_bitIndexUnicode ist nicht erforderlich, um Unicode-Daten zu indizieren. Es ist nur erforderlich, um die Normalisierung von Unicode-Daten anzupassen.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexTuples</p></td>
<td><p>Gibt an, dass der Index ein Tupelindex ist. Eine Beschreibung eines tupelindexes finden Sie unter <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p>
<p>Der JET_bitIndexTuples Wert wurde im Betriebssystem Windows XP eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexTupleLimits</p></td>
<td><p>Die Angabe dieses Flags wirkt sich auf die Interpretation des Union <strong>-Felds cbvarsegmac/ptuplelimits</strong> in der Struktur aus. Das Festlegen dieses Bits bedeutet, dass das Feld " <strong>ptuplelimits</strong> " tatsächlich auf eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur verweist, um benutzerdefinierte tupelindexlimits zuzulassen (impliziert JET_bitIndexTuples).</p>
<p>Der <strong>JET_bitIndexTupleLimits</strong> Wert wurde im Betriebssystem Windows Server 2003 eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexCrossProduct<br />
0x00004000</p></td>
<td><p>Wenn dieses Flag für einen Index angegeben wird, der mehr als eine Schlüssel Spalte aufweist, die eine mehrwertige Spalte ist, führt dies dazu, dass für jedes Ergebnis eines Kreuz Produkts aller Werte in diesen Schlüssel Spalten ein Index Eintrag erstellt wird. Andernfalls hätte der Index nur einen Eintrag für jeden mehrwertigen in der signifikantesten Schlüssel Spalte, bei der es sich um eine mehrwertige Spalte handelt, und jede dieser Indexeinträge würde den ersten multiwert aus anderen Schlüssel Spalten verwenden, die mehrwertige Spalten sind.</p>
<p>Wenn Sie z. B. dieses Flag für einen Index über Spalte a mit den Werten &quot; rot &quot; und &quot; blau &quot; und over column B mit den Werten &quot; 1 &quot; und 2 angegeben &quot; &quot; haben, werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; rot &quot; , &quot; 2 &quot; ; &quot; blau &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 2 &quot; . Andernfalls werden die folgenden Indexeinträge erstellt: &quot; rot &quot; , &quot; 1 &quot; ; &quot; blau &quot; , &quot; 1 &quot; .</p>
<p>Der <strong>JET_bitIndexCrossProduct</strong> Wert wurde in Windows Vista eingeführt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexKeyMost<br />
0x00008000</p></td>
<td><p>Die Angabe dieses Flags bewirkt, dass der Index die maximale Schlüsselgröße verwendet, die im Feld <strong>cbkeymost</strong> in der-Struktur angegeben ist. Andernfalls wird der Index JET_cbKeyMost (255) als maximale Schlüsselgröße verwendet.</p>
<p>Der <strong>JET_bitIndexKeyMost</strong> Wert wurde in Windows Vista eingeführt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexDisallowTruncation<br />
0x00010000</p></td>
<td><p>Die Angabe dieses Flags führt dazu, dass jedes Update des Indexes, das zu einem abgeschnittene Schlüssel führt, mit dem JET_errKeyTruncated-Antwort Code fehlschlägt. Andernfalls werden Schlüssel automatisch abgeschnitten. Weitere Informationen zum Abschneiden von Schlüsseln finden Sie unter <a href="gg269329(v=exchg.10).md">jetmakekey</a>.</p>
<p>Der <strong>JET_bitIndexDisallowTruncation</strong> Wert wurde in Windows Vista eingeführt.</p></td>
</tr>
</tbody>
</table>


**uldensity**

Die prozentuale Dichte des ersten Index B +-Baums. Wenn Sie eine Zahl angeben, die kleiner als 100 ist, wird zum ersten Mal mehr Speicherplatz zum Erstellen des Indexes verwendet, jedoch kann das zukünftige Wachstum des Indexes vorhanden sein, sodass die interne Fragmentierung vermieden wird.

**lcid**

Der Gebiets Schema Bezeichner (LCID), der bei der Normalisierung der Daten verwendet werden soll, wenn der JET_bitIndexUnicode Wert nicht im *grbit* -Parameter angegeben wird. Die LCID wirkt sich auf die Normalisierung aus, wenn der Index über Unicode-Spalten ist.

**pidxunicode**

Ein Zeiger auf eine [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) Struktur, wenn der JET_bitIndexUnicode Wert im *grbit* -Parameter angegeben wird. Dies ermöglicht es dem Benutzer, benutzerdefinierte Flags anzugeben, die während der Unicode-Normalisierung an die [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) -Funktion übergeben werden.

**cbvarsegmac**

Die maximale Länge (in Byte) der einzelnen Spalten, die im Index gespeichert werden sollen, wenn der JET_bitIndexTupleLimits Wert nicht im *grbit* -Parameter angegeben wird.

Die Angabe eines Werts von 0 (null) für dieses Feld entspricht Folgendem:

  - Angeben von JET_cbPrimaryKeyMost für einen primären Index.

  - Angeben von JET_cbSecondaryKeyMost für einen sekundären Index.

**ptuplelimits**

Ein Zeiger auf eine [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur, wenn der JET_bitIndexTupleLimits Wert im *grbit* -Parameter angegeben wird.

**ptuplelimits** wurde in Windows Server 2003 eingeführt.

**rgconditionalcolumn**

Ein optionaler Parameter für ein Array von [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) -Strukturen, die verwendet werden, um die bedingten Spalten im Index anzugeben.

**cconditionalcolumn**

Die Anzahl der Strukturen im **rgconditionalcolumn** -Array.

**irre**

Enthält den Rückgabecode zum Erstellen dieses Indexes.

**cbkeymost**

Gibt die maximal zulässige Größe für Schlüssel im Index in Bytes an. Dieser Parameter wird ignoriert, wenn JET_bitIndexKeyMost nicht im *grbit* -Parameter angegeben ist. Wenn dieser Parameter auf 0 (null) festgelegt ist, und JET_bitIndexKeyMost im *grbit* -Member angegeben wird, schlägt die Aufruf Funktion mit JET_err_InvalidDef fehl.

Die unterstützte Mindestschlüsselgröße ist JET_cbKeyMostMin (255). Dies ist die maximale maximale Schlüsselgröße.

Die maximale Schlüsselgröße hängt von der Datenbankseiten Größe (JET_paramDatabasePageSize) wie folgt ab:

  - Wenn JET_paramDatabasePageSize = 2048, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost2KBytePage (500)

  - Wenn JET_paramDatabasePageSize = 4096, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost4KBytePage (1000)

  - Wenn JET_paramDatabasePageSize = 8192, dann JET_cbKeyMostMin (255) \< =  **cbkeymost** \< = JET_cbKeyMost8KBytePage (2000)

Die maximal unterstützte maximale Schlüsselgröße für die-Instanz kann auch aus dem JET_paramKeyMost System-Parameter gelesen werden.

**cbkeymost** wurde in Windows Vista eingeführt.

**pspacehints**

Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) -Struktur.

**pspacehints** wurde in Windows 7 eingeführt.

### <a name="remarks"></a>Bemerkungen

ESE unterstützt die Indizierung über Schlüssel Spalten, die mehrere Werte enthalten. Um dieses Feature verwenden zu können, muss es sich bei der Spalte um einen markierten Spaltentyp (JET_bitColumnTagged) handeln, und es muss gekennzeichnet werden, damit die verschiedenen Werte mit JET_bitColumnMultiValued indiziert werden. In Windows-Versionen vor Windows Vista werden die Werte nur für die erste mehrwertige Schlüssel Spalte im Index im Index erweitert. Für alle anderen mehrwertigen und markierten Spalten werden nur die ersten Werte im Index erweitert.

Angenommen, die folgenden Zeilen sind in einer Tabelle vorhanden (die Spalte Alpha ist nicht mehr wertig, während die Spalten Beta, Gamma und Delta mehr wertig sind), und ein Index wird als "+ Alpha \\ 0 + Beta \\ 0 + Gamma \\ 0 + Delta \\ 0 \\ 0" erstellt:

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
PQR<br />
Stu</p></td>
<td><p>Vwx<br />
YZ</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>Die</p></td>
<td><p>REGEN<br />
Spanien</p></td>
<td><p>IN<br />
Engpässen</p></td>
</tr>
</tbody>
</table>


Die folgenden indextupel werden gespeichert:

{1, ABC, MNO, vwx}  
{1, ghi, MNO, vwx}  
{1, JKL, MNO, vwx}  
{2,, Regen, in}

Beachten Sie, dass {2,, Spanien, in} nicht gespeichert wird, auch wenn die Alpha Spalte in der zweiten Zeile einen einzelnen multiwert hat.

In Windows-Versionen ab Windows Vista können alle mehrwertigen Spalten im Index erweitert werden, indem JET_bitIndexCrossProduct angegeben werden.

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
<td><p>Wird als <strong>JET_ INDEXCREATE2_W</strong> (Unicode) und <strong>JET_ INDEXCREATE2_A</strong> (ANSI) implementiert.</p></td>
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
[Jetsetcolumn](./jetsetcolumn-function.md)  
[Jetupdate](./jetupdate-function.md)
