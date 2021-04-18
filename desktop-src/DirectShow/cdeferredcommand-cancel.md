---
description: 'Die Cancel-Methode bricht eine zuvor in die Warteschlange eingereihte cdeferredcommand:: Aufrufen-Anforderung ab.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Cdeferredcommand. Cancel-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364475"
---
# <a name="cdeferredcommandcancel-method"></a>Cdeferredcommand. Cancel-Methode

Die- `Cancel` Methode bricht eine zuvor in die Warteschlange eingereihte [**cdeferredcommand:: Aufrufen**](cdeferredcommand-invoke.md) -Anforderung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt VFW E zurück, die \_ \_ bereits \_ abgebrochen wurde, wenn **m \_ pqueue** **null** ist. Gibt ein **HRESULT** aus [**ccmdqueue:: Remove**](ccmdqueue-remove.md) zurück, wenn der-Befehl einen Fehler generiert. Gibt \_ bei Erfolg S OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die [**ideferredcommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdeferredcommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




