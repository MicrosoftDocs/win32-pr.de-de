---
description: 'CTransformOutputPin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: CTransformOutputPin.CheckMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3894e701b22f6380e591eccf978e84a1321f57a84485cea8a6e3116181f3f2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538460"
---
# <a name="ctransformoutputpincheckmediatype-method"></a>CTransformOutputPin.CheckMediaType-Methode

Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Mtin* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der Eingabepin des Filters ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode implementiert die rein virtuelle [**CBasePin::CheckMediaType-Methode.**](cbasepin-checkmediatype.md) Die -Methode schlägt fehl, wenn der Eingabepin des Filters nicht verbunden ist. Andernfalls ruft sie die [**CTransformFilter::CheckTransform-Methode**](ctransformfilter-checktransform.md) des Filters auf, die ebenfalls rein virtuell ist. Die abgeleitete Klasse des Filters muss **CheckTransform** implementieren, das bestimmt, ob der vorgeschlagene Ausgabemedientyp mit dem Eingabemedientyp kompatibel ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




