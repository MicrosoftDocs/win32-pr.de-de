---
description: Die OnRenderStart-Methode wird aufgerufen, wenn das Rendering gestartet wird.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: CBaseRenderer.OnRenderStart-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626dc1dbcb82aeec94ebe514e686d197cb17bbdd7807ac38057412617182bf55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157653"
---
# <a name="cbaserendereronrenderstart-method"></a>CBaseRenderer.OnRenderStart-Methode

Die `OnRenderStart` -Methode wird aufgerufen, wenn das Rendering gestartet wird.

## <a name="syntax"></a>Syntax


```C++
virtual void OnRenderStart(
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

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**CBaseRenderer::Render-Methode**](cbaserenderer-render.md) ruft diese Methode auf. In der Basisklasse wird nichts verwendet, aber die abgeleitete Klasse kann sie überschreiben. beispielsweise zum Sammeln von Qualitätskontrolldaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




