---
description: Ermöglicht dem Rückruf das Hinzufügen von Elementen am unteren Rand des erweiterten Menüs.
title: DFM_MERGECONTEXTMENU_BOTTOM (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 37414335-4f3c-461e-bd05-d6ef850f972a
api_name:
- DFM_MERGECONTEXTMENU_BOTTOM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11dade0f4b9526fa3c384f612b2c23eb77b437ef361d16c2adffc0a49df2ca28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111840"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a>DFM \_ MERGECONTEXTMENU \_ BOTTOM-Meldung

Ermöglicht dem Rückruf das Hinzufügen von Elementen am unteren Rand des erweiterten Menüs.


```C++
DFM_MERGECONTEXTMENU_BOTTOM

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

Flags, die angeben, wie das Kontextmenü geändert werden kann. Dieser Parameter verwendet die in \_ \* [**IContextMenu::QueryContextMenu beschriebenen CMF-Werte.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Elemente dem erweiterten Kontextmenü hinzugefügt werden, müssen sie mit Routinen unterstützt werden, die angemessen reagieren, wenn eines dieser Elemente mitHILFE von [**DFM \_ INVOKECOMMAND aufgerufen wird.**](dfm-invokecommand.md)

Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt erstellt wird. Es gibt zwei APIs für die Erstellung: [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen für den Rückruf zur Verfügung. Verwenden **Sie DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




