---
description: Benachrichtigt eine App-Leiste, wenn eine Vollbildanwendung geöffnet oder geschlossen wird. Diese Benachrichtigung wird in Form einer anwendungsdefinierten Nachricht gesendet, die von der ABM \_ NEW-Nachricht festgelegt wird.
title: ABN_FULLSCREENAPP (Shellapi.h)
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
ms.openlocfilehash: 55bba51153ff90dfa69b870468a1c5002121eaccf45559821c6031aba35d4b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090790"
---
# <a name="abn_fullscreenapp-message"></a>ABN \_ FULLSCREENAPP-Nachricht

Benachrichtigt eine App-Leiste, wenn eine Vollbildanwendung geöffnet oder geschlossen wird. Diese Benachrichtigung wird in Form einer anwendungsdefinierten Nachricht gesendet, die von der [**ABM \_ NEW-Nachricht festgelegt**](abm-new.md) wird.


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fopen* 
</dt> <dd>

Ein Flag, das an gibt, ob eine Vollbildanwendung geöffnet oder geschlossen wird. Dieser Parameter ist **TRUE,** wenn die Anwendung geöffnet wird, oder **FALSE,** wenn sie geschlossen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn eine Vollbildanwendung geöffnet wird, muss eine App-Leiste unten in der Z-Reihenfolge angezeigt werden. Wenn sie geschlossen wird, sollte die App-Leiste ihre Position in der Z-Reihenfolge wiederherstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




