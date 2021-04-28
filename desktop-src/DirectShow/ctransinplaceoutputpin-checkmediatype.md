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
ms.openlocfilehash: 66cd29758e0b2d63db88db8b998cc79ec12efdd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094718"
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

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                                | Beschreibung                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                 |
| <dl> <dt>**VFW \_ \_ E-TYP \_ NICHT \_ AKZEPTIERT**</dt> </dl> | Der Medientyp wird nicht akzeptiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CTransformOutputPin::CheckMediaType-Methode.**](ctransformoutputpin-checkmediatype.md)

Wenn der Filter bereits streamingt und zwei Zuweisungen verwendet, lehnt diese Methode formatierte Änderungen ab. Andernfalls ruft diese Methode die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) des Filters auf, um den Medientyp zu überprüfen. Wenn der Eingabepin verbunden ist, ruft er auch die [**IPin::QueryAccept-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Upstreamausgabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




