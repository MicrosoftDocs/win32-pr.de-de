---
description: Benachrichtigt das Rückrufobjekt, dass einer seiner Symbolleisten- oder Menübefehle vom Benutzer aufgerufen wurde. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: SFVM_INVOKECOMMAND (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b33eba78e0680fe940569c7a7ccfb4a27c61c3ffcb6eead0f2ff6436ec74f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968649"
---
# <a name="sfvm_invokecommand-message"></a>SFVM \_ INVOKECOMMAND-Nachricht

Benachrichtigt das Rückrufobjekt, dass einer seiner Symbolleisten- oder Menübefehle vom Benutzer aufgerufen wurde. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idCmd* \[ in\]
</dt> <dd>

Die Befehls-ID der ausgewählten Symbolleiste oder des ausgewählten Menüelements.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Meldung dient im Wesentlichen der gleichen Funktion wie eine [**WM \_ COMMAND-Nachricht**](../menurc/wm-command.md) in einer herkömmlichen Fensterprozedur. Sie ermöglicht es dem Rückrufobjekt, alle Elemente zu verarbeiten, die es dem Windows Explorer-Tool oder der Menüleiste hinzugefügt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
