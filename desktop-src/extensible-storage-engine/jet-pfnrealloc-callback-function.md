---
description: 'Weitere Informationen über: JET_PFNREALLOC Callback-Funktion'
title: JET_PFNREALLOC Callback-Funktion
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218594"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC Callback-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC Callback-Funktion

Die JET_PFNREALLOC-Funktion ist ein [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) -kompatibler Rückruf, der von [jetenumeratecolumns](./jetenumeratecolumns-function.md) verwendet wird, um Speicher für die Ausgabepuffer zuzuweisen.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parameter

*pvcontext*

Der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)angegebene Kontext Zeiger. Dieser Kontext Zeiger kann verwendet werden, um den Zustand des Aufrufers von [jetenumeratecolumns](./jetenumeratecolumns-function.md) an die Implementierung dieses Rückrufs zu übermitteln.

*teuren*

Wenn der Wert ungleich NULL ist, wird ein Zeiger auf einen Speicherblock angegeben, der zuvor von diesem Rückruf zugeordnet wurde. Wenn der Wert NULL ist, wird ein neuer Speicherblock der angeforderten Größe zugeordnet.

*betrieben*

Die neue Größe des Speicherblocks in Bytes. Wenn dieser Parameter 0 (null) ist und ein Speicherblock angegeben wird, wird dieser Speicherblock freigegeben.

### <a name="return-value"></a>Rückgabewert

Das System generiert möglicherweise Erfolgs-oder Fehlercodes, wenn diese Funktion aufgerufen wird. Informationen dazu, wie diese Codes als HRESULTs zurückgegeben werden, finden Sie unter [Fehler bei Extensible Storage Engine](./extensible-storage-engine-errors.md).

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
<td><p>Erfolg</p></td>
<td><p>Wenn ein zuvor zugewiesener Speicherblock angegeben wurde und eine neue Größe von 0 (null) angegeben wurde, wird der Block freigegeben, und es wird NULL zurückgegeben. Wenn ein zuvor zugewiesener Speicherblock angegeben wurde und eine neue Größe ungleich 0 (null) angegeben wurde, wird der neu zugeordnete Speicherblock zurückgegeben. Wenn kein Speicherblock angegeben wurde, wird ein neu zugeordneter Speicherblock der angegebenen Größe zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>Fehler</p></td>
<td><p>NULL wird zurückgegeben. Wenn ein zuvor zugeordneter Speicherblock bereitgestellt wurde, bleibt dieser Block reserviert.</p></td>
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

[Jetenreeratecolumschlag](./jetenumeratecolumns-function.md)
