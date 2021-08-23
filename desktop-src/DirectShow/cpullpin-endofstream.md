---
description: Die EndOfStream-Methode wird aufgerufen, nachdem das -Objekt das letzte Beispiel übermittelt hat. Die abgeleitete Klasse muss diese Methode implementieren.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: CPullPin.EndOfStream-Methode (Pullpin.h)
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
ms.openlocfilehash: 9544a5f35c42fcf65bff58ad63d6f22bdd4dd817ae91951b01ffe122bce50c5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954019"
---
# <a name="cpullpinendofstream-method"></a>CPullPin.EndOfStream-Methode

Die `EndOfStream` -Methode wird aufgerufen, nachdem das -Objekt das letzte Beispiel übermittelt hat. Die abgeleitete Klasse muss diese Methode implementieren.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) auf jedem Downstreameingabepin aufzurufen, der Daten von diesem Objekt empfängt. Wenn die Ausgabepins Ihres Filters von [**CBaseOutputPin**](cbaseoutputpin.md)abgeleitet sind, rufen Sie die [**CBaseOutputPin::D eliverEndOfStream-Methode**](cbaseoutputpin-deliverendofstream.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




