---
description: Entfernt ein Objekt aus der Shellansicht. Wird von SHShellFolderView \_ Message verwendet.
title: SFVM_REMOVEOBJECT (Shlobj.h)
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
ms.openlocfilehash: d5bb53da276e28d7598961cc8f68a2464f414db9a3eac2ddab769102149bf370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941950"
---
# <a name="sfvm_removeobject-message"></a>SFVM \_ REMOVEOBJECT-Meldung

Entfernt ein Objekt aus der Shellansicht. Wird von [**SHShellFolderView Message \_ verwendet.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidl* \[ In\]
</dt> <dd>PIDL des zu entfernenden Objekts.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, das entfernt wurde, wenn ein Element gefunden wurde, das mit der angegebenen PIDL übereinstimmen. andernfalls wird -1 zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




