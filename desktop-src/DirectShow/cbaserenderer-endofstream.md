---
description: Die EndOfStream-Methode benachrichtigt den Filter, dass der Eingabepin eine Benachrichtigung vom Streamende empfangen hat.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: CBaseRenderer.EndOfStream-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ff047865aa4f52dee6c03411cddb0c957327851f0f6ca1b7a03f0b6adaacfe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822731"
---
# <a name="cbaserendererendofstream-method"></a>CBaseRenderer.EndOfStream-Methode

Die `EndOfStream` -Methode benachrichtigt den Filter, dass der Eingabepin eine Benachrichtigung vom Streamende empfangen hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Der Eingabepin des Filters ruft diese Methode auf, wenn er eine Benachrichtigung über das Ende des Streams empfängt.

Diese Methode legt das [**Flag CBaseRenderer::m \_ bEOS**](cbaserenderer-m-beos.md) auf **TRUE** fest und ruft die [**CBaseRenderer::SendEndOfStream-Methode**](cbaserenderer-sendendofstream.md) auf, um ein [**EC \_ COMPLETE-Ereignis**](ec-complete.md) zu planen. Wenn der Filter angehalten ist und auf ein Beispiel wartet, schließt diese Methode den Zustandsübergang ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




