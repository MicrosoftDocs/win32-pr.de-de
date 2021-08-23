---
description: Ermöglicht es dem Rückrufobjekt, eine Hilfetextzeichenfolge für Menüelemente oder Symbolleistenschaltflächen anzugeben. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
title: SFVM_GETHELPTEXT (Shlobj.h)
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
ms.openlocfilehash: c015c1999cbd60174da1994d92766b4f334630294767ee390be21340aef97cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661020"
---
# <a name="sfvm_gethelptext-message"></a>SFVM \_ GETHELPTEXT-Nachricht

Ermöglicht es dem Rückrufobjekt, eine Hilfetextzeichenfolge für Menüelemente oder Symbolleistenschaltflächen anzugeben. Wird von [**IShellFolderViewCB::MessageSFVCB verwendet.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETHELPTEXT 

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



 

 
