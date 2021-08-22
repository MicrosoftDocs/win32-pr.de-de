---
description: Der SCE \_ ENUMERATION \_ CONTEXT-Datentyp ist ein nicht transparentes Handle, das vom Security Configuration-Toolsatz bereitgestellt wird. Sie wird von der PFSCE \_ QUERY \_ INFO-Funktion verwendet, um durch die Sicherheitsdatenbank zu navigieren.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (Scesvc.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b102c1eb2998f09dbe95c79c500e0bc66f4a790464071dbf9704a17a1348c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004998"
---
# <a name="sce_enumeration_context"></a>\_SCE-ENUMERATIONSKONTEXT \_

Der **SCE \_ ENUMERATION \_ CONTEXT-Datentyp** ist ein nicht transparentes Handle, das vom Security Configuration-Toolsatz bereitgestellt wird. Sie wird von der [**PFSCE \_ QUERY \_ INFO-Funktion**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) verwendet, um durch die Sicherheitsdatenbank zu navigieren.


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Scesvc.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_PFSCE-ABFRAGEINFORMATIONEN \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

