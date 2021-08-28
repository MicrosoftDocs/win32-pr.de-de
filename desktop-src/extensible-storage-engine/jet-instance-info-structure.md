---
description: 'Weitere Informationen finden Sie unter: JET_INSTANCE_INFO Struktur'
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
ms.openlocfilehash: 6dbeab994d012f031de7620487c754b69d00db3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472696"
---
# <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO Struktur

Die **JET_INSTANCE_INFO-Struktur** empfängt Informationen zum Ausführen von Datenbankinstanzen, wenn sie mit den [Funktionen JetGetInstanceInfo](./jetgetinstanceinfo-function.md) und [JetOSSnapshotFreeze verwendet](./jetossnapshotfreeze-function.md) wird.

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

**hInstanceId**

Die [JET_INSTANCE](./jet-instance.md) der angegebenen Instanz.

**szInstanceName**

Der Name der Datenbankinstanz. Dieser Wert kann NULL **sein,** wenn die Instanz keinen Namen hat.

**cDatabases**

Die Anzahl der Datenbanken, die an die Datenbankinstanz angefügt sind. **cDatabases enthält** auch die Größe der Arrays von Zeichenfolgen, die in **szDatabaseFileName,** **szDatabaseDisplayName** und **szDatabaseSLVFileName zurückgegeben werden.**

**szDatabaseFileName**

Ein Array von Zeichenfolgen, die jeweils den Dateinamen einer Datenbank enthalten, die an die Datenbankinstanz angefügt ist. Das Array verfügt **über cDatabases-Elemente.**

**szDatabaseDisplayName**

Ein Array von Zeichenfolgen, die jeweils den Anzeigenamen einer Datenbank enthalten. Derzeit kann die Zeichenfolge NULL sein. Das Array verfügt **über cDatabases-Elemente.**

**szDatabaseSLVFileName**

Ein Array von Zeichenfolgen, die jeweils den Dateinamen der SLV-Datei enthalten, die an die Datenbankinstanz angefügt ist. Das Array verfügt **über cDatabases-Elemente.** SLV-Dateien werden nicht unterstützt, daher sollte dieses Feld ignoriert werden.

### <a name="remarks"></a>Hinweise

An jede Datenbankinstanz können mehrere Datenbanken angefügt sein.

Für eine bestimmte **JET_INSTANCE_INFO-Struktur** befindet sich das Array von Zeichenfolgen, das für die Datenbanken zurückgegeben wird, in der gleichen Reihenfolge. Beispielsweise verweisen "szDatabaseDisplayName \[ \] i" und "szDatabaseFileName \[ \] i" auf dieselbe Datenbank.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_INSTANCE_INFO_W</strong> (Unicode) und JET_INSTANCE_INFO _A (ANSI) implementiert. <strong></strong></p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)
