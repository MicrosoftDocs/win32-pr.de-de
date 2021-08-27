---
description: 'Weitere Informationen zu: JET_OPENTEMPORARYTABLE-Struktur'
title: JET_OPENTEMPORARYTABLE-Struktur
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
ms.openlocfilehash: ee2f2ab2fca7a849f889d46badcc86a8a5438fa8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478506"
---
# <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE-Struktur

Die **JET_OPENTEMPORARYTABLE-Struktur** enthält eine leicht erweiterbare Auflistung von **Parametern** für die JET_OPENTEMPORARYTABLE Funktion. Diese Struktur ist die temporäre Tabellenentsprechung der [JET_TABLECREATE](./jet-tablecreate-structure.md) Struktur.

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

**Es** gibt wichtige Einschränkungen für die Spaltendefinitionsoptionen, die mit einer temporären Tabelle verwendet werden. Weitere Informationen finden Sie im Abschnitt Hinweise.

Zusätzlich zu den üblichen Spaltendefinitionsoptionen können auch null oder mehr der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>Die Sortierreihenfolge der Schlüsselspalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein. Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Die Spalte ist eine Schlüsselspalte für die temporäre Tabelle.</p><p>Die Reihenfolge der Spaltendefinitionen mit dieser Option, die im Eingabearray angegeben ist, bestimmt die Rangfolge jeder Schlüsselspalte für die temporäre Tabelle. Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüsselspalte usw. Wenn mehr Schlüsselspalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht unterstützten Schlüsselspalten ignoriert.</p> | 



**ccolumn**

Siehe *prgcolumndef*.

**pidxunicode**

Die Gebietsschema-ID und normalisierungsflags, die zum Vergleichen aller Unicode-Schlüsselspaltendaten in der temporären Tabelle verwendet werden sollen.

Wenn dieser Parameter nicht vorhanden ist und der *lcid-Parameter* nicht vorhanden ist, wird die STANDARD-LCID verwendet, um alle Unicode-Schlüsselspalten in der temporären Tabelle zu vergleichen. Die LCID-Standardeinstellung ist das gebietsschema für Englisch in den USA.

Wenn dieser Parameter nicht vorhanden ist, werden die Standardnormalisierungsflags verwendet, um alle Unicode-Schlüsselspaltendaten in der temporären Tabelle zu vergleichen. Die Standardnormalisierungsflags sind: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

**grbit**

Eine Gruppe von Bits, die null oder mehr der folgenden Optionen angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>JET_bitTTIndexed</p> | <p>Diese Option fordert an, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> zum Suchen von Datensätzen nach Indexschlüssel zu ermöglichen.</p><p>Wenn diese Funktion nicht erforderlich ist, ist es am besten, sie nicht anzufordern. Wenn diese Funktionalität nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTUnique</p> | <p>Fordert an, dass Datensätze mit doppelten Indexschlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden.</p><p>Vor Windows Server 2003 hat die Datenbank-Engine diese Option immer als wirksam angesehen, da alle gruppierten Indizes ebenfalls ein Primärschlüssel sein müssen und daher eindeutig sein müssen. Ab Windows Server 2003 ist es jetzt möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn auch die option JET_bitTTForwardOnly angegeben ist.</p><p>Es ist nicht möglich zu wissen, welches Duplikat erfolgreich ist und welche Duplikate im Allgemeinen verworfen werden. Wenn jedoch die option JET_bitTTErrorOnDuplicateInsertion angefordert wird, ist der erste Datensatz mit einem angegebenen Indexschlüssel, der in die temporäre Tabelle eingefügt werden soll, immer erfolgreich.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Fordert an, dass die temporäre Tabelle flexibel genug ist, damit datensätze, die zuvor eingefügt wurden, später geändert werden können. Wenn diese Funktion nicht erforderlich ist, ist es am besten, sie nicht anzufordern.</p><p>Wenn diese Funktionalität nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Fordert an, dass die temporäre Tabelle flexibel genug ist, um das Scannen von Datensätzen in beliebiger Reihenfolge und Richtung mithilfe von <a href="gg294117(v=exchg.10).md">JetMove</a>zu ermöglichen.</p><p>Wenn diese Funktionalität nicht erforderlich ist, ist es am besten, sie nicht anzufordern. Wenn diese Funktionalität nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Fordert an, dass <strong>NULL-Schlüsselspaltenwerte</strong> näher am Ende des Indexes als Werte der Schlüsselspalte ungleich NULL sortiert werden.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Erzwingt, dass der temporäre Tabellen-Manager die Suche nach der besten Strategie für die Verwaltung der temporären Tabelle abbricht, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Jeder Versuch, einen Datensatz mit demselben Indexschlüssel wie ein zuvor eingefügter Datensatz einzufügen, schlägt sofort mit JET_errKeyDuplicate fehl. Wenn diese Option nicht angefordert wird, wird sofort ein Duplikat erkannt, und es tritt ein Fehler auf oder wird später automatisch entfernt, je nach der Strategie, die von der Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität ausgewählt wurde.</p><p>Wenn diese Funktion nicht erforderlich ist, ist es am besten, sie nicht anzufordern. Wenn diese Funktionalität nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie für die Verwaltung der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>Die temporäre Tabelle wird nur erstellt, wenn der temporäre Tabellen-Manager die Implementierung verwenden kann, die für Zwischenabfrageergebnisse optimiert ist. Wenn ein Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</p><p>Ein Nebeneffekt dieser Option besteht darin, dass die temporäre Tabelle Datensätze mit doppelten Indexschlüsseln enthalten kann. Weitere Informationen finden Sie unter JET_bitTTUnique.</p><p><strong>Windows Server 2003:</strong> Diese Option ist nur in Windows Server 2003 und höher verfügbar.</p> | 



**prgcolumnid**

Der Ausgabepuffer, der das Array von Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.

Die Spalten-IDs in diesem Array entsprechen genau dem Eingabearray der Spaltendefinitionen. Daher muss die Größe dieses Puffers der Größe des Eingabearrays entsprechen.

**cbKeyMost**

Die maximale Größe für einen Schlüssel, der eine bestimmte Zeile darstellt.

Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden. Die Kürzung von Schlüsseln ist wichtig, da sie sich darauf auswirken kann, wenn Zeilen als unterschiedlich betrachtet werden.

Wenn dieser Parameter auf 0 oder JET_cbKeyMostMin (255) festgelegt ist, bleiben die maximale Schlüsselgröße und die zugehörige Semantik mit der maximalen Schlüsselgröße identisch, die von Windows Server 2003 und früheren Versionen unterstützt wird. Dieser Parameter kann auch als Funktion der Datenbankseitengröße für die Instanz (JET_paramDatabasePageSize) auf einen größeren Wert festgelegt werden. Weitere Informationen finden Sie unter JET_paramKeyMost.

**cbVarSegMac**

Die maximale Datenmenge, die aus einer beliebigen Spalte variabler Länge verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen.

Dieser Parameter kann verwendet werden, um die Menge an Schlüsselspeicherplatz zu steuern, die von einer bestimmten Schlüsselspalte belegt wird. Dieser Grenzwert wird in Bytes angegeben. Wenn dieser Parameter 0 (null) ist oder mit dem *cbKeyMost-Parameter* identisch ist, ist kein Grenzwert wirksam.

**tableid**

Das Tabellenhandle für die temporäre Tabelle, die als Ergebnis eines erfolgreichen Aufrufs von [JetOpenTemporaryTable](./jetopentemporarytable-function.md)erstellt wurde.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[Erweiterbare Storage Engine-Systemparameter](./extensible-storage-engine-system-parameters.md)
