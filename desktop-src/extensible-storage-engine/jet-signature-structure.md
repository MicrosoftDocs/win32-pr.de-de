---
description: 'Weitere Informationen finden Sie unter: JET_SIGNATURE Struktur'
title: JET_SIGNATURE Struktur
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
ms.openlocfilehash: da4684872358d9d6751812b2adb2b2bea819a2e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476476"
---
# <a name="jet_signature-structure"></a>JET_SIGNATURE Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_signature-structure"></a>JET_SIGNATURE Struktur

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

Diese kann als Element von gefunden [JET_DBINFOMISC.](./jet-dbinfomisc-structure.md)

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
