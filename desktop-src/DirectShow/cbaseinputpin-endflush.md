---
description: Die EndFlush-Methode beendet einen Leerungsvorgang. Implementiert die IPin::EndFlush-Methode.
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: CBaseInputPin.EndFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fba4c82679ebe96827cd45c9045080fb354cdab25eb562523869e97d533c5f2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056350"
---
# <a name="cbaseinputpinendflush-method"></a>CBaseInputPin.EndFlush-Methode

Die `EndFlush` -Methode beendet einen Leerungsvorgang. Implementiert die [**IPin::EndFlush-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt das [**Flag CBaseInputPin::m \_ bFlushing**](cbaseinputpin-m-bflushing.md) auf **TRUE** fest, wodurch die [**CBaseInputPin::Receive-Methode**](cbaseinputpin-receive.md) Beispiele akzeptieren kann.

Die abgeleitete Klasse muss diese Methode überschreiben und die folgenden Schritte ausführen:

1.  Geben Sie alle gepufferten Daten frei, und warten Sie, bis alle Stichproben in der Warteschlange verworfen wurden.
2.  Löschen Sie alle [**ausstehenden EC \_ COMPLETE-Benachrichtigungen.**](ec-complete.md)
3.  Rufen Sie die Basisklassenmethode auf.
4.  Rufen [**Sie IPin::EndFlush für**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) Downstreameingabepins auf. Wenn die Stecknadel noch keine Medienbeispiele nachgelagert hat, können Sie diesen Schritt überspringen. Wenn Ihre Ausgabepins von der [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) ableiten, können Sie die [**CBaseOutputPin::D eliverEndFlush-Methode**](cbaseoutputpin-deliverendflush.md) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




