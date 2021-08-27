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
ms.openlocfilehash: cd932f64956e1a00aae5925b97dbf6c35ecc2661
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987603"
---
# <a name="informational-parameters"></a>Informationsparameter


_**Gilt für:** Windows | Windows Server_

## <a name="informational-parameters"></a>Informationsparameter

Dieses Thema enthält Parameter, die verwendet werden, um Informationen über die Datenbank-Engine verfügbar zu machen.

*JET_paramKeyMost*  
134  

Dieser schreibgeschützte Parameter gibt die maximal zulässige Indexschlüssellänge an, die für die aktuelle Datenbankseitengröße ausgewählt werden kann (wie von JET_paramDatabasePageSize).


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>JET_cbKeyMost4KBytePage</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>255 – 65535</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nicht zutreffend</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nicht zutreffend</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Ab Windows Server 2008 und Windows Vista</p> | 



*JET_paramMaxColtyp*  
131  

Dieser schreibgeschützte Parameter gibt die maximale [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) für diese Version der Datenbank-Engine zurück. Dieser Wert kann verwendet werden, um zu testen, ob ein bestimmter Wert unterstützt [JET_COLTYP.](./jet-coltyp.md) Wenn ein [JET_COLTYP](./jet-coltyp.md) kleiner als der Wert dieses Parameters ist, wird er von der Datenbank-Engine unterstützt.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>JET_coltypUnsignedShort + 1</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 255</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nicht zutreffend</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nicht zutreffend</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Ab Windows Server 2008 und Windows Vista</p> | 



*JET_paramLVChunkSizeMost*  
163  

Schreibgeschützter Parameter, der die Long-Value-Blockgröße basierend auf der konfigurierten Seitengröße zurückgibt. Wenn ein Long-Wert mit mehreren Jet{Set,Retrieve}Column-Aufrufen gelesen oder geschrieben werden soll, ist die Verwendung eines Puffers, dessen Größe ein Vielfaches der Blockgröße ist, effizienter.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Seite 2 KB = 1966 Bytes<br />Seite 4 KB = 4014 Bytes<br />Seite 8 KB = 8110 Bytes<br />Seite 16 KB = 4050 Bytes<br />Seite 32 KB = 8150 Bytes</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0-10000</p> | 
| <p>Umfang:</p> | <p></p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p></p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p></p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p></p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p></p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p></p> | 
| <p>Betrifft Ressourcen:</p> | <p></p> | 
| <p>Verfügbarkeit:</p> | <p></p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
