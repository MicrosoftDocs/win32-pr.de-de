---
description: Fordert an, ob es akzeptabel ist, ein Datenobjekt für das Element zu löschen, das von der zugehörigen SMDATA-Struktur angegeben wird.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: SMC_SFDDRESTRICTED Nachricht (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edade5e240041979eeceeea29d42c67c38508492987d7e485e5d617a641eb581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046913"
---
# <a name="smc_sfddrestricted-message"></a>SMC \_ SFDDRESTRICTED-Nachricht

Fordert an, ob es akzeptabel ist, ein Datenobjekt für das Element zu löschen, das von der zugehörigen [**SMDATA-Struktur**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) angegeben wird.


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDropTarget* 
</dt> <dd>

Die Adresse eines void-Zeigers, der einen Zeiger auf Ihre [**IDropTarget-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) empfängt. Legen Sie diesen Wert auf **NULL** fest, wenn Sie das Datenobjekt nicht akzeptieren möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Benachrichtigung wird von der [**IShellMenuCallback::CallbackSM-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 
