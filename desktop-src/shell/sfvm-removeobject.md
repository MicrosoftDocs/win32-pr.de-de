---
description: Entfernt ein Objekt aus der shellansicht. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_REMOVEOBJECT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980888"
---
# <a name="sfvm_removeobject-message"></a>Sfvm- \_ removeobject-Nachricht

Entfernt ein Objekt aus der shellansicht. Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PIDL* \[ in\]
</dt> <dd>PIDL des zu entfernenden-Objekts.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, das entfernt wurde, wenn ein Element gefunden wurde, das mit der angegebenen PIDL übereinstimmt. Andernfalls wird-1 zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




