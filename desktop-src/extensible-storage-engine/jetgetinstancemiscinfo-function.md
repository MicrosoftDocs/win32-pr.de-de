---
description: 'Weitere Informationen finden Sie unter: JetGetInstanceMiscInfo-Funktion'
title: JetGetInstanceMiscInfo-Funktion
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ada8dfcd69a4e1933bcb60756d1b812f3b358cd37a3cda914819d2a9f6f4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472350"
---
# <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo-Funktion

Die **JetGetInstanceMiscInfo-Funktion** ruft Informationen über die Instanz ab, während die Instanz online ist.

**Windows Vista: JetGetInstanceMiscInfo** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*Instanz*

Identifiziert die Datenbankinstanz, die für den API-Aufruf verwendet wird.

*pvResult*

Zeiger auf einen Puffer, der die Informationen erhält. Der Typ des Puffers ist von *InfoLevel abhängig.* Der Aufrufer ist dafür verantwortlich, den Puffer entsprechend auszurichten.

*cbMax*

Die Größe des in pvResult übergebenen Puffers in *Bytes.*

*InfoLevel*

Bestimmt, welche Art von Informationen für die instanz angegebene Instanz abgerufen *wird.* Das Format der in *pvResult* gespeicherten Daten hängt von *InfoLevel ab.*

Die folgenden Optionen stehen für die Verwendung mit diesem Parameter zur Verfügung.

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
<td><p>JET_InstanceMiscInfoLogSignature</p></td>
<td><p><em>pvResult</em> wird als <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> Struktur der Transaktionsprotokollsequenz interpretiert, die dieser Instanz zugeordnet ist.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR-Datentyp](./jet-err.md) mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errSuccess</p></td>
<td><p>Der Vorgang wurde erfolgreich abgeschlossen.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Der Puffer war zu klein.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Entweder wurde ein <a href="gg294048(v=exchg.10).md">ungültiges JET_INSTANCE</a> oder ein ungültiges <em>InfoLevel</em> angegeben.</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>Anforderungen

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


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
