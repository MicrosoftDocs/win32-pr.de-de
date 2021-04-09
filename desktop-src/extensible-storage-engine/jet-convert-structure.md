---
description: 'Weitere Informationen finden Sie hier: JET_CONVERT Struktur'
title: JET_CONVERT Struktur
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863184"
---
# <a name="jet_convert-structure"></a>JET_CONVERT Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_convert-structure"></a>JET_CONVERT Struktur

Die **JET_CONVERT** Struktur enthält den Namen einer früheren ESE-Version-dll, die zum Lesen von Datenbanken verwendet wird, die mit dieser früheren Version erstellt wurden. Außerdem werden andere Flags bereitgestellt, um die Art der Konvertierung zu steuern.

**Windows Server 2003:** Die Funktion in [jetcompact](./jetcompact-function.md) , die eine Konvertierung durchgeführt hat, wurde aus dem Produkt in Windows Server 2003 entfernt. Sie wird nur in Windows 2000 und Windows XP unterstützt.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Member

**Szolddll**

Der Name, einschließlich der Pfadinformationen, zur früheren Version der ESE-dll.

**fFlags**

Ist für das System reserviert.

**nicht ordnungsgemäß**

Ist für das System reserviert.

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
<td><p>Wird als <strong>JET_CONVERT_W</strong> (Unicode) und <strong>JET_CONVERT_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetcompact](./jetcompact-function.md)
