---
description: 'CBaseRenderer.GetPin-Methode: Die GetPin-Methode ruft einen Pin ab.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: CBaseRenderer.GetPin-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c85b1a33abec4dfd10cf093e8673e270e7df02533846791a5d5d37702b51313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822701"
---
# <a name="cbaserenderergetpin-method"></a>CBaseRenderer.GetPin-Methode

Die `GetPin` -Methode ruft einen Pin ab.

## <a name="syntax"></a>Syntax


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Nummer des angegebenen Pins. Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**CBaseRenderer::m \_ pInputPin-Zeiger**](cbaserenderer-m-pinputpin.md) zurück.

## <a name="remarks"></a>Hinweise

Diese Methode implementiert die [**CBaseFilter::GetPin-Methode,**](cbasefilter-getpin.md) die in der **CBaseFilter-Klasse** rein virtuell ist. Der Filter unterstützt genau einen Pin (den Eingabepin). Beim ersten Aufruf dieser Methode wird die Stecknadel als neues [**CRendererInputPin-Objekt**](crendererinputpin.md) erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




