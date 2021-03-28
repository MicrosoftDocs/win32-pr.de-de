---
description: Gibt das Standard Symbol für das Element zurück, das durch die zugehörige smdata-Struktur angegeben wird.
title: SMC_DEFAULTICON Meldung (shobjidl. h)
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
ms.openlocfilehash: 10edab26c87dae4b1c9d2d5f06390fc608ba1edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994854"
---
# <a name="smc_defaulticon-message"></a>SMC- \_ DefaultIcon-Nachricht

Gibt das Standard Symbol für das Element zurück, das durch die zugehörige [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegeben wird.


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszicon* 
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den voll qualifizierten Pfad der Datei empfängt, die das Standard Symbol enthält.

</dd> <dt>

*Symbols* 
</dt> <dd>

Ein Zeiger auf eine Ganzzahl, die den Index des Symbols in der durch *pwszicon* angegebenen Datei empfängt.

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



 

 




