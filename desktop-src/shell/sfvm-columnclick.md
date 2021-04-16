---
description: 'Benachrichtigt das Rückruf Objekt, dass der Benutzer auf einen Spaltenheader geklickt hat, um die Liste der Objekte in der Ordneransicht zu sortieren. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_COLUMNCLICK Meldung (shlobj. h)
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
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485515"
---
# <a name="sfvm_columnclick-message"></a>Sfvm- \_ ColumnClick-Nachricht

Benachrichtigt das Rückruf Objekt, dass der Benutzer auf einen Spaltenheader geklickt hat, um die Liste der Objekte in der Ordneransicht zu sortieren. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*icolumn* \[ in\]
</dt> <dd>

Der Index der Spalte, auf die geklickt wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Als Antwort auf diese Benachrichtigung sollten Sie S OK zurückgeben, \_ um die Liste selbst neu anzuordnen. Wenn das Ansichts Objekt des System Ordners die Liste neu anordnen soll, geben Sie "false" zurück \_ .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
