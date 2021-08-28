---
description: 'Weitere Informationen zu: Informationsparameter'
title: Informationsparameter
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: 62adda8c818124b905cf81a2114cddd6556c3d13
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469527"
---
# <a name="informational-parameters"></a>Informationsparameter


_**Gilt für:** Windows | Windows Server_

## <a name="informational-parameters"></a>Informationsparameter

Dieses Thema enthält Parameter, die verwendet werden, um Informationen über die Datenbank-Engine verfügbar zu machen.

*JET_paramKeyMost*  
134  

Dieser schreibgeschützte Parameter gibt die maximal zulässige Indexschlüssellänge an, die für die aktuelle Datenbankseitengröße ausgewählt werden kann (wie von JET_paramDatabasePageSize).


| | | <p>Standardwert:</p> | <p>JET_cbKeyMost4KBytePage</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>255 – 65535</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>–</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>–</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Ab Windows Server 2008 und Windows Vista</p> | 



*JET_paramMaxColtyp*  
131  

Dieser schreibgeschützte Parameter gibt die maximale [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) für diese Version der Datenbank-Engine zurück. Dieser Wert kann verwendet werden, um zu testen, ob ein bestimmter Wert unterstützt [JET_COLTYP.](./jet-coltyp.md) Wenn ein [angegebener JET_COLTYP](./jet-coltyp.md) kleiner als der Wert dieses Parameters ist, wird er von der Datenbank-Engine unterstützt.


| | | <p>Standardwert:</p> | <p>JET_coltypUnsignedShort + 1</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0 – 255</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>–</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>–</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Ab Windows Server 2008 und Windows Vista</p> | 



*JET_paramLVChunkSizeMost*  
163  

Schreibgeschützter Parameter, der die Long-Value-Blockgröße basierend auf der konfigurierten Seitengröße zurückgibt. Wenn ein Long-Wert mit mehreren Jet{Set,Retrieve}Column-Aufrufen gelesen oder geschrieben werden soll, ist die Verwendung eines Puffers, dessen Größe ein Vielfaches der Blockgröße ist, effizienter.


| | | <p>Standardwert:</p> | <p>Seite 2 KB = 1966 Bytes<br />Seite 4 KB = 4014 Bytes<br />Seite 8 KB = 8110 Bytes<br />Seite 16 KB = 4050 Bytes<br />Seite 32 KB = 8150 Bytes</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-10000</p> | | <p>Umfang:</p> | <p></p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p></p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p></p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p></p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p></p> | | <p>Beeinträchtigt die Leistung:</p> | <p></p> | | <p>Betrifft Ressourcen:</p> | <p></p> | | <p>Verfügbarkeit:</p> | <p></p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
