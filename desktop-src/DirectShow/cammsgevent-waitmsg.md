---
description: Die waitmsg-Methode wartet darauf, dass das Ereignis signalisiert wird, während gesendete Nachrichten versendet werden.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Cammsgevent. waitmsg-Methode (wxutil. h)
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
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360383"
---
# <a name="cammsgeventwaitmsg-method"></a>Cammsgevent. waitmsg-Methode

Die- `WaitMsg` Methode wartet, bis das-Ereignis signalisiert wird, während gesendete Nachrichten versendet werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwtimeout* 
</dt> <dd>

Optionaler Timeout Wert in Millisekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn das Ereignis signalisiert wird, oder " **false** ", wenn das Timeout aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die Funktion "Peer Message" auf, um Nachrichten zu verarbeiten. Diese Methode wird anstelle von " [**camevent:: Wait**](camevent-wait.md) " aufgerufen, wenn der Thread beim Warten auf ein Ereignis Nachrichten verarbeiten muss. Wenn der Thread keine Nachrichten verarbeitet und ein anderer Thread eine Nachricht sendet, kann ein Deadlock auftreten.

Nehmen Sie beispielsweise an, Sie erstellen einen Thread und blockieren dann, bis der Thread initialisiert wird. Wenn der Thread durch Aufrufen der SendMessage-Funktion eine Nachricht an das Fenster sendet, führt dies zu einem Deadlock. Dies liegt daran, dass SendMessage erst zurückgegeben wird, wenn die Nachricht verarbeitet wurde. Durch den Aufruf von waitmsg kann der SendMessage-Aufruf zurückgegeben werden, wodurch der Deadlock verhindert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cammsgevent-Klasse**](cammsgevent.md)
</dt> </dl>

 

 




