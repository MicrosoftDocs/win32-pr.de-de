---
description: Fordert Informationen zu einem Menü Element eines shellordners an.
title: SMC_GETSFINFO Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3a02b61565eb08f623978900d6ce47e30eea85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994838"
---
# <a name="smc_getsfinfo-message"></a>SMC \_ gezfinfo-Nachricht

Fordert Informationen zu einem Menü Element eines shellordners an.


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psminfo* 
</dt> <dd>

Zeiger auf eine [**sminfo**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) -Struktur. Füllen Sie die Struktur mit den entsprechenden Informationen aus, und geben Sie \_ OK zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "S OK" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




