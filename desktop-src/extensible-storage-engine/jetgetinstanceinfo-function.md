---
description: Weitere Informationen finden Sie unter JetGetInstanceInfo-Funktion.
title: JetGetInstanceInfo-Funktion
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6db8dce5861f6b75590becf2fd8ce3da112d09ae9d01e6e7514043fa47241861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849980"
---
# <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo-Funktion


_**Gilt für:** Windows | Windows Server_

## <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo-Funktion

Die **JetGetInstanceInfo-Funktion** ruft Informationen zu den ausgeführten Instanzen ab.

**Windows XP: JetGetInstanceInfo** wird in Windows XP eingeführt.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Parameter

*pcInstanceInfo*

Ein Zeiger auf einen Puffer, der die Anzahl der in *paInstanceInfo gespeicherten Elemente erhält.*

*paInstanceInfo*

Ein Zeiger auf einen Puffer, der die Adresse des ersten Elements eines Arrays von Strukturen erhält.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Einer der bereitgestellten Parameter enthielt einen unerwarteten Wert oder einen Wert, der in Kombination mit dem Wert eines anderen Parameters nicht sinnvoll war. Dieser Fehler wird von <strong>JetGetInstanceInfo zurückgegeben, wenn:</strong></p>
<ul>
<li><p><em>pcInstanceInfo oder</em> <em>paInstanceInfo sind</em> NULL.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Es ist nicht genügend Arbeitsspeicher verfügbar, um die Anforderung zu verarbeiten.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Hinweise

Die Datenbank-Engine ordnet ein Array [von](./jet-instance-info-structure.md) JET_INSTANCE_INFO zu. Der Aufrufer ist dafür verantwortlich, diesen Arbeitsspeicher mit [JetFreeBuffer frei zu geben.](./jetfreebuffer-function.md)

Wenn keine aktiven Instanzen verfügbar sind, gibt **JetGetInstanceInfo** JET_errSuccess zurück, *und pcInstanceInfo* erhält den Wert 0.

#### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JetGetInstanceInfoW</strong> (Unicode) und <strong>JetGetInstanceInfoA</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Weitere Informationen

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
