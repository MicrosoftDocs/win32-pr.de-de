---
description: Ermöglicht dem Rückruf das Hinzufügen von Elementen am oberen Rand des erweiterten Menüs.
title: DFM_MERGECONTEXTMENU_TOP Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eed6aec6-11a0-4738-b5b9-a455d0e35eac
api_name:
- DFM_MERGECONTEXTMENU_TOP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4cafbbe7331242e65e27137a1b5b78da6b8c6086c8326f96bbc32520366d10a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351120"
---
# <a name="dfm_mergecontextmenu_top-message"></a>DFM \_ MERGECONTEXTMENU \_ TOP-Nachricht

Ermöglicht dem Rückruf das Hinzufügen von Elementen am oberen Rand des erweiterten Menüs.


```C++
DFM_MERGECONTEXTMENU_TOP

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

Wenn Dem erweiterten Kontextmenü Elemente hinzugefügt werden, müssen sie mit Routinen unterstützt werden, die entsprechend reagieren, wenn eines dieser Elemente mit [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md)aufgerufen wird.

Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt implementiert wird. Es gibt zwei APIs für die Implementierung: [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen zum Rückruf bereit. Verwenden Sie **DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




