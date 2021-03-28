---
description: 'Ermöglicht dem Rückruf Objekt das Angeben eines standardmäßigen Sortier Parameters. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_GETSORTDEFAULTS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980881"
---
# <a name="sfvm_getsortdefaults-message"></a>Sfvm \_ getsortdefaults-Meldung

Ermöglicht dem Rückruf Objekt das Angeben eines standardmäßigen Sortier Parameters. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idirection* \[ vorgenommen\]
</dt> <dd>

Die Standard Sortierrichtung. Legen Sie diesen Parameter auf einen positiven Wert fest, um in aufsteigender Reihenfolge zu sortieren. Legen Sie diesen Parameter auf NULL oder einen negativen Wert fest, um in absteigender Reihenfolge sortiert zu werden.

</dd> <dt>

*icolumn* \[ vorgenommen\]
</dt> <dd>

Die Spalte, die für die Sortierung verwendet wird. Diese wird an die [**IShellFolder:: compareids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in den unteren 16 Bits des *LPARAM* -Werts übermittelt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> : **Sfvm \_ getsortdefaults** wird vom Systemordner View-Objekt nicht erkannt.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
