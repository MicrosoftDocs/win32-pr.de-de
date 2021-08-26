---
description: Die CheckInputType-Methode überprüft, ob ein angegebener Medientyp für die Eingabe akzeptabel ist.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: CTransformFilter.CheckInputType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ef410ac8d96160b39ca9b7103e5125be8619169ba6b287a32b8769e57a0cbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053620"
---
# <a name="ctransformfiltercheckinputtype-method"></a>CTransformFilter.CheckInputType-Methode

Die `CheckInputType` -Methode überprüft, ob ein angegebener Medientyp für die Eingabe akzeptabel ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Mtin* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                                | Beschreibung                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Der Medientyp ist akzeptabel.<br/>     |
| <dl> <dt>**VFW \_ \_ E-TYP \_ NICHT \_ AKZEPTIERT**</dt> </dl> | Der Medientyp ist nicht akzeptabel.<br/> |



 

## <a name="remarks"></a>Hinweise

Die abgeleitete Klasse muss diese Methode implementieren. Geben Sie S \_ OK zurück, wenn das vorgeschlagene Eingabeformat akzeptabel ist, andernfalls ein Fehlercode.

Diese Methode muss nicht überprüfen, ob das Eingabeformat mit dem Ausgabeformat kompatibel ist (sofern verfügbar). Der Eingabepin überprüft dies durch Aufrufen der [**CheckTransform-Methode.**](ctransformfilter-checktransform.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




