---
description: 'Weitere Informationen finden Sie unter: JET_OPENTEMPORARYTABLE Struktur'
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
ms.openlocfilehash: b17c16e1d0a3c5cd2eb42151df415487750c44f0a8a2976cb44262b2740ab4d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720280"
---
# <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE Struktur

Die **JET_OPENTEMPORARYTABLE-Struktur** enthält eine leicht erweiterbare Auflistung von Parametern für die **JET_OPENTEMPORARYTABLE** Funktion. Diese Struktur ist die temporäre Tabellenentsprechung der [JET_TABLECREATE](./jet-tablecreate-structure.md) Struktur.

**Windows Vista:** Die **JET_OPENTEMPORARYTABLE-Struktur** wird in Windows Vista eingeführt.

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

Die Größe dieser Struktur in Bytes (für zukünftige Erweiterungen). Sie muss auf sizeof( JET_TABLECREATE ) in Bytes festgelegt werden.

**prgcolumndef**

Spaltendefinitionen für die in der temporären Tabelle erstellten Spalten.

**Für** die Spaltendefinitionsoptionen, die mit einer temporären Tabelle verwendet werden, gelten wichtige Einschränkungen. Weitere Informationen finden Sie im Abschnitt Hinweise.

Zusätzlich zu den üblichen Spaltendefinitionsoptionen können 0 oder mehr der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.

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
<td><p>Die Sortierreihenfolge der Schlüsselspalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein. Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Die Spalte ist eine Schlüsselspalte für die temporäre Tabelle.</p>
<p>Die Reihenfolge der Spaltendefinitionen mit dieser Option, die im Eingabearray angegeben ist, bestimmt die Rangfolge der einzelnen Schlüsselspalten für die temporäre Tabelle. Die erste Spaltendefinition im Array, für das diese Option festgelegt ist, ist die wichtigste Schlüsselspalte und so weiter. Wenn mehr Schlüsselspalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht unterstützten Schlüsselspalten ignoriert.</p></td>
</tr>
</tbody>
</table>


**ccolumn**

Weitere *Informationen finden Sie unter prgcolumndef*.

**pidxunicode**

Die Locale ID und normalisierungsflags, die zum Vergleichen von Unicode-Schlüsselspaltendaten in der temporären Tabelle verwendet werden.

Wenn dieser Parameter nicht vorhanden ist und der *lcid-Parameter* nicht vorhanden ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüsselspalten in der temporären Tabelle zu vergleichen. Die Standard-LCID ist das us-englische Locale.

Wenn dieser Parameter nicht vorhanden ist, werden die Standardnormalisierungsflags verwendet, um Unicode-Schlüsselspaltendaten in der temporären Tabelle zu vergleichen. Die Standardnormalisierungsflags sind: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

**grbit**

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen an geben.

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
<td><p>Diese Option fordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> zum Suchen von Datensätzen nach Indexschlüsseln zu ermöglichen.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUnique</p></td>
<td><p>Anforderungen, dass Datensätze mit doppelten Indexschlüsseln aus dem letzten Satz von Datensätzen in der temporären Tabelle entfernt werden.</p>
<p>Vor Windows Server 2003 hat die Datenbank-Engine diese Option immer als wirksam angenommen, da alle gruppierten Indizes ebenfalls ein Primärschlüssel sein müssen und daher eindeutig sein müssen. Ab Windows Server 2003 ist es jetzt möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die option JET_bitTTForwardOnly angegeben wird.</p>
<p>Es ist nicht möglich zu wissen, welches Duplikat erfolgreich ist und welche Duplikate im Allgemeinen verworfen werden. Wenn jedoch die JET_bitTTErrorOnDuplicateInsertion angefordert wird, ist der erste Datensatz mit einem bestimmten Indexschlüssel, der in die temporäre Tabelle eingefügt werden soll, immer erfolgreich.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Fordert an, dass die temporäre Tabelle flexibel genug ist, damit datensätze, die zuvor eingefügt wurden, später geändert werden können. Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern.</p>
<p>Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Fordert an, dass die temporäre Tabelle flexibel genug ist, damit Datensätze in beliebiger Reihenfolge und Richtung mit <a href="gg294117(v=exchg.10).md">JetMove gescannt werden können.</a></p>
<p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Fordert an, dass NULL-Schlüsselspaltenwerte näher am Ende des Indexes sortiert werden als Spaltenwerte, die keine NULL-Schlüsselspalten sind. <strong></strong></p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Zwingt den Manager für temporäre Tabellen, die Suche nach der besten Strategie für die Verwaltung der temporären Tabelle zu verlassen, was zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Jeder Versuch, einen Datensatz mit demselben Indexschlüssel wie ein zuvor eingefügter Datensatz einfüge, würde sofort JET_errKeyDuplicate. Wenn diese Option nicht angefordert wird, wird sofort ein Duplikat erkannt und schlägt fehl oder wird später automatisch entfernt. Dies hängt von der Strategie ab, die die Datenbank-Engine für die Implementierung der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt hat.</p>
<p>Wenn diese Funktionalität nicht erforderlich ist, sollten Sie sie nicht anfordern. Wenn diese Funktionalität nicht angefordert wird, kann der Manager für temporäre Tabellen möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Die temporäre Tabelle wird nur erstellt, wenn der Manager für temporäre Tabellen die Implementierung verwenden kann, die für Zwischenabfrageergebnisse optimiert ist. Wenn ein Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, kann der Vorgang nicht durchgeführt JET_errCannotMaterializeForwardOnlySort.</p>
<p>Ein Nebeneffekt dieser Option besteht im Zulassen, dass die temporäre Tabelle Datensätze mit doppelten Indexschlüsseln enthält. Weitere JET_bitTTUnique finden Sie unter JET_bitTTUnique.</p>
<p><strong>Windows Server 2003:</strong> Diese Option ist nur auf Windows Server 2003 und höher verfügbar.</p></td>
</tr>
</tbody>
</table>


**prgcolumnid**

Der Ausgabepuffer, der das Array von Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.

Die Spalten-IDs in diesem Array entsprechen genau dem Eingabearray von Spaltendefinitionen. Daher muss die Größe dieses Puffers der Größe des Eingabearrays entsprechen.

**cbKeyMost**

Die maximale Größe für einen Schlüssel, der eine bestimmte Zeile darstellt.

Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden. Das Abschneiden von Schlüsseln ist wichtig, da sie sich darauf auswirken kann, wenn Zeilen als eindeutig betrachtet werden.

Wenn dieser Parameter auf 0 oder JET_cbKeyMostMin (255) festgelegt ist, bleiben die maximale Schlüsselgröße und ihre Semantik mit der maximalen Schlüsselgröße identisch, die von Windows Server 2003 und früheren Versionen unterstützt wird. Dieser Parameter kann auch auf einen größeren Wert festgelegt werden, je nach Datenbankseitengröße für die Instanz (JET_paramDatabasePageSize). Weitere JET_paramKeyMost finden Sie unter JET_paramKeyMost.

**cbVarSegMac**

Die maximale Datenmenge, die aus einer Spalte variabler Länge verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen.

Dieser Parameter kann verwendet werden, um die Menge des Schlüsselspeicherplatzes zu steuern, der von einer bestimmten Schlüsselspalte verbraucht wird. Dieser Grenzwert beträgt byte. Wenn dieser Parameter 0 (null) ist oder mit dem *cbKeyMost-Parameter* identisch ist, ist kein Grenzwert wirksam.

**tableid**

Das Tabellenhand handle für die temporäre Tabelle, die als Ergebnis eines erfolgreichen Aufrufs von [JetOpenTemporaryTable erstellt wurde.](./jetopentemporarytable-function.md)

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
<td><p>Wird in Esent.h deklariert.</p></td>
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
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[Erweiterbare Storage-Engine-Systemparameter](./extensible-storage-engine-system-parameters.md)
