---
description: Benachrichtigt eine appbar, wenn eine Vollbildanwendung geöffnet oder geschlossen wird. Diese Benachrichtigung wird in Form einer von der Anwendung definierten Nachricht gesendet, die von der neuen ABM-Nachricht festgelegt wird \_ .
title: ABN_FULLSCREENAPP Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128476"
---
# <a name="abn_fullscreenapp-message"></a>ABN \_ fullscreenapp-Nachricht

Benachrichtigt eine appbar, wenn eine Vollbildanwendung geöffnet oder geschlossen wird. Diese Benachrichtigung wird in Form einer von der Anwendung definierten Nachricht gesendet, die von der [**\_ neuen ABM**](abm-new.md) -Nachricht festgelegt wird.


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fOpen* 
</dt> <dd>

Ein Flag, das angibt, ob eine Vollbildanwendung geöffnet oder geschlossen wird. Dieser Parameter ist " **true** ", wenn die Anwendung geöffnet wird, oder " **false** ", wenn Sie geschlossen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn eine Vollbildanwendung geöffnet wird, muss eine appbar am Ende der z-Reihenfolge ablegen. Beim Schließen sollte die appbar die Position der z-Reihenfolge wiederherstellen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




