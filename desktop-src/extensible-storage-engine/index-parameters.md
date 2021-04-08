---
description: 'Weitere Informationen finden Sie hier: Index Parameter'
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
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050540"
---
# <a name="index-parameters"></a>Indexparameter


_**Gilt für:** Windows | Windows Server_

## <a name="index-parameters"></a>Indexparameter

Dieses Thema enthält Parameter, die für den Index verwendet werden.

*JET_paramIndexTupleIncrement*  
132  

Dieser Parameter gibt den Standardwert für das Offset Inkrement an, mit dem der Wert der Quell Spalte durchlaufen wird, während jedes Tupel erzeugt wird. Weitere Informationen finden Sie in der [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) -Struktur.

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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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

Dieser Parameter gibt den Standardwert für den Offset in dem Wert der Quell Spalte an, ab dem die tupelgenerierung gestartet wird. Weitere Informationen finden Sie in der [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) -Struktur.

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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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

Dieser Parameter gibt den Standardwert für die maximale tupellänge in einem Tupelindex an. Weitere Informationen finden Sie in der [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) -Struktur.

**Windows Vista:**  Vor Windows Vista würde das Festlegen dieses Parameters auf NULL auf seinen Standardwert zurückgesetzt. Für Windows Vista wird dies nicht mehr unterstützt.

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
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003: </strong>  0, 2-255</p>
<p><strong>Windows Vista:</strong>  2-255</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMin*  
110  

Dieser Parameter gibt den Standardwert für die minimale tupellänge in einem Tupelindex an. Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  Vor Windows Vista würde das Festlegen dieses Parameters auf NULL auf seinen Standardwert zurückgesetzt. Für Windows Vista wird dies nicht mehr unterstützt.

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
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003: </strong>  0, 2-255</p>
<p><strong>Windows Vista:</strong>  2-255</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesToIndexMax*  
112  

Dieser Parameter gibt den Standardwert für die maximale Länge einer Quell Zeichenfolge an, um für einen Tupelindex in Tupel zu unterbrechen. Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .

**Windows Vista:**  Vor Windows Vista würde das Festlegen dieses Parameters auf NULL auf seinen Standardwert zurückgesetzt. Für Windows Vista wird dies nicht mehr unterstützt.

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
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  0 – 32767</p>
<p><strong>Windows Vista:</strong>  1 – 32767</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Instanz</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Versionen von Windows XP und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramUnicodeIndexDefault*  
72  

Dieser Parameter steuert die Unicode-Standardparameter, die von einem beliebigen Index für eine Unicode-Schlüssel Spalte verwendet werden. Der Typ dieses Parameters ist [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) und wird tatsächlich mithilfe eines Puffer Zeigers übergeben, der im Integer-Parameter von [jetgetsystemparameter](./jetgetsystemparameter-function.md) und [jetsetsystemparameter](./jetsetsystemparameter-function.md)gespeichert ist. Die Größe des Puffers muss der Größe des [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) entsprechen und mithilfe des Parameters für die Zeichen folgen Puffergröße an [jetgetsystemparameter](./jetgetsystemparameter-function.md) übergeben werden. Dies ist eindeutig inkonsistent, aber das Verhalten dieses Parameters.

Der Standardwert dieses Parameters enthält eine LCID für das US-englische Gebiets Schema und die folgenden [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa)-Flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

**Windows 2000:**  Die Element-ID in der LCID wird ignoriert. Eine Element-ID von SORT_DEFAULT wird immer verwendet.

**Windows 2000:**  Die [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa) -Flags müssen die folgenden Flags enthalten: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH. Außerdem können die [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa)-Flags die folgenden Flags enthalten: NORM_IGNORENONSPACE.

**Hinweis**  Wenn Ihre Anwendung Unicode-Daten speichern möchte, wird dringend empfohlen, nicht auf die standardmäßigen Unicode-Parameter für die Indizes zu vertrauen. Die Verwendung von US-Englisch ist gleichbedeutend mit der Verwendung des invarianten Gebiets Schemas, und die standardmäßigen [lcmapstringw](/windows/win32/api/winnls/nf-winnls-lcmapstringa)-Flags sind bekannt, dass einige Sprachen ernsthaft beeinträchtigt werden. Sie sollten mit [JET_INDEXCREATE](./jet-indexcreate-structure.md)immer eigene Einstellungen für die Unicode-Parameter für JetCreateIndex2 angeben.

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
<td><p>JET_UNICODEINDEX * (JET_UNICODEINDEX)</p></td>
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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[Jetkreateingestance](./jetcreateinstance-function.md)  
[Jetgetsystemparameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)
