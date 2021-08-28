---
description: Weitere Informationen finden Sie unter JetPrereadKeys-Funktion.
title: JetPrereadKeys-Funktion
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24547a7970270943546e5fcfbc026ff24be144b0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986643"
---
# <a name="jetprereadkeys-function"></a>JetPrereadKeys-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetprereadkeys-function"></a>JetPrereadKeys-Funktion

Die **JetPrereadKeys-Funktion** liest Schlüsselwerte, um die Leistung der Versionsspeicherbereinigung zu verbessern.

**Windows 7: Die PrereadKeys-Funktion** wird in Windows 7 eingeführt.

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a>Parameter

*sesid*

Der Datenbanksitzungskontext, der für den API-Aufruf verwendet werden soll.

*tableid*

Der Cursor, der für diesen Aufruf verwendet werden soll.

*rgpvKeys*

Ein Array von Zeigern auf Schlüssel. Schlüssel können mit [JetMakeKey oder](./jetmakekey-function.md) mit [JetGetBookmark abgerufen werden.](./jetgetbookmark-function.md) Die Schlüssel müssen abhängig vom übergebenen Grbit in aufsteigender oder absteigender Reihenfolge sortiert werden. Schlüssel können mit memcmp sortiert werden.

*rgcbKeys*

Ein Array von Schlüssellängen. rgpvKeys n sollte auf einen Schlüssel der Länge \[ \] rgcbKeys \[ n verweisen.\]

*ckeys*

Die Anzahl der Schlüssel. rgpvKeys und rgcbKeys müssen jeweils auf ein Array mit mindestens ckeys-Elementen zeigen.

*pckeysPreread*

Gibt die Anzahl der Schlüssel zurück, für die Prereads tatsächlich ausgegeben wurden. Dieser Parameter kann NULL sein.

*grbit*

Dies muss entweder JET_bitPrereadForward oder JET_bitPrereadBackward. Wenn grbit JET_bitPrereadForward ist, müssen die Schlüssel in aufsteigender Reihenfolge sortiert werden. Wenn grbit JET_bitPrereadBackward ist, müssen die Schlüssel in absteigender Reihenfolge sortiert werden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

Es können verschiedene E/A-Fehler zusammen mit den folgenden API-Nutzungsfehlern zurückgegeben werden:


| <p>Rückgabecode</p> | <p>Beschreibung</p> | 
|--------------------|--------------------|
| <p>JET_errInvalidGrbit</p> | <p>Grbit war weder JET_bitPrereadForward noch JET_bitPrereadBackward.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Eine falsche Schlüsselgröße wurde übergeben. Schlüssel dürfen weder 0 noch länger als die maximale Schlüssellänge für die Tabelle sein.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Ein ungültiger Parameter wurde übergeben. Dies kann durch einen NULL-Wert für einen erforderlichen Parameter verursacht werden oder darauf hinweisen, dass das Schlüsselarray nicht ordnungsgemäß sortiert ist.</p> | 



**JetPrereadKeys** durchläuft die internen Seiten der b-Struktur, um zu bestimmen, welche Blattseiten die von rgpvKeys/rgcbKeys angegebenen Schlüssel enthalten. Die Liste der Blattseiten wird sortiert, und dann werden Vorablese für die Seitenbereiche ausgegeben. Die Anzahl der Seiten, die vorgelesen werden können, ist begrenzt, sodass es möglich ist, dass nicht alle Schlüssel vorgelesen werden. In diesem Fall wird die Anzahl der Schlüssel, die tatsächlich im Voraus gelesen werden, in pckeysPreread zurückgegeben.

#### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows 7.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 R2.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Bibliothek</strong></p> | <p>Verwenden Sie ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Erfordert ESENT.dll.</p> | 

