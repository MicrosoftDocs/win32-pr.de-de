---
description: 'DFM_GETHELPTEXTW Meldung: Ermöglicht dem Rückrufobjekt das Angeben einer Hilfetextzeichenfolge.'
title: DFM_GETHELPTEXTW (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6a7a5c47fcdb81accf4c2370aa14fa5f477be50b718b326631b20847db528151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860925"
---
# <a name="dfm_gethelptextw-message"></a>DFM \_ GETHELPTEXTW-Nachricht

Ermöglicht dem Rückrufobjekt das Angeben einer Hilfetextzeichenfolge.


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idCmd \_ cchMax* \[ in\]
</dt> <dd>

Das niedrige Wort dieses Parameters enthält die Befehls-ID. Das obere Wort enthält die Anzahl der Zeichen im *pszText-Puffer.*

</dd> <dt>

*pszText* \[ out\]
</dt> <dd>

Eine auf NULL beendete Unicode-Zeichenfolge, die den Hilfetext enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt erstellt wird. Es gibt zwei APIs für die Erstellung: [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen für den Rückruf zur Verfügung. Verwenden **Sie DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DFM \_ GETHELPTEXTW** (Unicode)<br/>                                          |



 

 




