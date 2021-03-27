---
description: 'Ermöglicht dem Rückruf Objekt, eine HTML-Hilfedatei und ein Thema darin anzugeben. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_GETHELPTOPIC Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866779"
---
# <a name="sfvm_gethelptopic-message"></a>Sfvm \_ GetHelpTopic-Nachricht

Ermöglicht dem Rückruf Objekt, eine HTML-Hilfedatei und ein Thema darin anzugeben. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phtd* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer [**sfvm- \_ HelpTopic- \_ Daten**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) Struktur, die die HTML-Hilfedatei und das Thema angibt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
