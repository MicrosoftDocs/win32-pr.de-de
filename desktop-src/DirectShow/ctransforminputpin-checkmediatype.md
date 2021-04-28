---
description: 'CTransformInputPin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: CTransformInputPin.CheckMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084998"
---
# <a name="ctransforminputpincheckmediatype-method"></a>CTransformInputPin.CheckMediaType-Methode

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

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode implementiert die rein virtuelle [**CBasePin::CheckMediaType-Methode.**](cbasepin-checkmediatype.md) Sie ruft die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) des Filters auf, die ebenfalls rein virtuell ist. Die abgeleitete Klasse des Filters muss **CheckInputType** implementieren, um zu bestimmen, ob ein angegebener Eingabetyp akzeptabel ist.

Wenn der Ausgabepin des Filters verbunden ist, ruft diese Methode auch die [**CTransformFilter::CheckTransform-Methode**](ctransformfilter-checktransform.md) des Filters auf, um zu bestimmen, ob der Eingabetyp mit dem Ausgabetyp kompatibel ist. Die **CheckTransform-Methode** ist ebenfalls rein virtuell.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




