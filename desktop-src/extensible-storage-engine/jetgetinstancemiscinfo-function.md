---
description: 'Weitere Informationen zu: jetgetinstancefehlinfo-Funktion'
title: Jetgetinstancefehlinfo-Funktion
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
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042652"
---
# <a name="jetgetinstancemiscinfo-function"></a>Jetgetinstancefehlinfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetinstancemiscinfo-function"></a>Jetgetinstancefehlinfo-Funktion

Die **jetgetinstancefehlinfo** -Funktion Ruft Informationen über die Instanz ab, während die Instanz online ist.

**Windows Vista: jetgetinstancefehlinfo** wird in Windows Vista eingeführt.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parameter

*lichen*

Identifiziert die Daten Bank Instanz, die für den API-Befehl verwendet wird.

*pvresult*

Zeiger auf einen Puffer, der die Informationen empfängt. Der Typ des Puffers ist von *infolevel* abhängig. Der Aufrufer ist dafür verantwortlich, den Puffer entsprechend anzupassen.

*cbmax*

Die Größe (in Bytes) des Puffers, der in *pvresult* übergeben wird.

*Infolevel*

Bestimmt, welche Art von Informationen für die Instanz abgerufen werden, die von der- *Instanz* angegeben wird. Das Format der in *pvresult* gespeicherten Daten hängt von *infolevel* ab.

Die folgenden Optionen sind für die Verwendung mit diesem Parameter verfügbar.

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
<td><p><em>pvresult</em> wird als <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> Struktur der Transaktionsprotokoll Sequenz interpretiert, die dieser Instanz zugeordnet ist.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Es wurde entweder ein ungültiger <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> oder eine ungültige <em>infolevel</em> angegeben.</p></td>
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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothek</strong></p></td>
<td><p>Verwenden Sie ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Erfordert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
