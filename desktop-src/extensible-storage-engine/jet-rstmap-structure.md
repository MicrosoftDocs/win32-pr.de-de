---
description: 'Weitere Informationen finden Sie hier: JET_RSTMAP Struktur'
title: JET_RSTMAP Struktur
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750553"
---
# <a name="jet_rstmap-structure"></a>JET_RSTMAP Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_rstmap-structure"></a>JET_RSTMAP Struktur

Die **JET_RSTMAP** -Struktur ermöglicht die Neuzuordnung von Datenbankdatei Pfaden, die während der Wiederherstellung in den Transaktions Protokollen gespeichert werden, wenn Sie von der [jetinit](./jetinit-function.md) -Funktion und der [jetexternalrestore](./jetexternalrestore-function.md) -Funktion verwendet wird. Dadurch können die Datenbanken offline geschaltet oder von einer Sicherung wieder hergestellt werden.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Member

**szdatabasename**

Der aktuelle absolute Pfad einer Datenbank, die den Transaktions Protokollen zugeordnet ist, die während der Wiederherstellung wiedergegeben werden.

**sznewdatabasename**

Der neue absolute Pfad für die Datenbank.

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
<td><p>Wird als <strong>JET_RSTMAP_W</strong> (Unicode) und <strong>JET_RSTMAP_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetexternalrestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
