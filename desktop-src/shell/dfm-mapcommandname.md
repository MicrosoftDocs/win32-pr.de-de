---
description: Wird von der standardmäßigen Kontextmenüimplementierungen gesendet, um einem Menübefehl einen Namen zuzuweisen.
title: DFM_MAPCOMMANDNAME Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3dac1cdb3c04397a59b26a2212fe1c46b611ce72ba029aabd25e0b01c9000b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459976"
---
# <a name="dfm_mapcommandname-message"></a>DFM \_ MAPCOMMANDNAME-Nachricht

Wird von der standardmäßigen Kontextmenüimplementierungen gesendet, um einem Menübefehl einen Namen zuzuweisen.


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*defaultID* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die ID des ausgewählten Menübefehls.

</dd> <dt>

*pszCommandName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen des Befehls enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt implementiert wird. Es gibt zwei APIs für die Implementierung: [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen zum Rückruf bereit. Verwenden Sie **DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




