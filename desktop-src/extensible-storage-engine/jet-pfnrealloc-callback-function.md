---
description: 'Weitere Informationen finden Sie unter: JET_PFNREALLOC-Rückruffunktion'
title: JET_PFNREALLOC Rückruffunktion
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
ms.openlocfilehash: 24e4bc43928d6b7ea25294a0163b3b35b1fa04391196e86c54554a785ed2429d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616887"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC Rückruffunktion


_**Gilt für:** Windows | Windows Server_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC Rückruffunktion

Die JET_PFNREALLOC ist ein [realloc-kompatibler](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf, der von [JetEnumerateColumns](./jetenumeratecolumns-function.md) verwendet wird, um Arbeitsspeicher für die Ausgabepuffer zu reservieren.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parameter

*pvContext*

Der Kontextzeiger, der [JetEnumerateColumns gegeben wird.](./jetenumeratecolumns-function.md) Dieser Kontextzeiger kann verwendet werden, um den Zustand vom Aufrufer von [JetEnumerateColumns](./jetenumeratecolumns-function.md) an die Implementierung dieses Rückrufs zu übermitteln.

*Pv*

Wenn nicht NULL, gibt einen Zeiger auf einen Speicherblock an, der zuvor von diesem Rückruf zugeordnet wurde. Bei NULL wird ein neuer Speicherblock der angeforderten Größe zugeordnet.

*Cb*

Die neue Größe des Speicherblocks in Bytes. Wenn dieser Parameter 0 (null) ist und ein Speicherblock angegeben wird, wird dieser Speicherblock frei.

### <a name="return-value"></a>Rückgabewert

Das System kann Erfolgs- oder Fehlercodes als Ergebnis eines Aufrufs dieser Funktion generieren. Informationen zum Zurückgeben dieser Codes als HRESULTs finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).

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
<td><p>Wenn ein zuvor zugeordneter Speicherblock angegeben wurde und eine neue Größe von 0 angegeben wurde, wird dieser Block frei, und NULL wird zurückgegeben. Wenn ein zuvor zugeordneter Speicherblock angegeben wurde und eine neue Größe nicht 0 (null) angegeben wurde, wird der neu zugeordnete Speicherblock zurückgegeben. Wenn kein Speicherblock angegeben wurde, wird ein neu zugeordneter Speicherblock der angegebenen Größe zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p>Fehler</p></td>
<td><p>NULL wird zurückgegeben. Wenn ein zuvor zugeordneter Speicherblock bereitgestellt wurde, bleibt dieser Block zugeordnet.</p></td>
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
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
