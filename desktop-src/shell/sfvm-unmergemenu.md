---
description: 'Benachrichtigt das Rückruf Objekt, dass ein Menü entfernt wird. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_UNMERGEMENU Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980816"
---
# <a name="sfvm_unmergemenu-message"></a>Sfvm \_ unmergemenu-Meldung

Benachrichtigt das Rückruf Objekt, dass ein Menü entfernt wird. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmenucurrent* \[ in\]
</dt> <dd>

Das Handle des Menüs, das entfernt wird.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
