---
description: Stufen Sie das Element herab, das von der zugehörigen SMDATA-Struktur angegeben wird.
title: SMC_DEMOTE Nachricht (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c0f44f3de3b39d358bd90a758dfe7c9abe13182bc4eee2b06beddeb258550af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968189"
---
# <a name="smc_demote-message"></a>SMC \_ DEMOTE-Meldung

Stufen Sie das Element herab, das von der zugehörigen [**SMDATA-Struktur**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) angegeben wird.


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a>Parameter

Diese Nachricht enthält keine Parameter.

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



 

 




