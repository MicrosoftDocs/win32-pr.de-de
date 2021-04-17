---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE Struktur'
title: JET_OPENTEMPORARYTABLE Struktur
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
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
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345858"
---
# <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE Struktur

Die **JET_OPENTEMPORARYTABLE** -Struktur enthält eine leicht erweiterbare Auflistung von Parametern für die **JET_OPENTEMPORARYTABLE** -Funktion. Diese Struktur ist die temporäre Tabelle, die der [JET_TABLECREATE](./jet-tablecreate-structure.md) Struktur entspricht.

**Windows Vista:** Die **JET_OPENTEMPORARYTABLE** Struktur wird in Windows Vista eingeführt.

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a>Member

**cbStruct**

Die Größe dieser-Struktur in Bytes (für zukünftige Erweiterungen). Er muss auf sizeof (JET_TABLECREATE) in Bytes festgelegt werden.

**prgcolumndef**

Spaltendefinitionen für die Spalten, die in der temporären Tabelle erstellt werden.

**Wichtige** Einschränkungen gelten für die Spalten Definitions Optionen, die für eine temporäre Tabelle verwendet werden. Weitere Informationen finden Sie im Abschnitt Hinweise.

Zusätzlich zu den üblichen Spalten Definitions Optionen können auch keine oder mehrere der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.

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
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Die Sortierreihenfolge der Schlüssel Spalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein. Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Die Spalte ist eine Schlüssel Spalte für die temporäre Tabelle.</p>
<p>Die Reihenfolge der Spaltendefinitionen, bei denen diese Option im Eingabe Array angegeben ist, bestimmt die Rangfolge der einzelnen Schlüssel Spalten für die temporäre Tabelle. Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüssel Spalte usw. Wenn mehr Schlüssel Spalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht supportablen Schlüssel Spalten ignoriert.</p></td>
</tr>
</tbody>
</table>


**CColumn**

Siehe *prgcolumndef*.

**pidxunicode**

Die Gebiets Schema-ID und normalisierungs Flags, die verwendet werden, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen.

Wenn dieser Parameter nicht vorhanden ist und der *LCID* -Parameter nicht vorhanden ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüssel Spalten in der temporären Tabelle zu vergleichen. Die Standard-LCID ist das US-englische Gebiets Schema.

Wenn dieser Parameter nicht vorhanden ist, werden die standardnormalisierungs-Flags verwendet, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen. Die standardnormalisierungs-Flags lauten: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

**grbit**

Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.

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
<td><p>JET_bitTTIndexed</p></td>
<td><p>Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> für die Suche nach Datensätzen nach Index Schlüssel zuzulassen.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUnique</p></td>
<td><p>Fordert an, dass Datensätze mit doppelten Index Schlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden.</p>
<p>Vor Windows Server 2003 hat die Datenbank-Engine immer angenommen, dass diese Option wirksam ist, weil alle gruppierten Indizes auch ein Primärschlüssel sein müssen und daher eindeutig sein müssen. Ab Windows Server 2003 ist es möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die JET_bitTTForwardOnly-Option ebenfalls angegeben ist.</p>
<p>Im Allgemeinen ist es nicht möglich, zu ermitteln, welches Duplikat erfolgreich ist und welche Duplikate verworfen werden. Wenn jedoch die JET_bitTTErrorOnDuplicateInsertion-Option angefordert wird, ist der erste Datensatz mit einem bestimmten Index Schlüssel, der in die temporäre Tabelle eingefügt werden soll, immer erfolgreich.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Fordert an, dass die temporäre Tabelle flexibel genug ist, damit Datensätze, die zuvor eingefügt wurden, geändert werden können. Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</p>
<p>Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Fordert an, dass die temporäre Tabelle flexibel genug ist, um das Scannen von Datensätzen in beliebiger Reihenfolge und Richtung mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a>zuzulassen.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, ist es am besten, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Fordert an, dass <strong>null</strong> -Schlüssel Spaltenwerte näher am Ende des Indexes liegen als Schlüssel Spaltenwerte ungleich NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Zwingt den temporären Tabellen-Manager, die Suche nach der optimalen Strategie zu verwerfen, um die Verwaltung der temporären Tabelle zu verbessern, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Jeder Versuch, einen Datensatz mit dem gleichen Index Schlüssel wie ein zuvor eingefügter Datensatz einzufügen, schlägt mit JET_errKeyDuplicate sofort fehl. Wenn diese Option nicht angefordert wird, wird sofort ein Duplikat erkannt, und es wird ein Fehler zurückgegeben. Dies hängt von der Strategie ab, die von der Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt wurde.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern. Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Die temporäre Tabelle wird nur erstellt, wenn der temporäre Tabellen-Manager die-Implementierung verwenden kann, die für zwischen Abfrageergebnisse optimiert ist. Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</p>
<p>Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält. Weitere Informationen finden Sie unter JET_bitTTUnique.</p>
<p><strong>Windows Server 2003:  </strong> Diese Option ist nur für Windows Server 2003 und spätere Versionen verfügbar.</p></td>
</tr>
</tbody>
</table>


**prgcolumnid**

Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.

Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen. Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.

**cbkeymost**

Die maximale Größe für einen Schlüssel, der eine bestimmte Zeile darstellt.

Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden. Das Abschneiden von Schlüsseln ist wichtig, da sich dies auf den Fall auswirkt, dass Zeilen als verschieden betrachtet werden.

Wenn dieser Parameter auf 0 oder JET_cbKeyMostMin (255) festgelegt ist, bleiben die maximale Schlüsselgröße und ihre Semantik identisch mit der maximalen Schlüsselgröße, die von Windows Server 2003 und früheren Versionen unterstützt wird. Dieser Parameter kann auch auf einen größeren Wert als Funktion der Datenbankseiten Größe für die-Instanz (JET_paramDatabasePageSize) festgelegt werden. Weitere Informationen finden Sie unter JET_paramKeyMost.

**cbvarsegmac**

Die maximale Datenmenge, die in einer Spalte mit variabler Länge verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen.

Dieser Parameter kann verwendet werden, um die Menge des von einer bestimmten Schlüssel Spalte genutzten schlüsselplatzes zu steuern. Dieser Grenzwert ist in Bytes. Wenn dieser Parameter 0 (null) ist oder mit dem *cbkeymost* -Parameter identisch ist, ist kein Limit wirksam.

**TableID**

Das Tabellen Handle für die temporäre Tabelle, die als Ergebnis eines erfolgreichen [jetopumtemporarytable](./jetopentemporarytable-function.md)-Aufrufes erstellt wurde.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[Jetopumtemporarytable](./jetopentemporarytable-function.md)  
[System Parameter für Extensible Storage Engine](./extensible-storage-engine-system-parameters.md)
