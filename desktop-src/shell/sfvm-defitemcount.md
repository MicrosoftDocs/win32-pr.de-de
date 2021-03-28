---
description: 'Ermöglicht dem Rückruf Objekt, die Anzahl der Elemente in der Ordneransicht anzugeben. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_DEFITEMCOUNT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e3f746e422428ab9f925cf4ff3f460ccd578367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959995"
---
# <a name="sfvm_defitemcount-message"></a>Sfvm- \_ defitemcount-Nachricht

Ermöglicht dem Rückruf Objekt, die Anzahl der Elemente in der Ordneransicht anzugeben. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cItems* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Elemente in der Ordneransicht.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
