---
description: Die OnError-Methode wird aufgerufen, wenn während des Streamings ein Fehler auftritt. Die abgeleitete Klasse muss diese Methode implementieren.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: CPullPin.OnError-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0d9873e2d327c424b2cd1ffda7112676f53399a63d2a9ca92dca1f50a02f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908880"
---
# <a name="cpullpinonerror-method"></a>CPullPin.OnError-Methode

Die `OnError` -Methode wird aufgerufen, wenn während des Streamings ein Fehler auftritt. Die abgeleitete Klasse muss diese Methode implementieren.

## <a name="syntax"></a>Syntax


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Std.* 
</dt> <dd>

Gibt den **HRESULT-Wert** an, der von der fehlgeschlagenen Methode zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das -Objekt ruft diese Methode auf, wenn ein Fehler auftritt, der den Daten-Pullthread an hält. Der Filter kann diese Methode verwenden, um streamingfehler ordnungsgemäß wiederhergestellt zu werden. In den meisten Fällen wird der Fehler vom Upstreamfilter zurückgegeben, sodass der Upstreamfilter dafür verantwortlich ist, ihn an den Filter Graph Manager zu melden. Wenn der Fehler innerhalb der [**CPullPin::Receive-Methode**](cpullpin-receive.md) auftritt, sollte Ihr Filter ein [**EC \_ ERRORABORT-Ereignis**](ec-errorabort.md) senden. (Siehe [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




