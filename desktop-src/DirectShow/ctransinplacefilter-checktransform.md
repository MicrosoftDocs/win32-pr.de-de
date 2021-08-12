---
description: Die CheckTransform-Methode überprüft, ob ein Eingabemedientyp mit einem Ausgabemedientyp kompatibel ist. Diese Methode überschreibt die CTransformFilter::CheckTransform-Methode.
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: CTransInPlaceFilter.CheckTransform-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49b7f4aaac21cf6a55360e2e1b970bd9dfa62c0422241f7356871117e138d57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654959"
---
# <a name="ctransinplacefilterchecktransform-method"></a>CTransInPlaceFilter.CheckTransform-Methode

Die `CheckTransform` -Methode überprüft, ob ein Eingabemedientyp mit einem Ausgabemedientyp kompatibel ist. Diese Methode überschreibt die [**CTransformFilter::CheckTransform-Methode.**](ctransformfilter-checktransform.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Mtin* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Eingabetyp angibt.

</dd> <dt>

*mtOut* 
</dt> <dd>

Zeiger auf ein **CMediaType-Objekt,** das den Ausgabetyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Der **CTransInPlace-Filter** ruft nie `CheckTransform` auf. Stattdessen verwenden alle Pin-Verbindungen [**CTransformFilter::CheckInputType,**](ctransformfilter-checkinputtype.md) um den Medientyp zu überprüfen. Dabei wird davon ausgegangen, dass die Eingabe- und Ausgabetypen immer übereinstimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




