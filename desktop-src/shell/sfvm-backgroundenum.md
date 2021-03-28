---
description: 'Ermöglicht dem Rückruf Objekt, Enumeration in einem Hintergrund Thread anzufordern. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_BACKGROUNDENUM Meldung (shlobj. h)
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
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994919"
---
# <a name="sfvm_backgroundenum-message"></a>Sfvm- \_ backgroundenum-Meldung

Ermöglicht dem Rückruf Objekt, Enumeration in einem Hintergrund Thread anzufordern. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Parameter

Diese Nachricht weist keine Parameter auf.

## <a name="remarks"></a>Bemerkungen

Geben Sie als Antwort auf diese Benachrichtigung S \_ OK ein, um die hintergrundenumeration zu aktivieren. Standardmäßig wird das Systemordner Objekt die Animation "Taschenlampe" anzeigen, während die Enumeration stattfindet. Um eine benutzerdefinierte Animation anzugeben, behandeln Sie [**sfvm \_ getanimation**](sfvm-getanimation.md).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
