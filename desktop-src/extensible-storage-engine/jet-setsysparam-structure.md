---
description: 'Weitere Informationen finden Sie hier: JET_SETSYSPARAM Struktur'
title: JET_SETSYSPARAM Struktur
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342989"
---
# <a name="jet_setsysparam-structure"></a>JET_SETSYSPARAM Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_setsysparam-structure"></a>JET_SETSYSPARAM Struktur

Ein Array von **JET_SETSYSPARAM** Strukturen gibt einen bestimmten Satz globaler Systemparameter an, die bei Verwendung der [jetenablemultiinstance](./jetenablemultiinstance-function.md) -Funktion als Argument festgelegt werden.

**Windows XP:** Diese Struktur wird in Windows XP eingeführt.

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a>Member

**paramid**

Die ID des System Parameters, der festgelegt wird.

Eine umfassende Liste der Systemparameter und deren Eigenschaften finden Sie unter [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) .

**lParam**

Der optionale Wert, der für den ausgewählten Systemparameter festgelegt werden soll, wenn dieser Systemparameter einen ganzzahligen Typ hat.

**RT**

Der optionale Wert, der für den ausgewählten Systemparameter festgelegt werden soll, wenn dieser Systemparameter vom Typ String ist.

**irre**

Der Fehler, der sich aus dem Aufrufen von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit den zuvor angegebenen Parametern ergibt.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_ SETSYSPARAM_W</strong> (Unicode) und <strong>JET_ SETSYSPARAM_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[System Parameter für Extensible Storage Engine](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[Jetenablemultiinstance](./jetenablemultiinstance-function.md)  
[Jetsetsystemparameter](./jetsetsystemparameter-function.md)
