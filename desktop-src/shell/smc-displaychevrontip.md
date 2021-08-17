---
description: Benachrichtigt Sie darüber, dass eine Infotip für das Chevron angezeigt wird, das dem element zugeordnet ist, das von der zugehörigen SMDATA-Struktur angegeben wird.
title: SMC_DISPLAYCHEVRONTIP Nachricht (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f1107af5cd621bafbc1e463101cee2ea57236b9d29844d6183963134b50ce3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968169"
---
# <a name="smc_displaychevrontip-message"></a>SMC \_ DISPLAYCHEVRONTIP-Nachricht

Benachrichtigt Sie, dass eine Infotip für das Chevron angezeigt wird, das dem element zugeordnet ist, das von der zugehörigen [**SMDATA-Struktur**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) angegeben wird.


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Parameter

Diese Nachricht enthält keine Parameter.

## <a name="return-value"></a>Rückgabewert

Geben Sie S \_ OK zurück, um die Infotip anzuzeigen. Gibt S \_ FALSE zurück, um zu verhindern, dass die Infotip angezeigt wird.

## <a name="remarks"></a>Hinweise

Diese Benachrichtigung wird von der [**IShellMenuCallback::CallbackSM-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




