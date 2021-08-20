---
description: Die OnReceiveFirstSample-Methode wird aufgerufen, wenn der Filter eine Stichprobe empfängt, während er angehalten wurde.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: CBaseRenderer.OnReceiveFirstSample-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 882a356f47aa146ec8ba1b06d7af43235c8213334c0d82d0a241c590654bf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157700"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>CBaseRenderer.OnReceiveFirstSample-Methode

Die `OnReceiveFirstSample` -Methode wird aufgerufen, wenn der Filter ein Beispiel empfängt, während er angehalten wurde.

## <a name="syntax"></a>Syntax


```C++
virtual void OnReceiveFirstSample(
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

Die [**CBaseRenderer::Receive-Methode**](cbaserenderer-receive.md) ruft diese Methode auf. In der Basisklasse wird nichts verwendet, aber die abgeleitete Klasse kann sie überschreiben. Diese Methode ist in erster Linie für Videorenderer vorgesehen. Wenn ein Videorenderer angehalten wird, zeigt er in der Regel das erste Beispiel als Stillbild an.

Das Suchen des Graphen während des Anhaltens führt auch dazu, dass diese Methode aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




