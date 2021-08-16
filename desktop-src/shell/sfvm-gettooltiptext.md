---
description: Ermöglicht es dem Rückrufobjekt, eine QuickInfo-Textzeichenfolge für Menüelemente oder Symbolleistenschaltflächen anzugeben. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: SFVM_GETTOOLTIPTEXT (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3350d1f772cd78c97f7b57b47084c761808583dfe5396fafcdad336291a3a717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858222"
---
# <a name="sfvm_gettooltiptext-message"></a>SFVM \_ GETTOOLTIPTEXT-Nachricht

Ermöglicht es dem Rückrufobjekt, eine QuickInfo-Textzeichenfolge für Menüelemente oder Symbolleistenschaltflächen anzugeben. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idCmd \_ cchMax* \[ in\]
</dt> <dd>

Das niedrige Wort dieses Parameters enthält die Befehls-ID. Das obere Wort enthält die Anzahl der Zeichen im *pszText-Puffer.*

</dd> <dt>

*pszText* \[ out\]
</dt> <dd>

Eine auf NULL beendete Zeichenfolge, die den Hilfetext enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
