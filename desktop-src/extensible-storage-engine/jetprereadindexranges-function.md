---
description: Weitere Informationen finden Sie unter JetPrereadIndexRanges-Funktion.
title: JetPrereadIndexRanges-Funktion
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ff2d9e7c538e8aa8cc862fe9a72c0308e497fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986663"
---
# <a name="jetprereadindexranges-function"></a>JetPrereadIndexRanges-Funktion


_**Gilt für:** Windows | Windows Server_

Die **JetPrereadIndexRanges-Funktion** vorgelesen Indizes, um die Leistung zu verbessern.

Die **JetPrereadIndexRanges-Funktion** wurde im Windows 8 eingeführt.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Die Tabelle, für die die Prereads ausgefertigt werden.

*rgIndexRanges*

Die Schlüsselbereiche, die vorgelesen werden.

*cIndexRanges*

Die Anzahl der Vorableseschlüsselbereiche, die durch die Anzahl der Elemente in *rgIndexRanges bestimmt werden.*

*pcRangesPreread*

Die Anzahl der Schlüsselbereiche, die tatsächlich vorgelesen wurden.

*rgcolumnidPreread*

Liste der Spalten-IDs für Spalten mit langen Wert, die vorab gelesen werden sollen. Standardmäßig ist nur der Datensatz auf der Seite vorgelesen. Wenn Spalten mit seitenseitigem Long-Wert vorgelesen werden müssen, müssen ihre Spalten-IDs über diesen Parameter übergeben werden.

*ccolumnidPreread*

Die Anzahl der Spalten-IDs für Spalten mit langen Wert, die vorab gelesen werden sollen, bestimmt durch die Anzahl der Elemente in *rgcolumnidPreread*.

*grbit*

Eine Gruppe von Bits, die null oder mehr der in der folgenden Tabelle aufgeführten Werte für die Vorleserichtung angibt.


| <p>Wert</p> | <p>Bedeutung</p> | 
|--------------|----------------|
| <p>Weiter</p> | <p>Vorlesen.</p> | 
| <p>Rückwärts</p> | <p>Vorlesen rückwärts.</p> | 
| <p>FirstPageOnly</p> | <p>Es wird nur die erste Seite einer langen Spalte vorgelesen.</p> | 
| <p>NormalizedKey</p> | <p>Ein normalisierter Schlüssel/Lesezeichen wird anstelle des Spaltenwerts bereitgestellt.</p> | 



### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der in der folgenden Tabelle aufgeführten Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Der Vorgang wurde erfolgreich abgeschlossen.</p> | 



#### <a name="remarks"></a>Bemerkungen

Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffercache befinden, sollten Sie asynchrone Leseläufe starten, um die Datensätze in den Datenbankpuffercache zu übertragen.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 



#### <a name="see-also"></a>Siehe auch

[JET_ERR](./jet-err.md)
