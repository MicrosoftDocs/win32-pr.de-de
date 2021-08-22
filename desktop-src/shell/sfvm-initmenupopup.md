---
description: Ermöglicht es dem Rückrufobjekt, ein Popupmenü Windows Explorer zu ändern, bevor es angezeigt wird. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
title: SFVM_INITMENUPOPUP (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fd69d19f753c1c72c1e0c143a0aface2cdb234cb2ace8c87d559834b97bbf0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592316"
---
# <a name="sfvm_initmenupopup-message"></a>SFVM \_ INITMENUPOPUP-Meldung

Ermöglicht es dem Rückrufobjekt, ein Popupmenü Windows Explorer zu ändern, bevor es angezeigt wird. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idCmd \_ nIndex* \[ in\]
</dt> <dd>

Das niedrige Wort dieses Parameters enthält den Wert der ersten Befehls-ID, die für Clientbefehle reserviert ist. Das obere Wort enthält den Index des Menüs.

</dd> <dt>

*hmenu* \[ in, out\]
</dt> <dd>

Das Handle des Menüs.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Objekt der Systemordneransicht sendet diese Meldung, wenn ein Menü ausgewählt ist, aber bevor es angezeigt wird. Verarbeiten Sie diese Meldung, wenn Sie z. B. Menübefehle aktivieren oder deaktivieren müssen. Das Popupmenü kann wie im folgenden Menü angezeigt werden:

-   Das Menü Datei, Bearbeiten oder Ansicht.
-   Ein vom Client definiertes Menü der obersten Ebene.
-   Ein clientdefiniertes Untermenü.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SFVM \_ MERGEMENU**](sfvm-mergemenu.md)
</dt> </dl>

 

 
