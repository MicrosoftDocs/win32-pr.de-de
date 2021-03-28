---
description: Fordert einen Zeiger auf ein angegebenes Objekt an.
title: SMC_GETSFOBJECT Meldung (shobjidl. h)
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
ms.openlocfilehash: c7fb57ea8e3f02ce4e773e187310530c14d65515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216826"
---
# <a name="smc_getsfobject-message"></a>SMC \_ gezfobject-Nachricht

Fordert einen Zeiger auf ein angegebenes Objekt an.


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IID* 
</dt> <dd>

Die dem angeforderten Objekt zugeordnete IID.

</dd> <dt>

*teuren* 
</dt> <dd>

Ein void-Zeiger, der einen Zeiger auf die angeforderte Schnittstelle empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "S OK" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen. Sie ähnelt der Verwendung von [**SMC \_ GetObject**](smc-getobject.md) , wird jedoch für shellordnerelemente verwendet. Erstellen Sie das angeforderte Objekt, und weisen Sie der angeforderten Schnittstelle einen Zeiger auf *PV* zu.

Die folgenden Schnittstellen können angefordert werden.

-   [**IStream**](/windows/win32/api/objidl/nn-objidl-istream)
-   [**Ishellmenu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**Ishellmenucallback**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 
