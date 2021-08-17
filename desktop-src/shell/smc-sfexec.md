---
description: Führen Sie das shell-Ordnerelement aus, das in der zugehörigen SMDATA-Struktur angegeben ist.
title: SMC_SFEXEC Nachricht (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e4d02763745a0ffb548777c92d14ee7928a29a58d6a46ff7c335ac0300f64bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967999"
---
# <a name="smc_sfexec-message"></a>SMC \_ SFEXEC-Nachricht

Führen Sie das shell-Ordnerelement aus, das in der zugehörigen [**SMDATA-Struktur**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) angegeben ist.


```C++
SMC_SFEXEC
            
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



 

 




