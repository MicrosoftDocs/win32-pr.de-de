---
description: Die DeliverEndOfStream-Methode übermittelt eine End-of-Stream-Benachrichtigung an den verbundenen Eingabepin.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: CBaseOutputPin.DeliverEndOfStream-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c13463ae4effb9fee31ad7c9201ad5af6fd406099c5259c2e6fdff9dcbb62798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814190"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a>CBaseOutputPin.DeliverEndOfStream-Methode

Die `DeliverEndOfStream` -Methode übermittelt eine End-of-Stream-Benachrichtigung an den verbundenen Eingabepin.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Pin ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**IPin::EndOfStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) auf dem Eingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




