---
description: 'CTransInPlaceInputPin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: CTransInPlaceInputPin.CheckMediaType-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5de3cec87d740db42824b0d7abf1ee4bfc6aeecb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094798"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>CTransInPlaceInputPin.CheckMediaType-Methode

Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der vorgeschlagene Medientyp akzeptabel ist. Andernfalls wird S \_ FALSE oder ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CTransformInputPin::CheckMediaType-Methode.**](ctransforminputpin-checkmediatype.md) Sie ruft die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) des Filters auf, um den Eingabetyp zu überprüfen. Wenn der Ausgabepin verbunden ist, ruft diese Methode auch die [**IPin::QueryAccept-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Downstreameingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceInputPin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




