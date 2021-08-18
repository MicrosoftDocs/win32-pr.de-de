---
description: Fordert den Titel und Text für eine Chevron-Infotip für das Element an, das von der zugehörigen SMDATA-Struktur angegeben wird.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: SMC_CHEVRONGETTIP Nachricht (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e64636994743d4b13a96fe75947fb515c4dbd3edcc94e6dee0fa85efb8bc9d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968239"
---
# <a name="smc_chevrongettip-message"></a>\_SMC-CHEVRONGETTIP-Nachricht

Fordert den Titel und Text für eine Chevron-Infotip für das Element an, das von der zugehörigen [**SMDATA-Struktur**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) angegeben wird.


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszTipTitle* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine **Mit NULL** endende Unicode-Zeichenfolge empfängt, die den Titel der Infotip enthält. Diese Zeichenfolge darf nicht länger als MAX \_ PATH-Zeichen sein, einschließlich des abschließenden **NULL-Zeichens.**

</dd> <dt>

*pwszTipText* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine **mit NULL** beendete Unicode-Zeichenfolge empfängt, die den Text der Infotip enthält. Diese Zeichenfolge darf nicht länger als MAX \_ PATH-Zeichen sein, einschließlich des abschließenden **NULL-Zeichens.**

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



 

 




