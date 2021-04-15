---
description: 'Weitere Informationen finden Sie unter: jetprereadkeys-Funktion'
title: Jetprereadkeys-Funktion
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
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484875"
---
# <a name="jetprereadkeys-function"></a>Jetprereadkeys-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetprereadkeys-function"></a>Jetprereadkeys-Funktion

Die **jetprereadkeys** -Funktion liest Schlüsselwerte, um die Leistung der Bereinigung des Versionsspeicher zu verbessern.

**Windows 7: die prereadkeys** -Funktion wurde in Windows 7 eingeführt.

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

*-sid*

Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.

*TableID*

Der Cursor, der für diesen-Befehl verwendet werden soll.

*rgpvkeys*

Ein Array von Zeigern zu Schlüsseln. Schlüssel können mit [jetmakekey](./jetmakekey-function.md) erstellt oder mit [jetgetbookmark](./jetgetbookmark-function.md)abgerufen werden. Die Schlüssel müssen in aufsteigender oder absteigender Reihenfolge sortiert werden, je nach dem bestandenen grbit. Schlüssel können mit memcmp sortiert werden.

*rgcbkeys*

Ein Array von Schlüssellängen. rgpvkeys \[ n \] sollte auf einen Schlüssel der Länge rgcbkeys n zeigen. \[\]

*ckeys*

Die Anzahl der Schlüssel. rgpvkeys und rgcbkeys müssen jeweils auf ein Array mit mindestens "ckeys"-Elementen zeigen.

*pckeyspreread*

Gibt die Anzahl der Schlüssel zurück, für die prereads tatsächlich ausgestellt wurden. Dieser Parameter kann NULL sein.

*grbit*

Dies muss entweder JET_bitPrereadForward oder JET_bitPrereadBackward sein. Wenn grbit JET_bitPrereadForward ist, müssen die Schlüssel in aufsteigender Reihenfolge sortiert werden. Wenn grbit JET_bitPrereadBackward ist, müssen die Schlüssel in absteigender Reihenfolge sortiert werden.

### <a name="return-value"></a>Rückgabewert

Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück. Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).

Verschiedene e/a-Fehler können zusammen mit den folgenden API-Verwendungs Fehlern zurückgegeben werden:

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
<td><p>Es wurde eine falsche Schlüsselgröße übermittelt. Schlüssel können weder 0 noch länger als die maximale Schlüssellänge der Tabelle sein.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Ein ungültiger Parameter wurde übergeben. Dies kann durch einen NULL-Wert für einen erforderlichen Parameter verursacht werden, oder es kann darauf hingewiesen werden, dass das Schlüssel Array nicht ordnungsgemäß sortiert ist.</p></td>
</tr>
</tbody>
</table>


**Jetprereadkeys** durchläuft die internen Seiten der b-Struktur, um zu bestimmen, welche Blattseiten die von rgpvkeys/rgcbkeys angegebenen Schlüssel enthalten. Die Liste der Blattseiten wird sortiert, und dann werden die Seitenbereiche für die Seitenbereiche ausgegeben. Die Anzahl der Seiten, die auf "Preread" feststellen können, ist begrenzt, daher ist es möglich, dass nicht alle Schlüssel vorab registriert werden. In diesem Fall wird die Anzahl der Schlüssel, die tatsächlich in "pckeyspreread" geschrieben werden, zurückgegeben.

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
