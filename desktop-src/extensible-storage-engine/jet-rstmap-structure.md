---
description: 'Weitere Informationen zu: JET_RSTMAP-Struktur'
title: JET_RSTMAP-Struktur
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
ms.openlocfilehash: 8e9952c040540e78c76d81babbb4c7b326fe92f8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465857"
---
# <a name="jet_rstmap-structure"></a>JET_RSTMAP-Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_rstmap-structure"></a>JET_RSTMAP-Struktur

Die **JET_RSTMAP-Struktur** ermöglicht die Neuzuordnung von Datenbankdateipfaden, die während der Wiederherstellung in den Transaktionsprotokollen gespeichert werden, wenn sie von den [JetInit-](./jetinit-function.md) und [JetExternalRestore-Funktionen](./jetexternalrestore-function.md) verwendet werden. Dadurch können die Datenbanken verschoben werden, wenn sie offline oder aus einer Sicherung wiederhergestellt werden.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Member

**szDatabaseName**

Der aktuelle absolute Pfad einer Datenbank, die den Transaktionsprotokollen zugeordnet ist, die während der Wiederherstellung wiedergegeben werden.

**szNewDatabaseName**

Der neue absolute Pfad für die Datenbank.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementiert als <strong>JET_RSTMAP_W</strong> (Unicode) und <strong>JET_RSTMAP_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
