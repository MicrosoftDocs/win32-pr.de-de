---
description: 'SMC_GETSFOBJECT: Fordert einen Zeiger auf ein angegebenes Objekt an.'
title: SMC_GETSFOBJECT (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0b0b5e9e170c9df4bd89279f2b96c80a76002ba2adbbe14ebd90afe458ece161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047072"
---
# <a name="smc_getsfobject-message"></a>SMC \_ GETSFOBJECT-Nachricht

Fordert einen Zeiger auf ein angegebenes Objekt an.


```C++
SMC_GETSFOBJECT 
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

Diese Benachrichtigung wird von der [**IShellMenuCallback::CallbackSM-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) empfangen. Es ähnelt [**SMC \_ GETOBJECT,**](smc-getobject.md) wird aber für Shellordnerelemente verwendet. Erstellen Sie das angeforderte Objekt, und weisen Sie pv einen Zeiger auf die angeforderte Schnittstelle *zu.*

Die folgenden Schnittstellen können angefordert werden.

-   [**Istream**](/windows/win32/api/objidl/nn-objidl-istream)
-   [**IShellMenu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**IShellMenuCallback**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 
