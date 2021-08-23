---
description: Benachrichtigt das Rückrufobjekt, dass der Benutzer auf eine Spaltenüberschrift geklickt hat, um die Liste der Objekte in der Ordneransicht zu sortieren. Wird von IShellFolderViewCB::MessageSFVCB verwendet.
title: SFVM_COLUMNCLICK Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d5ebd98ebc887d26bcee4799ffa3412df803fd0dfa099ac41bc69e1c25d83f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592700"
---
# <a name="sfvm_columnclick-message"></a>SFVM \_ COLUMNCLICK-Nachricht

Benachrichtigt das Rückrufobjekt, dass der Benutzer auf eine Spaltenüberschrift geklickt hat, um die Liste der Objekte in der Ordneransicht zu sortieren. Wird von [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iColumn* \[ In\]
</dt> <dd>

Der Index der Spalte, auf die geklickt wurde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Als Reaktion auf diese Benachrichtigung sollten Sie S OK zurückgeben, \_ um die Liste selbst neu anzuordnen. Damit das Objekt der Systemordneransicht die Liste neu anordnen kann, geben Sie S \_ FALSE zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
