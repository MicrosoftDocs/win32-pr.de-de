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
ms.openlocfilehash: f53430a6b624b6b65a5d02727dc16d7f1fba669d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470896"
---
# <a name="index-parameters"></a>Indexparameter


_**Gilt für:** Windows | Windows Server_

## <a name="index-parameters"></a>Indexparameter

Dieses Thema enthält Parameter, die für den Index verwendet werden.

*JET_paramIndexTupleIncrement*  
132  

Dieser Parameter gibt den Standardwert für das Offsetinkrement an, das verwendet wird, um den Quellspaltenwert beim Generieren der einzelnen Tupel schrittweise zu durchschritten. Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur.


| | | <p>Standardwert:</p> | <p>1</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0 - 32767</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows Vista und spätere Versionen</p> | 



*JET_paramIndexTupleStart*  
133  

Dieser Parameter gibt den Standardwert für den Offset im Quellspaltenwert an, ab dem die Tupelgenerierung beginnt. Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur.


| | | <p>Standardwert:</p> | <p>0</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0 - 32767</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows Vista und spätere Versionen</p> | 



*JET_paramIndexTuplesLengthMax*  
111  

Dieser Parameter gibt den Standardwert für die maximale Tupellänge in einem Tupelindex an. Weitere Informationen finden Sie unter [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) Struktur.

**Windows Vista:**  Vor der Windows Vista würde das Festlegen dieses Parameters auf 0 (null) auf den Standardwert zurückgesetzt. Für Windows Vista wird dies nicht mehr unterstützt.


| | | <p>Standardwert:</p> | <p>10</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



*JET_paramIndexTuplesLengthMin*  
110  

Dieser Parameter gibt den Standardwert für die minimale Tupellänge in einem Tupelindex an. Weitere [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) finden Sie unter .

**Windows Vista:**  Vor der Windows Vista würde das Festlegen dieses Parameters auf 0 (null) auf den Standardwert zurückgesetzt. Für Windows Vista wird dies nicht mehr unterstützt.


| | | <p>Standardwert:</p> | <p>3</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Releases</p> | 



*JET_paramIndexTuplesToIndexMax*  
112  

Dieser Parameter gibt den Standardwert für die maximale Länge einer Quellzeichenfolge an, die in Tupel für einen Tupelindex unterteilt werden soll. Weitere Informationen finden Sie [unter JET_TUPLELIMITS.](./jet-tuplelimits-structure.md)

**Windows Vista:**  Vor Windows Vista wurde durch Festlegen dieses Parameters auf 0 (null) wieder der Standardwert festgelegt. Für Windows Vista wird dies nicht mehr unterstützt.


| | | <p>Standardwert:</p> | <p>32767</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0 – 32767</p><p><strong>Windows Vista:</strong> 1 bis 32767</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Releases</p> | 



*JET_paramUnicodeIndexDefault*  
72  

Dieser Parameter steuert die Unicode-Standardparameter, die von jedem Index für eine Unicode-Schlüsselspalte verwendet werden. Der Typ dieses Parameters ist [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) und wird tatsächlich mithilfe eines Pufferzeigers übergeben, der im ganzzahligen Parameter von [JetGetSystemParameter](./jetgetsystemparameter-function.md) und [JetSetSystemParameter](./jetsetsystemparameter-function.md)gespeichert ist. Die Größe des Puffers muss der Größe des [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) entsprechen und mithilfe des Parameters für die Zeichenfolgenpuffergröße an [JetGetSystemParameter](./jetgetsystemparameter-function.md) übergeben werden. Dies ist eindeutig inkonsistent, aber das ist das Verhalten dieses Parameters.

Der Standardwert dieses Parameters enthält eine LCID für das gebietsschema für Englisch (USA) und die folgenden [LCMapStringW-Flags:](/windows/win32/api/winnls/nf-winnls-lcmapstringa)LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

**Windows 2000:**  Die SORTID in der LCID wird ignoriert. Eine SORTID von SORT_DEFAULT wird immer verwendet.

**Windows 2000:**  Die [LCMapStringW-Flags](/windows/win32/api/winnls/nf-winnls-lcmapstringa) müssen die folgenden Flags enthalten: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH. Darüber hinaus können die [LCMapStringW-Flags](/windows/win32/api/winnls/nf-winnls-lcmapstringa)die folgenden Flags enthalten: NORM_IGNORENONSPACE.

**Hinweis**  Wenn Ihre Anwendung Unicode-Daten speichern möchte, wird dringend empfohlen, sich nicht auf die Unicode-Standardparameter für Ihre Indizes zu verlassen. Die Verwendung von Englisch in den USA ist für die Verwendung des invarianten Gebietsschemas erforderlich, und es ist bekannt, dass die [LCMapStringW-Standardflags](/windows/win32/api/winnls/nf-winnls-lcmapstringa)einige Sprachen schwerwiegend beeinträchtigen. Sie sollten immer ihre eigenen Einstellungen für die Unicode-Parameter in JetCreateIndex2 angeben, indem [Sie JET_INDEXCREATE](./jet-indexcreate-structure.md)verwenden.


| | | <p>Standardwert:</p> | <p>Sonderfunktionen</p> | | <p>Typ:</p> | <p>JET_UNICODEINDEX* (JET_UNICODEINDEX)</p> | | <p>Gültiger Bereich:</p> | <p>Sonderfunktionen</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
