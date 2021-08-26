---
description: 'Weitere Informationen zu: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
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
ms.openlocfilehash: f341f88a192fee6de55e0077778abde83493e35e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482276"
---
# <a name="jet_err"></a>JET_ERR


_**Gilt für:** Windows | Windows Server_

## <a name="jet_err"></a>JET_ERR

Der **JET_ERR-Datentyp** enthält den [Extensible Storage Engine-Fehlercode](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Datentypen

JET_ERR

Ein Wert von 0 (entspricht JET_errSuccess) gibt an, dass der Aufruf erfolgreich war. Ein positiver Wert warnt vor einer nicht schwerwiegenden Bedingung, die während eines ansonsten erfolgreichen Aufrufs aufgetreten ist. Ein negativer Wert gibt an, dass der Aufruf fehlgeschlagen ist.

### <a name="remarks"></a>Hinweise

Informationen zum Zurückgeben von Fehlern als HRESULTs finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md). Informationen zu Flags zum Konfigurieren der Datenbank zur Behandlung von Fehlern finden Sie unter [Fehlerbehandlungsparameter](./error-handling-parameters.md).

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[Erweiterbare Storage-Engine-Fehler](./extensible-storage-engine-errors.md)  
[Extensible Storage Engine Error Codes (Erweiterbare Storage-Engine-Fehlercodes)](./extensible-storage-engine-error-codes.md)  
[Fehlerbehandlungsparameter](./error-handling-parameters.md)
