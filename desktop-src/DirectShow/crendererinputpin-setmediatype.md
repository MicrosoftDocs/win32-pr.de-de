---
description: 'Die setmediatype-Methode legt den Medientyp für die Verbindung fest. Diese Methode überschreibt die cbasepin:: setmediatype-Methode.'
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Crendererinputpin. setmediatype-Methode (renbase. h)
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
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374007"
---
# <a name="crendererinputpinsetmediatype-method"></a>Crendererinputpin. setmediatype-Methode

Die- `SetMediaType` Methode legt den Medientyp für die Verbindung fest. Diese Methode überschreibt die [**cbasepin:: setmediatype**](cbasepin-setmediatype.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crendererinputpin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




