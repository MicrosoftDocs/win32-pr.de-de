---
description: Der timestamp-Datentyp enthält Informationen über die Gültigkeitsdauer von Sicherheits Token. Das Format des Werts des timestamp-Datentyps entspricht dem Format der FILETIME-Struktur.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Timestamp (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356651"
---
# <a name="timestamp"></a>TimeStamp

Der **timestamp** -Datentyp enthält Informationen über die Gültigkeitsdauer von Sicherheits Token. Das Format des Werts des **timestamp** -Datentyps entspricht dem Format der [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur.


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |



 

 
