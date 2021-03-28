---
description: Ermöglicht dem Rückruf, Elemente am unteren Rand des erweiterten Menüs hinzuzufügen.
title: DFM_MERGECONTEXTMENU_BOTTOM Meldung (shlobj. h)
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
ms.openlocfilehash: b9274a36f531e53f86d05adab20b4970ea5ace84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977281"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a>DFM- \_ mergecontextmenu- \_ untere Meldung

Ermöglicht dem Rückruf, Elemente am unteren Rand des erweiterten Menüs hinzuzufügen.


```C++
DFM_MERGECONTEXTMENU_BOTTOM

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pqcminfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**qcminfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) -Struktur, die die Informationen enthält, die in der Zusammenführung verwendet werden.

</dd> <dt>

*uFlags* \[ in\]
</dt> <dd>

Flags, die angeben, wie das Kontextmenü geändert werden kann. Dieser Parameter verwendet die CMF-Werte, die \_ \* in [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)beschrieben werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn dem erweiterten Kontextmenü Elemente hinzugefügt werden, müssen Sie mit Routinen unterstützt werden, die entsprechend reagieren, wenn eines dieser Elemente mithilfe von [**DFM \_ InvokeCommand**](dfm-invokecommand.md)aufgerufen wird.

Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das standardmäßige Kontextmenü Objekt erstellt wird. Es gibt zwei APIs für die Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf. Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




