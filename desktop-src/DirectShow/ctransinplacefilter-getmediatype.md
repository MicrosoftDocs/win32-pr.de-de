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
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094808"
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

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CTransformFilter::GetMediaType-Methode.**](ctransformfilter-getmediatype.md) In der **CTransInPlaceFilter-Klasse** ruft jeder Pin den gegenüberliegenden verbundenen Pin auf, um bevorzugte Medientypen zu aufzählen. Der Eingabepin ruft den Eingabepin des Downstreamfilters auf, und der Ausgabepin ruft den Ausgabepin des Upstreamfilters auf. Daher wird die -Methode `GetMediaType` des Filters nie aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




