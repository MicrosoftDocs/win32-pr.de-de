---
description: Die schedulesample-Methode plant ein Beispiel für das Rendering.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Cbaserderderer. schedulesample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369224"
---
# <a name="cbaserendererschedulesample-method"></a>Cbaserderderer. schedulesample-Methode

Die- `ScheduleSample` Methode plant ein Beispiel für das Rendering.

## <a name="syntax"></a>Syntax


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn das Beispiel geplant wurde, oder " **false** ", wenn das Beispiel gelöscht wurde.

## <a name="remarks"></a>Bemerkungen

Diese Methode bestimmt zunächst, ob das Beispiel sofort gerendert, in der Zukunft gerendert oder gelöscht werden soll. (Hierzu wird die [**cbaserdenderer:: getsampletimes**](cbaserenderer-getsampletimes.md) -Methode aufgerufen.) Wenn das Beispiel sofort gerendert werden soll, signalisiert die Methode das Ereignis [**cbaserenderer:: m \_ renderevent**](cbaserenderer-m-renderevent.md) . Wenn das Beispiel in Zukunft gerendert werden soll, ruft die-Methode die [**IReferenceClock:: advisettime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) -Methode für die Planung auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




