---
description: 'CTransInPlaceFilter.GetMediaType-Methode: Die GetMediaType-Methode ruft einen bevorzugten Medientyp für den Ausgabepin ab.'
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: CTransInPlaceFilter.GetMediaType-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a714d3dba30b3038d6c04ecedd51db4196a3c4d899d7c607dd12f9a068f8a803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079300"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>CTransInPlaceFilter.GetMediaType-Methode

Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp für den Ausgabepin ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iPosition* 
</dt> <dd>

Nullbasierter Indexwert.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ UNEXPECTED zurück.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CTransformFilter::GetMediaType-Methode.**](ctransformfilter-getmediatype.md) In der **CTransInPlaceFilter-Klasse** ruft jeder Pin den gegenüberliegenden verbundenen Pin auf, um bevorzugte Medientypen zu aufzählen. Der Eingabepin ruft den Eingabepin des Downstreamfilters auf, und der Ausgabepin ruft den Ausgabepin des Upstreamfilters auf. Daher wird die -Methode `GetMediaType` des Filters nie aufgerufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




