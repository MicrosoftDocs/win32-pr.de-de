---
description: Mit der ScheduleSample-Methode wird ein Beispiel für das Rendering geplant.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: CBaseRenderer.ScheduleSample-Methode (Renbase.h)
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
ms.openlocfilehash: 88e728b90078ab11a6215dad60a88b819b2c513071637e2aa5c6b6ed7226189b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157592"
---
# <a name="cbaserendererschedulesample-method"></a>CBaseRenderer.ScheduleSample-Methode

Die `ScheduleSample` -Methode geplant ein Beispiel für das Rendering.

## <a name="syntax"></a>Syntax


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn das Beispiel geplant wurde, oder **FALSE,** wenn das Beispiel gelöscht wurde.

## <a name="remarks"></a>Hinweise

Diese Methode bestimmt zuerst, ob das Beispiel sofort gerendert, in der Zukunft gerendert oder gelöscht werden soll. (Dazu wird die [**CBaseRenderer::GetSampleTimes-Methode**](cbaserenderer-getsampletimes.md) aufruft.) Wenn das Beispiel sofort gerendert werden soll, signalisiert die -Methode das [**CBaseRenderer::m-RenderEvent-Ereignis. \_**](cbaserenderer-m-renderevent.md) Wenn das Beispiel in Zukunft gerendert werden soll, ruft die -Methode die [**IReferenceClock::AdviseTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) für die Planung auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




