---
description: Ein undurchsichtiger Datentyp.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216207"
---
# <a name="plsa_client_request"></a>plsa- \_ Client \_ Anforderung

Der Datentyp der **plsa- \_ Client \_ Anforderung** ist ein undurchsichtiger Datentyp.

Die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) verwendet diese intern, um Client Informationen zu einzelnen Anforderungen zu verwalten.


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntsecpkg. h</dt> </dl> |



 

 
