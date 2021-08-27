---
description: 'Weitere Informationen finden Sie unter: JET_RSTMAP Struktur'
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
ms.openlocfilehash: e1f3813be8e1ea076a401ce5cdabef3e454b98c1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983583"
---
# <a name="jet_rstmap-structure"></a>JET_RSTMAP Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_rstmap-structure"></a>JET_RSTMAP Struktur

Die **JET_RSTMAP-Struktur** ermöglicht die Neustrukturierung von Datenbankdateipfaden, die während der Wiederherstellung in den Transaktionsprotokollen gespeichert werden, wenn sie von den [JetInit-](./jetinit-function.md) und [JetExternalRestore-Funktionen verwendet](./jetexternalrestore-function.md) werden. Dadurch können die Datenbanken verschoben werden, wenn sie offline oder aus einer Sicherung wiederhergestellt werden.

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


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_RSTMAP_W</strong> (Unicode) und JET_RSTMAP_A (ANSI) implementiert. <strong></strong></p> | 



### <a name="see-also"></a>Weitere Informationen

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
