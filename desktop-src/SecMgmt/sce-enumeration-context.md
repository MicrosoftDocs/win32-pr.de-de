---
description: Der SCE- \_ \_ EnumerationContext-Datentyp ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird. Sie wird von der pfsce- \_ Abfrage \_ Info-Funktion verwendet, um durch die Sicherheitsdatenbank zu navigieren.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343118"
---
# <a name="sce_enumeration_context"></a>SCE- \_ \_ enumerationskontext

Der **SCE- \_ EnumerationContext \_** -Datentyp ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird. Sie wird von der [**pfsce- \_ Abfrage \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) -Funktion verwendet, um durch die Sicherheitsdatenbank zu navigieren.


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

