---
description: 'Benachrichtigt das Rückruf Objekt, dass ein Ereignis aufgetreten ist, das sich auf eines seiner Elemente auswirkt. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_FSNOTIFY Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "104995222"
---
# <a name="sfvm_fsnotify-message"></a>Sfvm \_ fsnotify-Nachricht

Benachrichtigt das Rückruf Objekt, dass ein Ereignis aufgetreten ist, das sich auf eines seiner Elemente auswirkt. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppidl* \[ in\]
</dt> <dd>

Der Zeiger der PIDL des betroffenen Elements.

</dd> <dt>

*Levent* \[ in\]
</dt> <dd>

Ein shcne-Wert, der angibt, welches Ereignis aufgetreten ist. Eine Liste möglicher Werte finden Sie unter [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
