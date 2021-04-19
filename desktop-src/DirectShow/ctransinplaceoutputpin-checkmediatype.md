---
description: Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Ctransinplaceoutputpin. checkmediatype-Methode (transip. h)
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
ms.openlocfilehash: b0a422851bc7e09075076decc39d57b85d1052ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367611"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a>Ctransinplaceoutputpin. checkmediatype-Methode

Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                                | Beschreibung                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                 |
| <dl> <dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> </dl> | Der Medientyp wurde nicht akzeptiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**ctransformoutputpin:: checkmediatype**](ctransformoutputpin-checkmediatype.md) -Methode.

Wenn der Filter bereits Streaming ist und zwei Zuweisungen verwendet, lehnt diese Methode alle Formatänderungen ab. Andernfalls ruft diese Methode die [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters auf, um den Medientyp zu überprüfen. Wenn die eingabepin verbunden ist, wird auch die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Methode für die upstreamausgabepin aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceoutputpin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




