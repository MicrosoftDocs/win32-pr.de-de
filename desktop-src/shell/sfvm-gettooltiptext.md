---
description: 'Ermöglicht dem Rückruf Objekt, eine QuickInfo-Text Zeichenfolge für Menü Elemente oder Symbolleisten-Schaltflächen anzugeben. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: SFVM_GETTOOLTIPTEXT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960767"
---
# <a name="sfvm_gettooltiptext-message"></a>Sfvm \_ GetToolTipText-Nachricht

Ermöglicht dem Rückruf Objekt, eine QuickInfo-Text Zeichenfolge für Menü Elemente oder Symbolleisten-Schaltflächen anzugeben. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idcmd \_ cchmax* \[ in\]
</dt> <dd>

Das nieder wertige Wort dieses Parameters enthält die Befehls-ID. Das höchst wertige Wort enthält die Anzahl der Zeichen im *pszText* -Puffer.

</dd> <dt>

*pszText* \[ vorgenommen\]
</dt> <dd>

Eine mit NULL endenden Zeichenfolge, die den Hilfetext enthält.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
