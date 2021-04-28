---
description: 'DFM_GETHELPTEXTW Meldung: Ermöglicht dem Rückrufobjekt das Angeben einer Hilfetextzeichenfolge.'
title: DFM_GETHELPTEXTW Nachricht (Shlobj.h)
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
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097038"
---
# <a name="dfm_gethelptextw-message"></a>DFM \_ GETHELPTEXTW-Nachricht

Ermöglicht es dem Rückrufobjekt, eine Hilfetextzeichenfolge anzugeben.


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idCmd \_ cchMax* \[ in\]
</dt> <dd>

Das Wort in niedriger Reihenfolge dieses Parameters enthält die Befehls-ID. Das Wort in hoher Reihenfolge enthält die Anzahl der Zeichen im *pszText-Puffer.*

</dd> <dt>

*pszText* \[ out\]
</dt> <dd>

Eine auf NULL endende Unicode-Zeichenfolge, die den Hilfetext enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt erstellt wird. Es gibt zwei APIs für die Erstellung: [**CDefFolderMenu \_ Create2,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) [**SHCreateDefaultContextMenu.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen zum Rückruf bereit. Verwenden Sie **DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DFM \_ GETHELPTEXTW** (Unicode)<br/>                                          |



 

 




