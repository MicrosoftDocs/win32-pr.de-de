---
description: Die SetMediaType-Methode wird aufgerufen, wenn der Medientyp an einem der Pins des Filters festgelegt wird.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: CTransformFilter.SetMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc9331a532f6748de4e03c6972fdd555e4d5e11516d946bbd131da9acab364c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584940"
---
# <a name="ctransformfiltersetmediatype-method"></a>CTransformFilter.SetMediaType-Methode

Die `SetMediaType` -Methode wird aufgerufen, wenn der Medientyp für einen der Pins des Filters festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*direction* 
</dt> <dd>

Member des [**PIN DIRECTION-Enumerationstyps, \_**](/windows/win32/api/strmif/ne-strmif-pin_direction) der einen Pin für den Filter (Eingabe oder Ausgabe) angibt.

</dd> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die Methoden [**CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) und [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) rufen diese Methode auf, wenn der Medientyp eines Pins festgelegt ist. Diese Methode führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




