---
description: Benachrichtigt das Rückrufobjekt, dass das Ordneransichtsfenster erstellt wird. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
title: SFVM_WINDOWCREATED Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2d09957e1164d5caacbddc23c9a72cb33ef80ffa156dd0538c0be1e24f192018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111160"
---
# <a name="sfvm_windowcreated-message"></a>SFVM \_ WINDOWCREATED-Meldung

Benachrichtigt das Rückrufobjekt, dass das Ordneransichtsfenster erstellt wird. Wird von [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndView* \[ In\]
</dt> <dd>

Das Fensterhandle der Ordneransicht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
