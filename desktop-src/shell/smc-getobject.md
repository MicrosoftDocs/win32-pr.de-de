---
description: 'SMC_GETOBJECT: Fordert einen Zeiger auf ein angegebenes Objekt an.'
title: SMC_GETOBJECT (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 693159f44d3b8878e2b70b9878ced5234c51e79110de8771d57a1c59a22feb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047082"
---
# <a name="smc_getobject-message"></a>SMC \_ GETOBJECT-Nachricht

Fordert einen Zeiger auf ein angegebenes Objekt an.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Iid* 
</dt> <dd>

Die IID, die dem angeforderten Objekt zugeordnet ist.

</dd> <dt>

*Pv* 
</dt> <dd>

Ein void-Zeiger, der einen Zeiger auf die angeforderte Schnittstelle empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Benachrichtigung wird von der [**IShellMenuCallback::CallbackSM-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) empfangen. Erstellen Sie das angeforderte Objekt, und weisen Sie pv einen Zeiger auf die angeforderte Schnittstelle *zu.*

Die folgenden Schnittstellen können angefordert werden.

-   [**IShellMenu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [**IShellMenuCallback**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [**Idroptarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 
