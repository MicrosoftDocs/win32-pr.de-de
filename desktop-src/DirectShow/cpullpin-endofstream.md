---
description: Die EndOfStream-Methode wird aufgerufen, nachdem das-Objekt das letzte Beispiel übermittelt hat. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Cpullpin. EndOf Stream-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366826"
---
# <a name="cpullpinendofstream-method"></a>Cpullpin. EndOf Stream-Methode

Die- `EndOfStream` Methode wird aufgerufen, nachdem das-Objekt das letzte Beispiel übermittelt hat. Diese Methode muss von der abgeleiteten Klasse implementiert werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) für jede Downstream-Eingabe-PIN aufzurufen, die Daten von diesem Objekt empfängt. Wenn die Ausgabe-PIN (s) Ihres Filters von [**cbaseoutputpin**](cbaseoutputpin.md)abgeleitet ist, rufen Sie die [**cbaseoutputpin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




