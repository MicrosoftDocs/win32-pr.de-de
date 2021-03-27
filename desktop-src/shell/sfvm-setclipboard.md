---
description: Benachrichtigt ishellview, wenn eines der Objekte als Ergebnis eines Menübefehls in der Zwischenablage platziert wird. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_SETCLIPBOARD Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995158"
---
# <a name="sfvm_setclipboard-message"></a>Sfvm- \_ setClipboard-Nachricht

Benachrichtigt [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) , wenn eines der Objekte als Ergebnis eines Menübefehls in der Zwischenablage platziert wird. Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dweffect* \[ in\]
</dt> <dd>

Verwenden Sie (wParam)-2, wenn das Element in die Zwischenablage ausgeschnitten wird, oder (wParam)-3, wenn das Element in die Zwischenablage kopiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




