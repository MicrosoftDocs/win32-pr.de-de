---
description: Die Run-Methode benachrichtigt den Pin, dass der Filter jetzt ausgeführt wird.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: CBasePin.Run-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f145a827546a9258ee2968d0348ab7725147bb47132f5df5acbd2865a45b78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429810"
---
# <a name="cbasepinrun-method"></a>CBasePin.Run-Methode

Die `Run` -Methode benachrichtigt den Pin, dass der Filter jetzt ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tStart* 
</dt> <dd>

Startzeit, die an die [**IMediaFilter::Run-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) des Filters übergeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Wenn der Filter von angehalten in ausgeführt wird, ruft die [**CBaseFilter-Klasse**](cbasefilter.md) diese Methode an allen Pins des Filters auf.

Diese Methode führt in der Basisklasse nichts aus. Abgeleitete Klassen können diese Methode überschreiben. Beispielsweise kann ein Pin einen Arbeitsthread starten, der Beispiele übermittelt.

Der interne Zustand des Filtergraph-Managers wird erst aktualisiert, nachdem diese Memberfunktion zurückgegeben wurde. Testen Sie daher nicht den Zustand dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




