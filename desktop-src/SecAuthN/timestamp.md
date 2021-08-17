---
description: Der TimeStamp-Datentyp enthält Informationen zur Zeitgültigkeitsdauer von Sicherheitstoken. Das Format des Werts des TimeStamp-Datentyps ist mit dem der FILETIME-Struktur identisch.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: TimeStamp (Sspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e521818c9001213396c0046b92f8f0bd9727dddfeaf99b2e23b652a48f8ff95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786365"
---
# <a name="timestamp"></a>TimeStamp

Der **TimeStamp-Datentyp** enthält Informationen zur Zeitgültigkeitsdauer von Sicherheitstoken. Das Format des Werts des **TimeStamp-Datentyps** ist mit dem der [**FILETIME-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) identisch.


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (einschließlich Security.h)</dt> </dl> |



 

 
