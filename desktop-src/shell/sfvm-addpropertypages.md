---
description: 'Ermöglicht dem Rückruf Objekt, eine Seite bereitzustellen, die dem Eigenschaften Blatt Eigenschaften des ausgewählten Objekts hinzugefügt werden kann. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_ADDPROPERTYPAGES Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994886"
---
# <a name="sfvm_addpropertypages-message"></a>Sfvm \_ addpropertypages-Meldung

Ermöglicht dem Rückruf Objekt, eine Seite bereitzustellen, die dem **Eigenschaften Blatt Eigenschaften** des ausgewählten Objekts hinzugefügt werden kann. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer [**sfvm- \_ PropPage- \_ Daten**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Meldung dient im wesentlichen derselben Funktion wie [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Weitere Erläuterungen finden Sie unter [Erstellen von Eigenschaften Blatt Handlern](propsheet-handlers.md) .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
