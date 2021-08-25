---
description: Benachrichtigt die IShellView, ihre Elemente neu anzuordnen. Wird von SHShellFolderView \_ Message verwendet.
title: SFVM_REARRANGE Meldung (Shlobj.h)
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
ms.openlocfilehash: 03bb5b8d39a85d8ce4fb6e76b75967a642361f502ce3bcb20ca49f276a5221de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941980"
---
# <a name="sfvm_rearrange-message"></a>\_SFVM-NACHRICHT "REARRANGE"

Benachrichtigt die [**IShellView,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) ihre Elemente neu anzuordnen. Wird von [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* \[ In\]
</dt> <dd>

Wird an [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids)übergeben. Weitere Informationen zu diesem Parameter finden Sie unter [**IShellFolder::CompareIDs.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




