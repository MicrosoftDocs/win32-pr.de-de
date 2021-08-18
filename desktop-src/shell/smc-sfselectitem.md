---
description: Der Benutzer hat das von der zugehörigen SMDATA-Struktur angegebene Element ausgewählt.
title: SMC_SFSELECTITEM (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 82c3dfca-98a8-43ca-bebc-85bfdf640d38
api_name:
- SMC_SFSELECTITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eafe0e910c9c0b934dac7d11219869245a619564909968c39a95cd2ae1484f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118046846"
---
# <a name="smc_sfselectitem-message"></a>SMC \_ SFSELECTITEM-Nachricht

Der Benutzer hat das von der zugehörigen [**SMDATA-Struktur**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) angegebene Element ausgewählt.


```C++
SMC_SFSELECTITEM
            
```



## <a name="parameters"></a>Parameter

Diese Meldung enthält keine Parameter.

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



 

 




