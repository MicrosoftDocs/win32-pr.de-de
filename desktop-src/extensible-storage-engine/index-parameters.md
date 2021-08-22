---
description: Weitere Informationen finden Sie unter Indexparameter.
title: Indexparameter
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 3d322334d5a14439461f903a583e11e78a7b829863c2b55dbf653dc13aa4d22d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604480"
---
# <a name="index-parameters"></a>Indexparameter


_**Gilt für:** Windows | Windows Server_

## <a name="index-parameters"></a>Indexparameter

Dieses Thema enthält Parameter, die für den Index verwendet werden.

*JET_paramIndexTupleIncrement*  
132  

Dieser Parameter gibt den Standardwert für das Offsetinkrement an, das verwendet wird, um den Quellspaltenwert beim Generieren der einzelnen Tupel schrittweise zu durchschritten. Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Vista und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTupleStart*  
133  

Dieser Parameter gibt den Standardwert für den Offset im Quellspaltenwert an, ab dem die Tupelgenerierung beginnt. Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Vista und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMax*  
111  

Dieser Parameter gibt den Standardwert für die maximale Tupellänge in einem Tupelindex an. Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur.

**Windows Vista:**  Vor der Windows Vista würde das Festlegen dieses Parameters auf 0 (null) den Standardwert zurücksetzen. Für Windows Vista wird dies nicht mehr unterstützt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0, 2-255</p>
<p><strong>Windows Vista:</strong> 2-255</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und spätere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMin*  
110  

Dieser Parameter gibt den Standardwert für die minimale Tupellänge in einem Tupelindex an. Weitere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) finden Sie unter .

**Windows Vista:**  Vor der Windows Vista würde das Festlegen dieses Parameters auf 0 (null) den Standardwert zurücksetzen. Für Windows Vista wird dies nicht mehr unterstützt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0, 2-255</p>
<p><strong>Windows Vista:</strong> 2-255</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und höhere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesToIndexMax*  
112  

Dieser Parameter gibt den Standardwert für die maximale Länge einer Quellzeichenfolge an, die in Tupel für einen Tupelindex unterteilt werden soll. Weitere Informationen finden Sie [unter JET_TUPLELIMITS.](./jet-tuplelimits-structure.md)

**Windows Vista:**  Vor Windows Vista wurde der Standardwert zurückgesetzt, wenn dieser Parameter auf 0 festgelegt wurde. Für Windows Vista wird dies nicht mehr unterstützt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>32767</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0 bis 32767</p>
<p><strong>Windows Vista:</strong> 1 bis 32767</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows XP und höhere Versionen</p></td>
</tr>
</tbody>
</table>


*JET_paramUnicodeIndexDefault*  
72  

Dieser Parameter steuert die Unicode-Standardparameter, die von jedem Index für eine Unicode-Schlüsselspalte verwendet werden. Der Typ dieses Parameters ist [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) und wird tatsächlich mithilfe eines Pufferzeigers übergeben, der im ganzzahligen Parameter von [JetGetSystemParameter](./jetgetsystemparameter-function.md) und [JetSetSystemParameter](./jetsetsystemparameter-function.md)gespeichert ist. Die Größe des Puffers muss der Größe von [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) entsprechen und mithilfe des Parameters für die Zeichenfolgenpuffergröße an [JetGetSystemParameter](./jetgetsystemparameter-function.md) übergeben werden. Dies ist eindeutig inkonsistent, aber das ist das Verhalten dieses Parameters.

Der Standardwert dieses Parameters enthält eine LCID für das gebietsschema für Englisch (USA) und die folgenden [LCMapStringW-Flags:](/windows/win32/api/winnls/nf-winnls-lcmapstringa)LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

**Windows 2000:**  Die SORTID in der LCID wird ignoriert. Eine SORTID von SORT_DEFAULT wird immer verwendet.

**Windows 2000:**  Die [LCMapStringW-Flags](/windows/win32/api/winnls/nf-winnls-lcmapstringa) müssen die folgenden Flags enthalten: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH. Darüber hinaus können die [LCMapStringW-Flags](/windows/win32/api/winnls/nf-winnls-lcmapstringa)die folgenden Flags enthalten: NORM_IGNORENONSPACE.

**Hinweis**  Wenn Ihre Anwendung Unicode-Daten speichern möchte, wird dringend empfohlen, sich nicht auf die Unicode-Standardparameter für Ihre Indizes zu verlassen. Die Verwendung von Englisch in den USA ist für die Verwendung des invarianten Gebietsschemas erforderlich, und es ist bekannt, dass die [LCMapStringW-Standardflags](/windows/win32/api/winnls/nf-winnls-lcmapstringa)einige Sprachen schwerwiegend beeinträchtigen. Sie sollten immer ihre eigenen Einstellungen für die Unicode-Parameter in JetCreateIndex2 angeben, indem [Sie JET_INDEXCREATE](./jet-indexcreate-structure.md)verwenden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Sonderfunktionen</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>JET_UNICODEINDEX* (JET_UNICODEINDEX)</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>Sonderfunktionen</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


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
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
