---
description: 'Ermöglicht dem Rückruf Objekt das Zusammenführen von Menü Elementen in den Windows-Explorer-Menüs. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_MERGEMENU Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980832"
---
# <a name="sfvm_mergemenu-message"></a>Sfvm \_ MergeMenu-Meldung

Ermöglicht dem Rückruf Objekt das Zusammenführen von Menü Elementen in den Windows-Explorer-Menüs. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinfo* \[ vorgenommen\]
</dt> <dd>

Eine [**qcminfo**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) -Struktur, die die Informationen enthält, die erforderlich sind, um die Elemente im Menü zusammenzuführen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Nachricht dient im Wesentlichen dem gleichen Zweck wie [**ishellbrowser:: insertmenussb**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) und [**ishellbrowser:: setmenusb**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in einer benutzerdefinierten Ordneransicht. Weitere Informationen finden Sie im Abschnitt *Verwenden von ishellbrowser zum kommunizieren mit Windows-Explorer* unter [Implementieren einer Ordneransicht](../lwef/nse-folderview.md) .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
