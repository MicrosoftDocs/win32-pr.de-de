---
description: Ermöglicht dem Rückrufobjekt das Anfordern einer Enumeration in einem Hintergrundthread. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
title: SFVM_BACKGROUNDENUM (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 724f971f52b57a008ec17ac316b78839a6890e3e2efee5d5a037ab4fdcd7ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592740"
---
# <a name="sfvm_backgroundenum-message"></a>SFVM \_ BACKGROUNDENUM-Meldung

Ermöglicht dem Rückrufobjekt das Anfordern einer Enumeration in einem Hintergrundthread. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Parameter

Diese Meldung enthält keine Parameter.

## <a name="remarks"></a>Hinweise

Geben Sie als Reaktion auf diese Benachrichtigung S \_ OK zurück, um die Hintergrundenumeration zu aktivieren. Standardmäßig zeigt das Systemordnerobjekt die "Taschenlampenanimation" an, während die Enumeration stattfindet. Um eine benutzerdefinierte Animation anzugeben, behandeln [**Sie SFVM \_ GETANIMATION**](sfvm-getanimation.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
