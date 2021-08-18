---
description: Die WaitDispatchingMessages-Funktion wartet, bis ein Objekt signalisiert wird, während Fenstermeldungen gesendet werden.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: WaitDispatchingMessages-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26442633d1a4d5187b5e53ae53e0a898f759f91dc3719f09715b570108b701f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071904"
---
# <a name="waitdispatchingmessages-function"></a>WaitDispatchingMessages-Funktion

Die `WaitDispatchingMessages` Funktion wartet, bis ein Objekt signalisiert wird, während Fenstermeldungen gesendet werden.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hObject* 
</dt> <dd>

Handle des Objekts, auf das gewartet werden soll.

</dd> <dt>

*dwWait* 
</dt> <dd>

Time out interval ,in milliseconds. (Time out interval in milliseconds(Time out-Intervall in Millisekunden))

</dd> <dt>

*Hwnd* 
</dt> <dd>

Optionales Handle für ein Fenster.

</dd> <dt>

*uMsg* 
</dt> <dd>

Optionale Fenstermeldung mit Angabe einer zu sendenden Nachricht.

</dd> <dt>

*hEvent* 
</dt> <dd>

Optionales Handle für ein Ereignis, auf das gewartet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert der **WaitForMultipleObjects-Funktion** zurück.

## <a name="remarks"></a>Hinweise

Wenn ein Objekt ein Fenster besitzt, sollte es Während des Wartens Fenstermeldungen senden. Diese Funktion ermöglicht es dem Objekt, beim Senden von Nachrichten auf ein Ereignis, ein Semaphor oder ein anderes Objekt für gegenseitigen Ausschluss zu warten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verschiedene Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




