---
description: Die WaitMsg-Methode wartet, bis das Ereignis signalisiert wird, während gesendete Nachrichten gesendet werden.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: CABMsgEvent.WaitMsg-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a2169d9938a8c2ff8a1961eee0895fefd7cc8a2dd487a4193d8053d27d98ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955449"
---
# <a name="cammsgeventwaitmsg-method"></a>CABMsgEvent.WaitMsg-Methode

Die `WaitMsg` -Methode wartet, bis das Ereignis signalisiert wird, während gesendete Nachrichten gesendet werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwTimeOut* 
</dt> <dd>

Optionaler Time out-Wert in Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn das Ereignis signalisiert wird, oder **FALSE,** wenn das Time out aufgetreten ist.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die PeekMessage-Funktion auf, um Nachrichten zu verarbeiten. Rufen Sie diese Methode anstelle von [**CABEvent::Wait**](camevent-wait.md) auf, wenn Ihr Thread Nachrichten verarbeiten muss, während auf ein Ereignis gewartet wird. Wenn der Thread keine Nachrichten verarbeitet und ein anderer Thread eine Nachricht sendet, kann ein Deadlock auftreten.

Angenommen, Sie erstellen einen Thread und blockieren dann, bis der Thread initialisiert wird. Wenn der Thread eine Nachricht durch Aufrufen der SendMessage-Funktion an Ihr Fenster sendet, führt dies zu einem Deadlock. Dies liegt daran, dass SendMessage erst dann zurückgegeben wird, wenn die Nachricht verarbeitet wurde. Durch Aufrufen von WaitMsg kann der SendMessage-Aufruf zurückgegeben werden, wodurch der Deadlock verhindert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMMsgEvent-Klasse**](cammsgevent.md)
</dt> </dl>

 

 




