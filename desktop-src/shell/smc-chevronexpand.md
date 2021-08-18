---
description: Der Benutzer hat auf ein Chevron geklickt, um das von der zugehörigen SMDATA-Struktur angegebene Element zu erweitern.
title: SMC_CHEVRONEXPAND Nachricht (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 036c45c6bd0e156a17cbcf2f89d3f64b2f619d4b4a6eb7e0a19b70eb3295292c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968249"
---
# <a name="smc_chevronexpand-message"></a>\_SMC-CHEVRONEXPAND-Nachricht

Der Benutzer hat auf ein Chevron geklickt, um das von der zugehörigen [**SMDATA-Struktur**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) angegebene Element zu erweitern.


```C++
SMC_CHEVRONEXPAND
            
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



 

 




