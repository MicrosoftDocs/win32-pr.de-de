---
description: 'Weitere Informationen zu: JET_SIGNATURE-Struktur'
title: JET_SIGNATURE-Struktur
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: 9d254a392ade9daa43382d8418f2dda90729eddc81f6c3bbd7013d89ae8f2e74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616190"
---
# <a name="jet_signature-structure"></a>JET_SIGNATURE-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_signature-structure"></a>JET_SIGNATURE-Struktur

Die **JET_SIGNATURE-Struktur** enthält Informationen, die eine Datenbank eindeutig identifizieren.

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>Member

**ulRandom**

Eine zufällig zugewiesene Zahl.

**logtimeCreate**

Die [JET_LOGTIME](./jet-logtime-structure.md) zum Zeitpunkt der Ausführung von [JetCreateDatabase.](./jetcreatedatabase-function.md)

**szComputerName**

Der optionale Zeichenfolgenwert des NetBIOS-Namens für den Computer. Dieser Wert kann nicht festgelegt werden.

### <a name="remarks"></a>Hinweise

Dies kann als Element von [JET_DBINFOMISC](./jet-dbinfomisc-structure.md)gefunden werden.

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
<td><p>Deklariert in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
