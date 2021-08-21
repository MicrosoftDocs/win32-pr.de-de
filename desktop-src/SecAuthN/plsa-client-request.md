---
description: Ein nicht transparenter Datentyp.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792b81516e434469750b4ddd667bf6ddb82df31f4f13f82588d281f743bc8835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921039"
---
# <a name="plsa_client_request"></a>\_PLSA-CLIENTANFORDERUNG \_

Der **PLSA \_ CLIENT \_ REQUEST-Datentyp** ist ein nicht transparenter Datentyp.

Die [*lokale Sicherheitsautorität (Local Security Authority,*](../secgloss/l-gly.md) LSA) verwendet sie intern, um Clientinformationen im Zusammenhang mit einzelnen Anforderungen zu verwalten.


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntsecpkg.h</dt> </dl> |



 

 
