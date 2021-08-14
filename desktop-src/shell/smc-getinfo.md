---
description: Fordert Informationen zu einem regulären Menüelement an.
title: SMC_GETINFO (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 95f27905a59fd8ce7c84cfc1166b59cb38356934b3603b0cec7f56c2365a3984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968109"
---
# <a name="smc_getinfo-message"></a>SMC \_ GETINFO-Nachricht

Fordert Informationen zu einem regulären Menüelement an.


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psminfo* 
</dt> <dd>

Ein Zeiger auf eine [**SMINFO-Struktur.**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) Füllen Sie die Struktur mit den entsprechenden Informationen aus, und geben Sie S \_ OK zurück.

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



 

 




