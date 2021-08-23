---
description: Gibt das Standardsymbol für das Element zurück, das von der zugehörigen SMDATA-Struktur angegeben wird.
title: SMC_DEFAULTICON (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c0245cad585f461fbc1b22611b0a39a25ec0e6ac235bb29a490fdd47ba5e5979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968199"
---
# <a name="smc_defaulticon-message"></a>SMC \_ DEFAULTICON-Meldung

Gibt das Standardsymbol für das Element zurück, das von der zugehörigen [**SMDATA-Struktur angegeben**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) wird.


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszIcon* 
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den vollqualifizierten Pfad der Datei empfängt, die das Standardsymbol enthält.

</dd> <dt>

*iIcon* 
</dt> <dd>

Ein Zeiger auf eine ganze Zahl, die den Index des Symbols in der durch *pwszIcon angegebenen Datei empfängt.*

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



 

 




