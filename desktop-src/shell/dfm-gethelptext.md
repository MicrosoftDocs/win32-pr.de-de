---
description: 'DFM_GETHELPTEXT Meldung: Ermöglicht dem Rückrufobjekt das Angeben einer Hilfetextzeichenfolge.'
title: DFM_GETHELPTEXT (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2428fe6696ff5949a0b25487437c8f3408b95f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097068"
---
# <a name="dfm_gethelptext-message"></a>DFM \_ GETHELPTEXT-Nachricht

Ermöglicht dem Rückrufobjekt das Angeben einer Hilfetextzeichenfolge.


```C++
DFM_GETHELPTEXT 

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

Eine AUF NULL beendete ANSI-Zeichenfolge, die den Hilfetext enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt erstellt wird. Es gibt zwei APIs für die Erstellung: [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen für den Rückruf zur Verfügung. Verwenden **Sie DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DFM \_ GETHELPTEXT** (ANSI)<br/>                                              |



 

 




