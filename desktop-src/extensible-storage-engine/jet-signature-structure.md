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
ms.openlocfilehash: 456eadecbaba7295753a18ec2ca739f5e3fc8391
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987823"
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

### <a name="remarks"></a>Bemerkungen

Dies kann als Element von [JET_DBINFOMISC](./jet-dbinfomisc-structure.md)gefunden werden.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
