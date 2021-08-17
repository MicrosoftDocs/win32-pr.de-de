---
description: Benachrichtigt die IShellView, wenn eines ihrer Objekte als Ergebnis eines Menübefehls in der Zwischenablage platziert wird. Wird von SHShellFolderView \_ Message verwendet.
title: SFVM_SETCLIPBOARD Meldung (Shlobj.h)
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
ms.openlocfilehash: 99548be90c7f4fb9b840e4d4c6f816710c6e02cc1a888ce0c1c774f73c58f668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858212"
---
# <a name="sfvm_setclipboard-message"></a>SFVM \_ SETCLIPBOARD-Meldung

Benachrichtigt die [**IShellView,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) wenn eines ihrer Objekte als Ergebnis eines Menübefehls in der Zwischenablage platziert wird. Wird von [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwEffect* \[ In\]
</dt> <dd>

Verwenden Sie (WPARAM)-2, wenn das Element in die Zwischenablage ausgeschnitten wird, oder (WPARAM)-3, wenn das Element in die Zwischenablage kopiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




