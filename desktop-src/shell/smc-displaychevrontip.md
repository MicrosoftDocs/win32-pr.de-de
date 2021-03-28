---
description: Benachrichtigt Sie, dass ein Infotipp für das Chevron angezeigt wird, das dem von der zugehörigen smdata-Struktur angegebenen Element zugeordnet ist.
title: SMC_DISPLAYCHEVRONTIP Meldung (shobjidl. h)
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
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485507"
---
# <a name="smc_displaychevrontip-message"></a>SMC \_ displaychevrontip-Meldung

Benachrichtigt Sie, dass ein Infotipp für das Chevron angezeigt wird, das dem von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebenen Element zugeordnet ist.


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Parameter

Diese Nachricht weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Gibt "S OK" zurück \_ , um den infotip anzuzeigen. Gibt den Wert "false" zurück \_ , um zu verhindern, dass InfoTipp angezeigt wird.

## <a name="remarks"></a>Bemerkungen

Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




