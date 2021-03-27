---
description: 'Ermöglicht dem Rückruf Objekt, eine Hilfe Text Zeichenfolge für Menü Elemente oder Symbolleisten-Schaltflächen anzugeben. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_GETHELPTEXT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757842"
---
# <a name="sfvm_gethelptext-message"></a>Sfvm- \_ GetHelpText-Nachricht

Ermöglicht dem Rückruf Objekt, eine Hilfe Text Zeichenfolge für Menü Elemente oder Symbolleisten-Schaltflächen anzugeben. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETHELPTEXT 

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



 

 
