---
description: 'Weitere Informationen zu: JetPrereadKeys-Funktion'
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
ms.openlocfilehash: b7eb98c9478f912ff8d403a65ceb29055dd6d05f2c5cec9e8c348a3a1d354d10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559610"
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

Ein Array von Zeigern auf Schlüssel. Schlüssel können mit [JetMakeKey](./jetmakekey-function.md) oder mit [JetGetBookmark](./jetgetbookmark-function.md)abgerufen werden. Die Schlüssel müssen abhängig vom übergebenen Grbit in aufsteigender oder absteigender Reihenfolge sortiert werden. Schlüssel können mit memcmp sortiert werden.

*rgcbKeys*

Ein Array von Schlüssellängen. rgpvKeys \[ n \] sollte auf einen Schlüssel der Länge rgcbKeys n verweisen. \[\]

*ckeys*

Die Anzahl der Schlüssel. rgpvKeys und rgcbKeys müssen jeweils auf ein Array mit mindestens ckeys-Elementen zeigen.

*pckeysPreread*

Gibt die Anzahl der Schlüssel zurück, für die Prereads tatsächlich ausgegeben wurden. Dieser Parameter kann NULL sein.

*grbit*

Dies muss entweder JET_bitPrereadForward oder JET_bitPrereadBackward sein. Wenn grbit JET_bitPrereadForward ist, müssen die Schlüssel in aufsteigender Reihenfolge sortiert werden. Wenn grbit JET_bitPrereadBackward ist, müssen die Schlüssel in absteigender Reihenfolge sortiert werden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

Neben den folgenden API-Nutzungsfehlern können verschiedene E/A-Fehler zurückgegeben werden:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Rückgabecode</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Grbit war weder JET_bitPrereadForward noch JET_bitPrereadBackward.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Eine falsche Schlüsselgröße wurde übergeben. Schlüssel dürfen weder 0 noch länger als die maximale Schlüssellänge für die Tabelle sein.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde übergeben. Dies kann durch einen NULL-Wert für einen erforderlichen Parameter verursacht werden oder darauf hinweisen, dass das Schlüsselarray nicht ordnungsgemäß sortiert ist.</p></td>
</tr>
</tbody>
</table>


**JetPrereadKeys** durchläuft die internen Seiten der b-Struktur, um zu bestimmen, welche Blattseiten die von rgpvKeys/rgcbKeys angegebenen Schlüssel enthalten. Die Liste der Blattseiten wird sortiert, und dann werden Prereads für die Seitenbereiche ausgegeben. Die Anzahl der Seiten, die vorab gelesen werden können, ist begrenzt, sodass es möglich ist, dass nicht alle Schlüssel vorab gelesen werden können. In diesem Fall wird die Anzahl der Schlüssel, die tatsächlich vorab gelesen werden, in pckeysPreread zurückgegeben.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows 7.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 R2.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Deklariert in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>
