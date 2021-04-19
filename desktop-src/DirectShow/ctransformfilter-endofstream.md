---
description: Die EndOf Stream-Methode benachrichtigt den Filter, dass keine weiteren Daten von der Eingabe-PIN erwartet werden.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Ctransformfilter. EndOf Stream-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364660"
---
# <a name="ctransformfilterendofstream-method"></a>Ctransformfilter. EndOf Stream-Methode

Die- `EndOfStream` Methode benachrichtigt den Filter, dass keine zusätzlichen Daten von der eingabepin erwartet werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**ctransforminputpin:: endovstream**](ctransforminputpin-endofstream.md) -Methode der Eingabe-PIN ruft diese Methode auf. Diese Methode übermittelt die downstreambenachrichtigung. Wenn die abgeleitete Klasse einen Arbeits Thread zum Übermitteln von Medien Beispielen verwendet, sollte diese Methode überschrieben werden, und das Ende der Stream-Benachrichtigung wird in die Warteschlange eingereiht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




