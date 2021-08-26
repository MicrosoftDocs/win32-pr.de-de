---
description: Die CBaseInputPin-Methode startet einen Leerungsvorgang. Diese Methode implementiert die IPin::BeginFlush-Methode.
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: CBaseInputPin.BeginFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b9e5e4e97a3a010523f61cc9efedf224d8dfc7fa373c9514b6d38dc0105d2d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103210"
---
# <a name="cbaseinputpinbeginflush-method"></a>CBaseInputPin.BeginFlush-Methode

Die `CBaseInputPin` -Methode startet einen Leerungsvorgang. Diese Methode implementiert die [**IPin::BeginFlush-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt das [**CBaseInputPin::m \_ bFlushing-Flag**](cbaseinputpin-m-bflushing.md) auf **TRUE** fest, wodurch die [**CBaseInputPin::Receive-Methode**](cbaseinputpin-receive.md) weitere Stichproben ablehnt.

Die abgeleitete Klasse muss diese Methode überschreiben und die folgenden Schritte ausführen:

1.  Rufen Sie die [**IPin::BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) für downstream-Eingabepins auf. Wenn der Pin noch keine Medienbeispiele nachgeschaltet hat, können Sie diesen Schritt überspringen. Wenn Ihre Ausgabepins von der [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) abgeleitet werden, können Sie die [**CBaseOutputPin::D eliverBeginFlush-Methode**](cbaseoutputpin-deliverbeginflush.md) aufrufen.
2.  Rufen Sie die Basisklassenmethode auf.
3.  Beginnen Sie mit dem Verwerfen von Daten in der Warteschlange.
4.  Gibt von blockierten Aufrufen der **Receive-Methode** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




