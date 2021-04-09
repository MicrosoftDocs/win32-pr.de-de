---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE_INFO Struktur'
title: JET_INSTANCE_INFO Struktur
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868380"
---
# <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO Struktur

Die **JET_INSTANCE_INFO** -Struktur erhält Informationen über das Ausführen von Datenbankinstanzen, wenn Sie mit den Funktionen [jetgetinstanceinfo](./jetgetinstanceinfo-function.md) und [jedessnapshotfreeze](./jetossnapshotfreeze-function.md) verwendet werden.

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a>Member

**hinstanceid**

Der [JET_INSTANCE](./jet-instance.md) der angegebenen-Instanz.

**szinstancename**

Der Name der Datenbankinstanz. Dieser Wert kann **null** sein, wenn die Instanz keinen Namen hat.

**cdatenbanken**

Die Anzahl der Datenbanken, die an die Daten Bank Instanz angefügt sind. **CDatabase** enthält auch die Größe der Arrays von Zeichen folgen, die in " **szdatabasefilename**", " **szdatabasedisplayname**" und " **szdatabaseslvfilename**" zurückgegeben werden.

**szdatabasedateiname**

Ein Array von Zeichen folgen, das jeweils den Dateinamen einer Datenbank enthält, die an die Daten Bank Instanz angefügt ist. Das Array verfügt über **cdatenbanken** -Elemente.

**szdatabasedisplayname**

Ein Array von Zeichen folgen, die jeweils den anzeigen Amen einer Datenbank enthalten. Derzeit kann die Zeichenfolge NULL sein. Das Array verfügt über **cdatenbanken** -Elemente.

**szdatabaseslvfilename**

Ein Array von Zeichen folgen, das jeweils den Dateinamen der an die Daten Bank Instanz angefügten SLV-Datei enthält. Das Array verfügt über **cdatenbanken** -Elemente. SLV-Dateien werden nicht unterstützt. Daher sollte dieses Feld ignoriert werden.

### <a name="remarks"></a>Bemerkungen

Jede Daten Bank Instanz kann mehrere Datenbanken enthalten.

Für eine angegebene **JET_INSTANCE_INFO** Struktur ist das Array von Zeichen folgen, das für die Datenbanken zurückgegeben wird, in derselben Reihenfolge. Beispielsweise verweisen "szdatabasedisplayname \[ i \] " und "szdatabasefilename \[ i \] " auf dieselbe Datenbank.

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
<td><p>Wird als <strong>JET_INSTANCE_INFO_W</strong> (Unicode) und <strong>JET_INSTANCE_INFO _A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[Jetgetinstanceingefo](./jetgetinstanceinfo-function.md)  
[Jeto ssnapshotfreeze](./jetossnapshotfreeze-function.md)
