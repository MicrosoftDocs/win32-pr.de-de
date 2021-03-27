---
description: Benachrichtigt Sie, das bestandene-Objekt zu speichern.
title: SMC_SETSFOBJECT Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216824"
---
# <a name="smc_setsfobject-message"></a>SMC- \_ Nachricht

Benachrichtigt Sie, das bestandene-Objekt zu speichern.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IID* 
</dt> <dd>

Die IID, die dem Objekt zugeordnet ist.

</dd> <dt>

*teuren* 
</dt> <dd>

Ein Zeiger auf die-Schnittstelle für das von *IID* angegebene Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "S OK" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.

Die **SMC \_** -Abmelde Benachrichtigung wird mit dem IID- \_ Stream verwendet. Das Objekt wird in einem persistenten Formular in der Registrierung gespeichert, und es wird nichts mit dem Verweis Zähler für das über gegebene Objekt ausgeführt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




