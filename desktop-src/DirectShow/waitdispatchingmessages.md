---
description: Die waitdispatchingmessages-Funktion wartet darauf, dass ein Objekt signalisiert wird, während Fenster Meldungen verteilt werden.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Waitdispatchingmessages-Funktion (wxutil. h)
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
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351269"
---
# <a name="waitdispatchingmessages-function"></a>Waitdispatchingmessages-Funktion

Die- `WaitDispatchingMessages` Funktion wartet auf die Signalisierung eines Objekts während der Verteilung von Fenster Meldungen.

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

*hobject* 
</dt> <dd>

Handle des Objekts, auf das gewartet werden soll.

</dd> <dt>

*dwwait* 
</dt> <dd>

Timeout Intervall in Millisekunden.

</dd> <dt>

*HWND* 
</dt> <dd>

Optionales Handle für ein Fenster.

</dd> <dt>

*Umschlag* 
</dt> <dd>

Optionale Fenster Meldung, die eine zu Verteil dende Nachricht angibt.

</dd> <dt>

*hevent* 
</dt> <dd>

Optionales Handle für ein Ereignis, auf das gewartet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert aus der **WaitForMultipleObjects** -Funktion zurück.

## <a name="remarks"></a>Bemerkungen

Wenn ein Objekt ein Fenster besitzt, sollte es beim Warten Fenster Meldungen verteilen. Diese Funktion ermöglicht es dem-Objekt, während der Verteilung von Nachrichten auf ein Ereignis, ein Semaphor oder ein anderes gegenseitiges Ausschluss Objekt zu warten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Diverse Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




