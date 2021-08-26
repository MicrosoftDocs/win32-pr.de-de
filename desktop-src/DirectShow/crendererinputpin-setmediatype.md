---
description: Die SetMediaType-Methode legt den Medientyp für die Verbindung fest. Diese Methode überschreibt die CBasePin::SetMediaType-Methode.
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: CRendererInputPin.SetMediaType-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f248e15c3965305719269a19a1f2ff2c8feddfe0e57b6349985d9133e38789
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054400"
---
# <a name="crendererinputpinsetmediatype-method"></a>CRendererInputPin.SetMediaType-Methode

Die `SetMediaType` -Methode legt den Medientyp für die Verbindung fest. Diese Methode überschreibt die [**CBasePin::SetMediaType-Methode.**](cbasepin-setmediatype.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CRendererInputPin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




