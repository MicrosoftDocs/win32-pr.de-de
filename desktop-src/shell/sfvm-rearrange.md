---
description: Benachrichtigt die ishellview, ihre Elemente neu anzuordnen. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_REARRANGE Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050536"
---
# <a name="sfvm_rearrange-message"></a>Sfvm- \_ Nachricht neu anordnen

Benachrichtigt die [**ishellview**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) , ihre Elemente neu anzuordnen. Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LPARAM* \[ in\]
</dt> <dd>

An [**IShellFolder:: compareids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids)übermittelt. Weitere Informationen zu diesem Parameter finden Sie unter [**IShellFolder:: compareids**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




