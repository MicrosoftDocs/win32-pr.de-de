---
description: 'CTransInPlaceOutputPin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: CTransInPlaceOutputPin.CheckMediaType-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2816d148af2a7514dc28a71036402f3781e47a0144848a2ea81bbb94d339f961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999030"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a>CTransInPlaceOutputPin.CheckMediaType-Methode

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

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                | Beschreibung                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                 |
| <dl> <dt>**VFW \_ \_ E-TYP \_ NICHT \_ AKZEPTIERT**</dt> </dl> | Medientyp nicht akzeptiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CTransformOutputPin::CheckMediaType-Methode.**](ctransformoutputpin-checkmediatype.md)

Wenn der Filter bereits gestreamt wird und zwei Zuweisungen verwendet, lehnt diese Methode alle Formatänderungen ab. Andernfalls ruft diese Methode die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) des Filters auf, um den Medientyp zu überprüfen. Wenn der Eingabepin verbunden ist, ruft er auch die [**IPin::QueryAccept-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Upstreamausgabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




