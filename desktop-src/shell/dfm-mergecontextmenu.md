---
description: Ermöglicht dem Rückruf das Hinzufügen von Elementen zum Menü.
title: DFM_MERGECONTEXTMENU Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ddd071e40d3c017a513eb0e85efb634df530a8686afaf7df59b922602d37f22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455970"
---
# <a name="dfm_mergecontextmenu-message"></a>DFM \_ MERGECONTEXTMENU-Nachricht

Ermöglicht dem Rückruf das Hinzufügen von Elementen zum Menü.


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pqcminfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**QCMINFO-Struktur,**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) die die in der Zusammenführung verwendeten Informationen enthält.

</dd> <dt>

*uFlags* \[ In\]
</dt> <dd>

Flags, die angeben, wie das Kontextmenü geändert werden kann. Dieser Parameter verwendet die \_ \* cmf-Werte, die in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)beschrieben sind.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Dem Kontextmenü Elemente hinzugefügt werden, müssen sie mit Routinen unterstützt werden, die angemessen reagieren, wenn eines dieser Elemente mit [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md)aufgerufen wird.

Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt implementiert wird. Es gibt zwei APIs für die Implementierung: [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen zum Rückruf bereit. Verwenden Sie **DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




